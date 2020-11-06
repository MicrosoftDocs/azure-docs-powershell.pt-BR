---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428345"
---
# <span data-ttu-id="a1fe4-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a1fe4-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="a1fe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fe4-103">Obtém um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1fe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1fe4-104">SYNTAX</span></span>

### <span data-ttu-id="a1fe4-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1fe4-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1fe4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1fe4-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1fe4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="a1fe4-108">O cmdlet **Get-AzureRmSearchService** Obtém o serviço de pesquisa do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="a1fe4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="a1fe4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1fe4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="a1fe4-111">Obter um serviço de pesquisa do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="a1fe4-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1fe4-112">PARAMETERS</span></span>

### <span data-ttu-id="a1fe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fe4-113">-DefaultProfile</span></span>
<span data-ttu-id="a1fe4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fe4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1fe4-115">-Name</span></span>
<span data-ttu-id="a1fe4-116">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fe4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1fe4-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1fe4-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fe4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1fe4-119">-ResourceId</span></span>
<span data-ttu-id="a1fe4-120">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-120">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1fe4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fe4-121">CommonParameters</span></span>
<span data-ttu-id="a1fe4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fe4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fe4-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1fe4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fe4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1fe4-124">INPUTS</span></span>

### <span data-ttu-id="a1fe4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a1fe4-125">System.String</span></span>

## <span data-ttu-id="a1fe4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1fe4-126">OUTPUTS</span></span>

### <span data-ttu-id="a1fe4-127">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a1fe4-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="a1fe4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1fe4-128">NOTES</span></span>

## <span data-ttu-id="a1fe4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1fe4-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1fe4-130">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a1fe4-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="a1fe4-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a1fe4-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="a1fe4-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="a1fe4-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
