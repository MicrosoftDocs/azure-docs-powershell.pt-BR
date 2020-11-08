---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125093"
---
# <span data-ttu-id="090dc-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="090dc-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="090dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="090dc-102">SYNOPSIS</span></span>
<span data-ttu-id="090dc-103">Obtém a (s) chave (s) de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="090dc-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="090dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="090dc-104">SYNTAX</span></span>

### <span data-ttu-id="090dc-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="090dc-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="090dc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="090dc-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="090dc-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="090dc-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="090dc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="090dc-108">DESCRIPTION</span></span>
<span data-ttu-id="090dc-109">O cmdlet **Get-AzSearchQueryKey** Obtém a (s) chave (s) de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="090dc-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="090dc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="090dc-110">EXAMPLES</span></span>

### <span data-ttu-id="090dc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="090dc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="090dc-112">O exemplo obtém todas as chaves de consulta do serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="090dc-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="090dc-113">OS</span><span class="sxs-lookup"><span data-stu-id="090dc-113">PARAMETERS</span></span>

### <span data-ttu-id="090dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090dc-114">-DefaultProfile</span></span>
<span data-ttu-id="090dc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="090dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="090dc-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="090dc-116">-ParentObject</span></span>
<span data-ttu-id="090dc-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="090dc-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="090dc-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="090dc-118">-ParentResourceId</span></span>
<span data-ttu-id="090dc-119">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="090dc-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="090dc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="090dc-120">-ResourceGroupName</span></span>
<span data-ttu-id="090dc-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="090dc-121">Resource Group name.</span></span>

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

### <span data-ttu-id="090dc-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="090dc-122">-ServiceName</span></span>
<span data-ttu-id="090dc-123">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="090dc-123">Search Service name.</span></span>

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

### <span data-ttu-id="090dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090dc-124">CommonParameters</span></span>
<span data-ttu-id="090dc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="090dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090dc-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090dc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090dc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="090dc-127">INPUTS</span></span>

### <span data-ttu-id="090dc-128">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="090dc-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="090dc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="090dc-129">System.String</span></span>

## <span data-ttu-id="090dc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="090dc-130">OUTPUTS</span></span>

### <span data-ttu-id="090dc-131">Microsoft. Azure. Commands. Management. Search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="090dc-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="090dc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="090dc-132">NOTES</span></span>

## <span data-ttu-id="090dc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="090dc-133">RELATED LINKS</span></span>

[<span data-ttu-id="090dc-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="090dc-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="090dc-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="090dc-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)