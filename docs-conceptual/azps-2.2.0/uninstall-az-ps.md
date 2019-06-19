---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: eaabd8014368f7ea8f4c9504e58d920dad8a6518
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498617"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="04e11-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04e11-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="04e11-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="04e11-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="04e11-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="04e11-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="04e11-106">Caso você encontre um bug, ficaremos felizes se você [registrar um problema do GitHub](https://github.com/azure/azure-powershell/issues) para que ele possa ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="04e11-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="04e11-107">Desinstalar o módulo Az</span><span class="sxs-lookup"><span data-stu-id="04e11-107">Uninstall the Az module</span></span>

<span data-ttu-id="04e11-108">Para desinstalar os módulos Az, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="04e11-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="04e11-109">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="04e11-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="04e11-110">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="04e11-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="04e11-111">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04e11-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="04e11-112">Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="04e11-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="04e11-113">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="04e11-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="04e11-114">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="04e11-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="04e11-115">Você precisará ter acesso de administrador para executar esse script em um escopo diferente de `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="04e11-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="04e11-116">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04e11-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="04e11-117">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04e11-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="04e11-118">À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="04e11-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="04e11-119">Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="04e11-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="04e11-120">Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="04e11-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="04e11-121">Para sua conveniência, o script a seguir desinstala todas as versões do Az __exceto__ a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="04e11-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="04e11-122">Desinstalar o módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="04e11-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="04e11-123">Se você instalou o módulo Az em seu sistema e gostaria de desinstalar o AzureRM, há duas opções que não exigem a execução do script `Uninstall-AllModules` acima.</span><span class="sxs-lookup"><span data-stu-id="04e11-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="04e11-124">Qual método você segue depende de como instalou o módulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="04e11-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="04e11-125">Caso não tenha certeza do método de instalação original, siga as etapas para desinstalar um MSI primeiro.</span><span class="sxs-lookup"><span data-stu-id="04e11-125">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="04e11-126">Desinstale o MSI do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04e11-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="04e11-127">Se você instalou módulos AzureRM do Azure PowerShell usando o pacote MSI, realize a desinstalação por meio do sistema do Windows em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04e11-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="04e11-128">Plataforma</span><span class="sxs-lookup"><span data-stu-id="04e11-128">Platform</span></span> | <span data-ttu-id="04e11-129">Instruções</span><span class="sxs-lookup"><span data-stu-id="04e11-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="04e11-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="04e11-130">Windows 10</span></span> | <span data-ttu-id="04e11-131">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="04e11-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="04e11-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04e11-132">Windows 7</span></span> </br><span data-ttu-id="04e11-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04e11-133">Windows 8</span></span> | <span data-ttu-id="04e11-134">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="04e11-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="04e11-135">Nessa tela, você deverá ver __Azure PowerShell__ na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="04e11-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="04e11-136">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="04e11-136">This is the app to uninstall.</span></span> <span data-ttu-id="04e11-137">Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.</span><span class="sxs-lookup"><span data-stu-id="04e11-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="04e11-138">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="04e11-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="04e11-139">Se instalou o AzureRM com o PowerShellGet, pode remover os módulos com o comando [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponível como parte do módulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="04e11-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="04e11-140">Isso remove _todos_ os módulos do AzureRM de sua máquina, mas requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="04e11-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="04e11-141">Se você não puder executar o comando `Uninstall-AzureRM` com êxito, use o [script `Uninstall-AllModules`](#uninstall-script) fornecido neste artigo com a seguinte invocação:</span><span class="sxs-lookup"><span data-stu-id="04e11-141">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```