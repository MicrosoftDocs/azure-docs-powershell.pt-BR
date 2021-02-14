---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 2fa58235c0ba18042fde13ce9f8d3fb396940d07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115946"
---
# <span data-ttu-id="32844-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="32844-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="32844-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32844-102">SYNOPSIS</span></span>
<span data-ttu-id="32844-103">Obter ou listar manifesto de ACR.</span><span class="sxs-lookup"><span data-stu-id="32844-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="32844-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32844-104">SYNTAX</span></span>

### <span data-ttu-id="32844-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32844-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32844-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="32844-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32844-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="32844-107">DESCRIPTION</span></span>
<span data-ttu-id="32844-108">Obter ou listar manifesto de ACR.</span><span class="sxs-lookup"><span data-stu-id="32844-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="32844-109">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="32844-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="32844-110">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="32844-110">first.</span></span>

## <span data-ttu-id="32844-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32844-111">EXAMPLES</span></span>

### <span data-ttu-id="32844-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32844-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="32844-113">Manifestos de lista para o alpino do repositório sob o Registro.</span><span class="sxs-lookup"><span data-stu-id="32844-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="32844-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="32844-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="32844-115">Receba manifestos sha256:a5426f084c755f4d6c1d1d1562a2d456aaa574a24a61706f6806415627360c06ac0 para repositório alpine em registro.</span><span class="sxs-lookup"><span data-stu-id="32844-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="32844-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32844-116">PARAMETERS</span></span>

### <span data-ttu-id="32844-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32844-117">-DefaultProfile</span></span>
<span data-ttu-id="32844-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32844-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32844-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="32844-119">-Name</span></span>
<span data-ttu-id="32844-120">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="32844-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32844-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="32844-121">-RegistryName</span></span>
<span data-ttu-id="32844-122">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="32844-122">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32844-123">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="32844-123">-RepositoryName</span></span>
<span data-ttu-id="32844-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="32844-124">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32844-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32844-125">CommonParameters</span></span>
<span data-ttu-id="32844-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32844-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32844-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32844-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32844-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="32844-128">INPUTS</span></span>

### <span data-ttu-id="32844-129">System.String</span><span class="sxs-lookup"><span data-stu-id="32844-129">System.String</span></span>

## <span data-ttu-id="32844-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="32844-130">OUTPUTS</span></span>

### <span data-ttu-id="32844-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="32844-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="32844-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="32844-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="32844-133">Notas</span><span class="sxs-lookup"><span data-stu-id="32844-133">NOTES</span></span>

## <span data-ttu-id="32844-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32844-134">RELATED LINKS</span></span>
