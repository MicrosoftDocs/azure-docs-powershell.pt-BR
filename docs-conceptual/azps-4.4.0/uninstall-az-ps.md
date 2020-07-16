---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/14/2020
ms.locfileid: "86381754"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="06858-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06858-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="06858-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="06858-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="06858-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="06858-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="06858-106">Caso você encontre um bug, ficaremos felizes se você [registrar um problema do GitHub](https://github.com/azure/azure-powershell/issues) para que ele possa ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="06858-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="06858-107">Desinstalar o Azure PowerShell do MSI</span><span class="sxs-lookup"><span data-stu-id="06858-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="06858-108">Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06858-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="06858-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="06858-109">Platform</span></span>         |                      <span data-ttu-id="06858-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="06858-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="06858-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="06858-111">Windows 10</span></span>               | <span data-ttu-id="06858-112">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="06858-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="06858-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06858-113">Windows 7</span></span> </br><span data-ttu-id="06858-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06858-114">Windows 8</span></span> | <span data-ttu-id="06858-115">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="06858-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="06858-116">Nessa tela, você deverá ver **Azure PowerShell** na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="06858-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="06858-117">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="06858-117">This is the app to uninstall.</span></span> <span data-ttu-id="06858-118">Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.</span><span class="sxs-lookup"><span data-stu-id="06858-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershellget"></a><span data-ttu-id="06858-119">Desinstalar o Azure PowerShell do PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="06858-119">Uninstall Azure PowerShell from PowerShellGet</span></span>

<span data-ttu-id="06858-120">Para desinstalar os módulos Az, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="06858-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="06858-121">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="06858-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="06858-122">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="06858-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="06858-123">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06858-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="06858-124">Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="06858-124">To check which versions of Azure PowerShell you've installed, run the following command:</span></span>

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

<span data-ttu-id="06858-125">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="06858-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="06858-126">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="06858-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="06858-127">Será necessário ter acesso de administrador para executar esse script em um escopo diferente de **Processo** ou **UsuárioAtual**.</span><span class="sxs-lookup"><span data-stu-id="06858-127">You need to have administrator access to run this script in a scope other than **Process** or **CurrentUser**.</span></span>

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

<span data-ttu-id="06858-128">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06858-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="06858-129">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06858-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="06858-130">À medida que o script for executado, ele exibirá o **Nome**, a **Versão** e o **Estado** de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="06858-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="06858-131">Para executar o script para ver apenas o que seria excluído, sem removê-lo, especifique o parâmetro `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="06858-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="06858-132">Se esse script não puder corresponder a uma dependência exata com a mesma versão a desinstalar, ele não desinstalará _nenhuma_ versão dessa dependência.</span><span class="sxs-lookup"><span data-stu-id="06858-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="06858-133">Isso ocorre porque pode haver outras versões do módulo de destino no sistema que contam com essas dependências.</span><span class="sxs-lookup"><span data-stu-id="06858-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="06858-134">Execute o exemplo a seguir para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="06858-134">Run the following example for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="06858-135">Para sua conveniência, o script a seguir desinstala todas as versões do Az **exceto** a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="06858-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="06858-136">Desinstalar o módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="06858-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="06858-137">Se você instalou o módulo Az em seu sistema e gostaria de desinstalar o AzureRM, há duas opções que não exigem a execução do script `Uninstall-AzModule` acima.</span><span class="sxs-lookup"><span data-stu-id="06858-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AzModule` script above.</span></span> <span data-ttu-id="06858-138">Qual método você segue depende de como instalou o módulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="06858-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="06858-139">Caso não tenha certeza do método de instalação original, siga as etapas para desinstalar um MSI primeiro.</span><span class="sxs-lookup"><span data-stu-id="06858-139">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="06858-140">Desinstale o MSI do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06858-140">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="06858-141">Se você instalou módulos AzureRM do Azure PowerShell usando o pacote MSI, realize a desinstalação por meio do sistema do Windows em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06858-141">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="06858-142">Plataforma</span><span class="sxs-lookup"><span data-stu-id="06858-142">Platform</span></span>         |                      <span data-ttu-id="06858-143">Instruções</span><span class="sxs-lookup"><span data-stu-id="06858-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="06858-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="06858-144">Windows 10</span></span>               | <span data-ttu-id="06858-145">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="06858-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="06858-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06858-146">Windows 7</span></span> </br><span data-ttu-id="06858-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06858-147">Windows 8</span></span> | <span data-ttu-id="06858-148">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="06858-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="06858-149">Nessa tela, você deverá ver o **Azure PowerShell** ou o **Microsoft Azure PowerShell – mês e ano** na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="06858-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="06858-150">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="06858-150">This is the app to uninstall.</span></span> <span data-ttu-id="06858-151">Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.</span><span class="sxs-lookup"><span data-stu-id="06858-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="06858-152">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="06858-152">Uninstall from PowerShell</span></span>

<span data-ttu-id="06858-153">Se você instalou o AzureRM com o PowerShellGet, pode remover os módulos com o cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponível como parte do módulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="06858-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="06858-154">O exemplo a seguir remove _todos_ os módulos do AzureRM de seu computador, mas requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="06858-154">The following example removes _all_ AzureRM modules from your machine but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="06858-155">Se você não puder executar o comando `Uninstall-AzureRM` com êxito, use o [script `Uninstall-AzModule`](#uninstall-script) fornecido neste artigo com a seguinte invocação:</span><span class="sxs-lookup"><span data-stu-id="06858-155">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AzModule` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
