---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890288"
---
# <span data-ttu-id="ad69e-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="ad69e-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="ad69e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad69e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad69e-103">Obter ou listar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="ad69e-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="ad69e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad69e-104">SYNTAX</span></span>

### <span data-ttu-id="ad69e-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad69e-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad69e-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad69e-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad69e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad69e-107">DESCRIPTION</span></span>
<span data-ttu-id="ad69e-108">Obter ou listar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="ad69e-108">Get or list ACR tag.</span></span>
<span data-ttu-id="ad69e-109">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="ad69e-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="ad69e-110">primeiro.</span><span class="sxs-lookup"><span data-stu-id="ad69e-110">first.</span></span>

## <span data-ttu-id="ad69e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad69e-111">EXAMPLES</span></span>

### <span data-ttu-id="ad69e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ad69e-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="ad69e-113">Listar marcas para o repositório alpino no Registro.</span><span class="sxs-lookup"><span data-stu-id="ad69e-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="ad69e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ad69e-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="ad69e-115">Obter a marca mais recente para o repositório alpino no Registro.</span><span class="sxs-lookup"><span data-stu-id="ad69e-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="ad69e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad69e-116">PARAMETERS</span></span>

### <span data-ttu-id="ad69e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad69e-117">-DefaultProfile</span></span>
<span data-ttu-id="ad69e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad69e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad69e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ad69e-119">-Name</span></span>
<span data-ttu-id="ad69e-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="ad69e-120">Tag.</span></span>

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

### <span data-ttu-id="ad69e-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ad69e-121">-RegistryName</span></span>
<span data-ttu-id="ad69e-122">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad69e-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="ad69e-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ad69e-123">-RepositoryName</span></span>
<span data-ttu-id="ad69e-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="ad69e-124">Repository Name.</span></span>

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

### <span data-ttu-id="ad69e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad69e-125">CommonParameters</span></span>
<span data-ttu-id="ad69e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad69e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad69e-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad69e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad69e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad69e-128">INPUTS</span></span>

### <span data-ttu-id="ad69e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ad69e-129">System.String</span></span>

## <span data-ttu-id="ad69e-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad69e-130">OUTPUTS</span></span>

### <span data-ttu-id="ad69e-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="ad69e-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="ad69e-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="ad69e-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="ad69e-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad69e-133">NOTES</span></span>

## <span data-ttu-id="ad69e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad69e-134">RELATED LINKS</span></span>
