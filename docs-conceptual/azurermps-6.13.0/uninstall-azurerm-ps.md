---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 7456e45fe9a94d3c1e809dfd075a090448001607
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982803"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="aeb57-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aeb57-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="aeb57-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="aeb57-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="aeb57-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="aeb57-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="aeb57-106">Se você encontrar um bug, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="aeb57-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-msi"></a><span data-ttu-id="aeb57-107">Desinstalar o MSI</span><span class="sxs-lookup"><span data-stu-id="aeb57-107">Uninstall MSI</span></span>

<span data-ttu-id="aeb57-108">Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeb57-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="aeb57-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="aeb57-109">Platform</span></span> | <span data-ttu-id="aeb57-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="aeb57-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="aeb57-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="aeb57-111">Windows 10</span></span> | <span data-ttu-id="aeb57-112">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="aeb57-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="aeb57-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aeb57-113">Windows 7</span></span> </br><span data-ttu-id="aeb57-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aeb57-114">Windows 8</span></span> | <span data-ttu-id="aeb57-115">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="aeb57-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="aeb57-116">Nessa tela, você deverá ver "Azure PowerShell" na lista de programas e poderá desinstalar a partir daí.</span><span class="sxs-lookup"><span data-stu-id="aeb57-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="aeb57-117">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="aeb57-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="aeb57-118">Se você instalou o Azure PowerShell usando o PowerShellGet, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="aeb57-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="aeb57-119">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="aeb57-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="aeb57-120">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="aeb57-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="aeb57-121">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeb57-121">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="aeb57-122">Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="aeb57-122">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="aeb57-123">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="aeb57-123">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="aeb57-124">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="aeb57-124">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="aeb57-125">Você precisará ter acesso de administrador para executar esse script em um escopo diferente de `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="aeb57-125">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="aeb57-126">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeb57-126">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="aeb57-127">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aeb57-127">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="aeb57-128">À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="aeb57-128">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="aeb57-129">Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="aeb57-129">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="aeb57-130">Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="aeb57-130">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="aeb57-131">Para sua conveniência, o script a seguir irá desinstalar todas as versões do AzureRM __exceto__ a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="aeb57-131">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
