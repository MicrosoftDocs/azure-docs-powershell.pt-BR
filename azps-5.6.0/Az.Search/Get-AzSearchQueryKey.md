---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890072"
---
# <span data-ttu-id="e9a4b-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e9a4b-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="e9a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a4b-103">Obtém as teclas de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e9a4b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e9a4b-104">SYNTAX</span></span>

### <span data-ttu-id="e9a4b-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9a4b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9a4b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9a4b-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9a4b-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9a4b-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9a4b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e9a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="e9a4b-109">O cmdlet **Get-AzSearchQueryKey** obtém as teclas de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e9a4b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="e9a4b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9a4b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="e9a4b-112">O exemplo obtém todas as teclas de consulta do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e9a4b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-113">PARAMETERS</span></span>

### <span data-ttu-id="e9a4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a4b-114">-DefaultProfile</span></span>
<span data-ttu-id="e9a4b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a4b-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e9a4b-116">-ParentObject</span></span>
<span data-ttu-id="e9a4b-117">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="e9a4b-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e9a4b-118">-ParentResourceId</span></span>
<span data-ttu-id="e9a4b-119">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e9a4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9a4b-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-121">Resource Group name.</span></span>

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

### <span data-ttu-id="e9a4b-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e9a4b-122">-ServiceName</span></span>
<span data-ttu-id="e9a4b-123">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="e9a4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a4b-124">CommonParameters</span></span>
<span data-ttu-id="e9a4b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a4b-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9a4b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a4b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-127">INPUTS</span></span>

### <span data-ttu-id="e9a4b-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e9a4b-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e9a4b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a4b-129">System.String</span></span>

## <span data-ttu-id="e9a4b-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-130">OUTPUTS</span></span>

### <span data-ttu-id="e9a4b-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e9a4b-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="e9a4b-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="e9a4b-132">NOTES</span></span>

## <span data-ttu-id="e9a4b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9a4b-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9a4b-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e9a4b-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="e9a4b-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e9a4b-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)