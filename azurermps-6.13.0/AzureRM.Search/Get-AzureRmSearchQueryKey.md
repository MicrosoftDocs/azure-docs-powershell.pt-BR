---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428349"
---
# <span data-ttu-id="8509a-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8509a-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="8509a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8509a-102">SYNOPSIS</span></span>
<span data-ttu-id="8509a-103">Obtém a (s) chave (s) de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8509a-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8509a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8509a-104">SYNTAX</span></span>

### <span data-ttu-id="8509a-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8509a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8509a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8509a-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8509a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8509a-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8509a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8509a-108">DESCRIPTION</span></span>
<span data-ttu-id="8509a-109">O cmdlet **Get-AzureRmSearchQueryKey** Obtém a (s) chave (s) de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8509a-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="8509a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8509a-110">EXAMPLES</span></span>

### <span data-ttu-id="8509a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8509a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="8509a-112">O exemplo obtém todas as chaves de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="8509a-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="8509a-113">OS</span><span class="sxs-lookup"><span data-stu-id="8509a-113">PARAMETERS</span></span>

### <span data-ttu-id="8509a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8509a-114">-DefaultProfile</span></span>
<span data-ttu-id="8509a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8509a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8509a-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8509a-116">-ParentObject</span></span>
<span data-ttu-id="8509a-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8509a-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8509a-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8509a-118">-ParentResourceId</span></span>
<span data-ttu-id="8509a-119">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8509a-119">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8509a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8509a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8509a-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8509a-121">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8509a-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8509a-122">-ServiceName</span></span>
<span data-ttu-id="8509a-123">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8509a-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8509a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8509a-124">CommonParameters</span></span>
<span data-ttu-id="8509a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8509a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8509a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8509a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8509a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8509a-127">INPUTS</span></span>

### <span data-ttu-id="8509a-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8509a-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="8509a-129">Parâmetros: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8509a-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="8509a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8509a-130">System.String</span></span>

## <span data-ttu-id="8509a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8509a-131">OUTPUTS</span></span>

### <span data-ttu-id="8509a-132">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8509a-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="8509a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8509a-133">NOTES</span></span>

## <span data-ttu-id="8509a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8509a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8509a-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8509a-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="8509a-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8509a-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
