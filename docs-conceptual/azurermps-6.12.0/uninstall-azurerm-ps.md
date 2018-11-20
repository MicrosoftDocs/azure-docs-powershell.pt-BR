---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: bf1f81b4929ec066eeb888da4ba1303430f026b4
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574695"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="e36b4-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e36b4-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="e36b4-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="e36b4-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="e36b4-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="e36b4-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="e36b4-106">Se você encontrar um bug, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e36b4-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="e36b4-107">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="e36b4-107">Uninstall from PowerShell</span></span>

<span data-ttu-id="e36b4-108">Se você instalou o Azure PowerShell usando o PowerShellGet, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="e36b4-108">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="e36b4-109">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="e36b4-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="e36b4-110">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="e36b4-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="e36b4-111">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e36b4-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="e36b4-112">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="e36b4-112">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="e36b4-113">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="e36b4-113">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.minimumVersion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="e36b4-114">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e36b4-114">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="e36b4-115">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e36b4-115">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="e36b4-116">À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="e36b4-116">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="e36b4-117">Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="e36b4-117">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="e36b4-118">Para sua conveniência, o script a seguir irá desinstalar todas as versões do AzureRM __exceto__ a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="e36b4-118">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a><span data-ttu-id="e36b4-119">Desinstalar o MSI</span><span class="sxs-lookup"><span data-stu-id="e36b4-119">Uninstall MSI</span></span>

<span data-ttu-id="e36b4-120">Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e36b4-120">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="e36b4-121">Plataforma</span><span class="sxs-lookup"><span data-stu-id="e36b4-121">Platform</span></span> | <span data-ttu-id="e36b4-122">Instruções</span><span class="sxs-lookup"><span data-stu-id="e36b4-122">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="e36b4-123">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e36b4-123">Windows 10</span></span> | <span data-ttu-id="e36b4-124">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e36b4-124">Start > Settings > Apps</span></span> |
| <span data-ttu-id="e36b4-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e36b4-125">Windows 7</span></span> </br><span data-ttu-id="e36b4-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e36b4-126">Windows 8</span></span> | <span data-ttu-id="e36b4-127">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="e36b4-127">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="e36b4-128">Nessa tela, você deverá ver "Azure PowerShell" na lista de programas e poderá desinstalar a partir daí.</span><span class="sxs-lookup"><span data-stu-id="e36b4-128">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>
