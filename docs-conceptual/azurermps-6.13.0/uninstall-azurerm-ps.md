---
title: Desinstalar o Azure PowerShell
description: Como desinstalar completamente o Azure PowerShell
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 58d861f09eef04638cfa7e784ef0e28e9f4751d4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244255"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="b496c-103">Desinstalar o módulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b496c-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="b496c-104">Este artigo informa como desinstalar uma versão mais antiga do Azure PowerShell ou removê-la completamente do sistema.</span><span class="sxs-lookup"><span data-stu-id="b496c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="b496c-105">Se você decidiu desinstalar completamente o Azure PowerShell, envie-nos seus comentários por meio do cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="b496c-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="b496c-106">Se você encontrar um bug, agradeceríamos se [registrasse um problema do GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="b496c-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="b496c-107">Desinstale o MSI do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b496c-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="b496c-108">Se você instalou o Azure PowerShell usando o pacote MSI, desinstale por meio do sistema do Windows, em vez do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b496c-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="b496c-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="b496c-109">Platform</span></span> | <span data-ttu-id="b496c-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="b496c-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="b496c-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b496c-111">Windows 10</span></span> | <span data-ttu-id="b496c-112">Iniciar > Configurações > Aplicativos</span><span class="sxs-lookup"><span data-stu-id="b496c-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="b496c-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b496c-113">Windows 7</span></span> </br><span data-ttu-id="b496c-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b496c-114">Windows 8</span></span> | <span data-ttu-id="b496c-115">Iniciar > Painel de Controle > Programas > Desinstalar um programa</span><span class="sxs-lookup"><span data-stu-id="b496c-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="b496c-116">Nessa tela, você deverá ver __Azure PowerShell__ na lista de programas.</span><span class="sxs-lookup"><span data-stu-id="b496c-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="b496c-117">Esse é o aplicativo a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b496c-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="b496c-118">Desinstalar pelo PowerShell</span><span class="sxs-lookup"><span data-stu-id="b496c-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="b496c-119">Se você instalou o Azure PowerShell usando o PowerShellGet, use o cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="b496c-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="b496c-120">No entanto, `Uninstall-Module` desinstala apenas um módulo.</span><span class="sxs-lookup"><span data-stu-id="b496c-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="b496c-121">Para remover completamente o Azure PowerShell, desinstale cada módulo individualmente.</span><span class="sxs-lookup"><span data-stu-id="b496c-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="b496c-122">A desinstalação poderá ser complicada se você tiver mais de uma versão instalada do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b496c-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="b496c-123">Para verificar qual versão do Azure PowerShell foi instalada, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b496c-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="b496c-124">O script a seguir consulta a Galeria do PowerShell para obter uma lista de submódulos dependentes.</span><span class="sxs-lookup"><span data-stu-id="b496c-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="b496c-125">Em seguida, o script desinstala a versão correta de cada submódulo.</span><span class="sxs-lookup"><span data-stu-id="b496c-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="b496c-126">Você precisará ter acesso de administrador para executar esse script em um escopo diferente de `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="b496c-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="b496c-127">Para usar essa função, copie e cole o código em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b496c-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="b496c-128">O exemplo a seguir mostra como executar a função para remover uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b496c-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="b496c-129">À medida que o script for executado, ele exibirá o nome e a versão de cada submódulo que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b496c-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="b496c-130">Para executar o script para ver apenas o que seria excluído, sem removê-lo, use a opção `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="b496c-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="b496c-131">Se esse script não puder corresponder a uma dependência exata com a mesma versão a desinstalar, ele não desinstalará _nenhuma_ versão dessa dependência.</span><span class="sxs-lookup"><span data-stu-id="b496c-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="b496c-132">Isso ocorre porque pode haver outras versões do módulo de destino no sistema que contam com essas dependências.</span><span class="sxs-lookup"><span data-stu-id="b496c-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="b496c-133">Nesse caso, as versões disponíveis da dependência são listadas.</span><span class="sxs-lookup"><span data-stu-id="b496c-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="b496c-134">Então, você poderá remover qualquer uma das versões antigas manualmente com o `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="b496c-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="b496c-135">Execute o comando para cada versão do Azure PowerShell que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="b496c-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="b496c-136">Para sua conveniência, o script a seguir irá desinstalar todas as versões do AzureRM __exceto__ a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="b496c-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
