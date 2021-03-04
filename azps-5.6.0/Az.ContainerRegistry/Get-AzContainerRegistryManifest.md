---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892204"
---
# <span data-ttu-id="768d7-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="768d7-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="768d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="768d7-102">SYNOPSIS</span></span>
<span data-ttu-id="768d7-103">Obter ou listar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="768d7-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="768d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="768d7-104">SYNTAX</span></span>

### <span data-ttu-id="768d7-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="768d7-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="768d7-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="768d7-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="768d7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="768d7-107">DESCRIPTION</span></span>
<span data-ttu-id="768d7-108">Obter ou listar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="768d7-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="768d7-109">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="768d7-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="768d7-110">primeiro.</span><span class="sxs-lookup"><span data-stu-id="768d7-110">first.</span></span>

## <span data-ttu-id="768d7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="768d7-111">EXAMPLES</span></span>

### <span data-ttu-id="768d7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="768d7-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="768d7-113">Listar manifestos para o repositório alpino no Registro.</span><span class="sxs-lookup"><span data-stu-id="768d7-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="768d7-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="768d7-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="768d7-115">Obter manifestos sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="768d7-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="768d7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="768d7-116">PARAMETERS</span></span>

### <span data-ttu-id="768d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768d7-117">-DefaultProfile</span></span>
<span data-ttu-id="768d7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="768d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="768d7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="768d7-119">-Name</span></span>
<span data-ttu-id="768d7-120">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="768d7-120">Manifest reference.</span></span>

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

### <span data-ttu-id="768d7-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="768d7-121">-RegistryName</span></span>
<span data-ttu-id="768d7-122">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="768d7-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="768d7-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="768d7-123">-RepositoryName</span></span>
<span data-ttu-id="768d7-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="768d7-124">Repository Name.</span></span>

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

### <span data-ttu-id="768d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768d7-125">CommonParameters</span></span>
<span data-ttu-id="768d7-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="768d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768d7-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="768d7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768d7-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="768d7-128">INPUTS</span></span>

### <span data-ttu-id="768d7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="768d7-129">System.String</span></span>

## <span data-ttu-id="768d7-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="768d7-130">OUTPUTS</span></span>

### <span data-ttu-id="768d7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="768d7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="768d7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="768d7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="768d7-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="768d7-133">NOTES</span></span>

## <span data-ttu-id="768d7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="768d7-134">RELATED LINKS</span></span>
