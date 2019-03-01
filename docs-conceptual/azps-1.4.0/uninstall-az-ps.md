---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837598"
---
# <a name="uninstall-the-azure-powershell-module"></a>Desinstalar o módulo Azure PowerShell

Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema. Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Se você encontrar um bug, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Desinstalar o módulo Az

Para desinstalar os módulos Az, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). No entanto, `Uninstall-Module` desinstala apenas um módulo. Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente. A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.

Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes. Em seguida, o script desinstala a versão correta de cada submódulo. Você precisará ter acesso de administrador para executar esse script em um escopo diferente de `Process` ou `CurrentUser`.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Para usar essa função, copie e cole o código em sua sessão do PowerShell. O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado. Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar. Para sua conveniência, o script a seguir desinstala todas as versões do Az __exceto__ a versão mais recente.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Desinstalar o módulo AzureRM

Se você tiver o módulo Az instalado em seu sistema e quiser desinstalar o AzureRM, há duas opções simples que não exigem a execução do script `Uninstall-AllModules` acima. O método seguido depende de como você instalou o AzureRM.
Se você não tiver certeza, verifique as etapas para desinstalar um MSI primeiro.

### <a name="uninstall-azure-powershell-msi"></a>Desinstale o MSI do Azure PowerShell

Se você instalou módulos AzureRM do Azure PowerShell usando o pacote MSI, realize a desinstalação por meio do sistema do Windows em vez do PowerShell.

| Plataforma | Instruções |
|----------|--------------|
| Windows 10 | Iniciar > Configurações > Aplicativos |
| Windows 7 </br>Windows 8 | Iniciar > Painel de Controle > Programas > Desinstalar um programa |

Nessa tela, você deverá ver __Azure PowerShell__ na lista de programas. Esse é o aplicativo a ser desinstalado.

### <a name="uninstall-from-powershell"></a>Desinstalar pelo PowerShell

Se tiver instalado o AzureRM a partir do PowerShellGet, poderá remover os módulos com o novo comando `Uninstall-AzureRM`. Isso remove _todos_ os módulos do AzureRM de sua máquina, mas requer privilégios de administrador.

```powershell-interactive
Uninstall-AzureRm
```

Se você não puder executar o comando `Uninstall-AzureRM` de forma eficaz, use o script `Uninstall-AllModules` fornecido neste artigo.
