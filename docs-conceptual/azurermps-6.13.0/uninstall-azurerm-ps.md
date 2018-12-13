---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: a35814f4411dd9cab75fa36bd13ff087cdec8f9b
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217058"
---
# <a name="uninstall-the-azure-powershell-module"></a>Desinstalar o módulo Azure PowerShell

Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema. Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Se você encontrar um bug, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-from-powershell"></a>Desinstalar pelo PowerShell

Se você instalou o Azure PowerShell usando o PowerShellGet, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). No entanto, `Uninstall-Module` desinstala apenas um módulo. Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente. A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.

Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado. Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar. Para sua conveniência, o script a seguir irá desinstalar todas as versões do AzureRM __exceto__ a versão mais recente.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a>Desinstalar o MSI

Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.

| Plataforma | Instruções |
|----------|--------------|
| Windows 10 | Iniciar > Configurações > Aplicativos |
| Windows 7 </br>Windows 8 | Iniciar > Painel de Controle > Programas > Desinstalar um programa |

Nessa tela, você deverá ver "Azure PowerShell" na lista de programas e poderá desinstalar a partir daí.
