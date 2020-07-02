---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85267804"
---
# <a name="uninstall-the-azure-powershell-module"></a>Desinstalar o módulo Azure PowerShell

Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema. Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback). Caso você encontre um bug, ficaremos felizes se você [registrar um problema do GitHub](https://github.com/azure/azure-powershell/issues) para que ele possa ser corrigido.

## <a name="uninstall-azure-powershell-from-msi"></a>Desinstalar o Azure PowerShell do MSI

Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.

|         Plataforma         |                      Instruções                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Iniciar > Configurações > Aplicativos                                |
| Windows 7 </br>Windows 8 | Iniciar > Painel de Controle > Programas > Desinstalar um programa |

Nessa tela, você deverá ver **Azure PowerShell** na lista de programas. Esse é o aplicativo a ser desinstalado. Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.

## <a name="uninstall-azure-powershell-from-powershellget"></a>Desinstalar o Azure PowerShell do PowerShellGet

Para desinstalar os módulos Az, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). No entanto, `Uninstall-Module` desinstala apenas um módulo. Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente. A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.

Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes. Em seguida, o script desinstala a versão correta de cada submódulo. Será necessário ter acesso de administrador para executar esse script em um escopo diferente de **Processo** ou **UsuárioAtual**.

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

Para usar essa função, copie e cole o código em sua sessão do PowerShell. O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

À medida que o script for executado, ele exibirá o **Nome**, a **Versão** e o **Estado** de cada submódulo que está sendo desinstalado. Para executar o script para ver apenas o que seria excluído, sem removê-lo, especifique o parâmetro `-WhatIf`.

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> Se esse script não puder corresponder a uma dependência exata com a mesma versão a desinstalar, ele não desinstalará _nenhuma_ versão dessa dependência. Isso ocorre porque pode haver outras versões do módulo de destino no sistema que contam com essas dependências.

Execute o exemplo a seguir para cada versão do Azure PowerShell que você deseja desinstalar. Para sua conveniência, o script a seguir desinstala todas as versões do Az **exceto** a versão mais recente.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Desinstalar o módulo AzureRM

Se você instalou o módulo Az em seu sistema e gostaria de desinstalar o AzureRM, há duas opções que não exigem a execução do script `Uninstall-AzModule` acima. Qual método você segue depende de como instalou o módulo AzureRM. Caso não tenha certeza do método de instalação original, siga as etapas para desinstalar um MSI primeiro.

### <a name="uninstall-azure-powershell-msi"></a>Desinstale o MSI do Azure PowerShell

Se você instalou módulos AzureRM do Azure PowerShell usando o pacote MSI, realize a desinstalação por meio do sistema do Windows em vez do PowerShell.

|         Plataforma         |                      Instruções                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Iniciar > Configurações > Aplicativos                                |
| Windows 7 </br>Windows 8 | Iniciar > Painel de Controle > Programas > Desinstalar um programa |

Nessa tela, você deverá ver o **Azure PowerShell** ou o **Microsoft Azure PowerShell – mês e ano** na lista de programas. Esse é o aplicativo a ser desinstalado. Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.

### <a name="uninstall-from-powershell"></a>Desinstalar pelo PowerShell

Se você instalou o AzureRM com o PowerShellGet, pode remover os módulos com o cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponível como parte do módulo `Az.Accounts`. O exemplo a seguir remove _todos_ os módulos do AzureRM de seu computador, mas requer privilégios de administrador.

```powershell-interactive
Uninstall-AzureRm
```

Se você não puder executar o comando `Uninstall-AzureRM` com êxito, use o [script `Uninstall-AzModule`](#uninstall-script) fornecido neste artigo com a seguinte invocação:

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
