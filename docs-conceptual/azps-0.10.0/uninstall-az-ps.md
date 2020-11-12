---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ff9135839b01ad9a1bf10e5969cd3226fe492145
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408846"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d5357-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5357-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="d5357-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="d5357-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d5357-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d5357-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="d5357-106">Caso você encontre um bug, ficaremos felizes se você [registrar um problema do GitHub](https://github.com/azure/azure-powershell/issues) para que ele possa ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="d5357-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="d5357-107">Desinstalar o módulo Az PowerShell do MSI</span><span class="sxs-lookup"><span data-stu-id="d5357-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="d5357-108">Se você tiver instalado o módulo Az PowerShell usando o pacote MSI, desinstale-o por meio do sistema do Windows, em vez de por meio do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5357-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="d5357-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d5357-109">Platform</span></span>         |                      <span data-ttu-id="d5357-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="d5357-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="d5357-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5357-111">Windows 10</span></span>               | <span data-ttu-id="d5357-112">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="d5357-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="d5357-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5357-113">Windows 7</span></span> </br><span data-ttu-id="d5357-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5357-114">Windows 8</span></span> | <span data-ttu-id="d5357-115">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="d5357-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d5357-116">Nessa tela, você deverá ver **Azure PowerShell** na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="d5357-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="d5357-117">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d5357-117">This is the app to uninstall.</span></span> <span data-ttu-id="d5357-118">Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.</span><span class="sxs-lookup"><span data-stu-id="d5357-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="d5357-119">Desinstalar o módulo Az PowerShell do PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d5357-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="d5357-120">Para desinstalar os módulos Az, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="d5357-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d5357-121">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="d5357-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d5357-122">Para remover completamente o módulo Az PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="d5357-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d5357-123">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5357-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d5357-124">Para verificar qual versão do módulo Az PowerShell foi instalada, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d5357-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="d5357-125">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="d5357-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d5357-126">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="d5357-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="d5357-127">Será necessário ter acesso de administrador para executar esse script em um escopo diferente de **Processo** ou **Usuário Atual**.</span><span class="sxs-lookup"><span data-stu-id="d5357-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="d5357-128">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5357-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d5357-129">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do módulo Az PowerShell e os respectivos submódulos.</span><span class="sxs-lookup"><span data-stu-id="d5357-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="d5357-130">À medida que o script for executado, ele exibirá o **Nome** , a **Versão** e o **Estado** de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d5357-130">As the script runs, it displays the **Name** , **Version** , and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="d5357-131">Para executar o script para ver apenas o que seria excluído, sem removê-lo, especifique o parâmetro `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="d5357-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="d5357-132">Se esse script não puder corresponder a uma dependência exata com a mesma versão a desinstalar, ele não desinstalará _nenhuma_ versão dessa dependência.</span><span class="sxs-lookup"><span data-stu-id="d5357-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="d5357-133">Isso ocorre porque pode haver outras versões do módulo de destino no sistema que contam com essas dependências.</span><span class="sxs-lookup"><span data-stu-id="d5357-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="d5357-134">Execute o exemplo a seguir para cada versão do módulo Az PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="d5357-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="d5357-135">Para sua conveniência, o script a seguir desinstala todas as versões do Az **exceto** a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="d5357-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="d5357-136">Desinstalar o módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="d5357-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="d5357-137">Caso você tenha instalado o módulo Az no seu sistema e queira desinstalar o AzureRM, há duas opções.</span><span class="sxs-lookup"><span data-stu-id="d5357-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="d5357-138">Qual método você segue depende de como instalou o módulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d5357-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="d5357-139">Caso não tenha certeza do método de instalação original, siga as etapas para desinstalar um MSI primeiro.</span><span class="sxs-lookup"><span data-stu-id="d5357-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="d5357-140">Desinstalar o módulo AzureRM PowerShell do MSI</span><span class="sxs-lookup"><span data-stu-id="d5357-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="d5357-141">Se você tiver instalado o módulo AzureRM PowerShell usando o pacote MSI, desinstale-o por meio do sistema do Windows, em vez de por meio do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5357-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="d5357-142">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d5357-142">Platform</span></span>         |                      <span data-ttu-id="d5357-143">Instruções</span><span class="sxs-lookup"><span data-stu-id="d5357-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="d5357-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5357-144">Windows 10</span></span>               | <span data-ttu-id="d5357-145">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="d5357-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="d5357-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5357-146">Windows 7</span></span> </br><span data-ttu-id="d5357-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5357-147">Windows 8</span></span> | <span data-ttu-id="d5357-148">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="d5357-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d5357-149">Nessa tela, você deverá ver o **Azure PowerShell** ou o **Microsoft Azure PowerShell – mês e ano** na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="d5357-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="d5357-150">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="d5357-150">This is the app to uninstall.</span></span> <span data-ttu-id="d5357-151">Se você não vir esse programa listado, então instalou por meio do PowerShellGet e deve seguir as próximas instruções.</span><span class="sxs-lookup"><span data-stu-id="d5357-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="d5357-152">Desinstalar o módulo AzureRM PowerShell do PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d5357-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="d5357-153">Se você instalou o AzureRM com o PowerShellGet, pode remover os módulos com o cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponível como parte do módulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="d5357-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="d5357-154">O exemplo a seguir remove _todos_ os módulos do AzureRM do seu computador.</span><span class="sxs-lookup"><span data-stu-id="d5357-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="d5357-155">Ele requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="d5357-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
