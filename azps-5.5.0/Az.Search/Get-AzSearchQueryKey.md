---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 1c5845b0273d47f1aa1a18782a9243bc5ee5ca9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118724"
---
# <span data-ttu-id="042eb-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="042eb-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="042eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="042eb-102">SYNOPSIS</span></span>
<span data-ttu-id="042eb-103">Obtém as teclas de consulta do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="042eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="042eb-104">SYNTAX</span></span>

### <span data-ttu-id="042eb-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="042eb-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042eb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="042eb-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="042eb-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="042eb-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="042eb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="042eb-108">DESCRIPTION</span></span>
<span data-ttu-id="042eb-109">O cmdlet **Get-AzSearchQueryKey** obtém as teclas de consulta do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="042eb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="042eb-110">EXAMPLES</span></span>

### <span data-ttu-id="042eb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="042eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="042eb-112">O exemplo obtém todas as teclas de consulta do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="042eb-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="042eb-113">PARAMETERS</span></span>

### <span data-ttu-id="042eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042eb-114">-DefaultProfile</span></span>
<span data-ttu-id="042eb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="042eb-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="042eb-116">-ParentObject</span></span>
<span data-ttu-id="042eb-117">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="042eb-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="042eb-118">-ParentResourceId</span></span>
<span data-ttu-id="042eb-119">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="042eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="042eb-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="042eb-121">Resource Group name.</span></span>

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

### <span data-ttu-id="042eb-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="042eb-122">-ServiceName</span></span>
<span data-ttu-id="042eb-123">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="042eb-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="042eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042eb-124">CommonParameters</span></span>
<span data-ttu-id="042eb-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042eb-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="042eb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042eb-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="042eb-127">INPUTS</span></span>

### <span data-ttu-id="042eb-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="042eb-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="042eb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="042eb-129">System.String</span></span>

## <span data-ttu-id="042eb-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="042eb-130">OUTPUTS</span></span>

### <span data-ttu-id="042eb-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="042eb-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="042eb-132">Notas</span><span class="sxs-lookup"><span data-stu-id="042eb-132">NOTES</span></span>

## <span data-ttu-id="042eb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="042eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="042eb-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="042eb-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="042eb-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="042eb-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)