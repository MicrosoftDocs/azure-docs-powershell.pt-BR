---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037686"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="1ab61-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ab61-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="1ab61-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="1ab61-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="1ab61-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="1ab61-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="1ab61-106">Se você encontrou um erro, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1ab61-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="1ab61-107">Desinstalar o MSI ou o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="1ab61-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="1ab61-108">Se você instalou o Azure PowerShell usando o pacote MSI ou o Web Platform Installer, desinstale por meio do sistema do Windows em vez de usar o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ab61-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="1ab61-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="1ab61-109">Platform</span></span> | <span data-ttu-id="1ab61-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="1ab61-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="1ab61-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1ab61-111">Windows 10</span></span> | <span data-ttu-id="1ab61-112">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="1ab61-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="1ab61-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ab61-113">Windows 7</span></span> </br><span data-ttu-id="1ab61-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ab61-114">Windows 8</span></span> | <span data-ttu-id="1ab61-115">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="1ab61-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="1ab61-116">Nessa tela, você deverá ver "Azure PowerShell" na lista de programas e poderá desinstalar a partir daí.</span><span class="sxs-lookup"><span data-stu-id="1ab61-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="1ab61-117">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ab61-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="1ab61-118">Se você instalou o Azure PowerShell usando o PowerShellGet, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="1ab61-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="1ab61-119">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="1ab61-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="1ab61-120">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="1ab61-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="1ab61-121">A desinstalação poderá ser complicada se você tiver várias versões instaladas do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ab61-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="1ab61-122">O script a seguir pode ser usado para remover completamente uma única versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ab61-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="1ab61-123">O script consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="1ab61-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="1ab61-124">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="1ab61-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="1ab61-125">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ab61-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="1ab61-126">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ab61-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="1ab61-127">À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="1ab61-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="1ab61-128">Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="1ab61-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="1ab61-129">Se esse script não puder corresponder a uma dependência exata com a mesma versão a desinstalar, ele não desinstalará _nenhuma_ versão dessa dependência.</span><span class="sxs-lookup"><span data-stu-id="1ab61-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="1ab61-130">Isso ocorre porque pode haver outras versões do módulo de destino no sistema que contam com essas dependências.</span><span class="sxs-lookup"><span data-stu-id="1ab61-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="1ab61-131">Nesse caso, as versões disponíveis da dependência são listadas.</span><span class="sxs-lookup"><span data-stu-id="1ab61-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="1ab61-132">Então, você poderá remover qualquer uma das versões antigas manualmente com o `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="1ab61-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="1ab61-133">Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="1ab61-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="1ab61-134">Para sua conveniência, o script a seguir irá desinstalar todas as versões do AzureRM __exceto__ a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="1ab61-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
