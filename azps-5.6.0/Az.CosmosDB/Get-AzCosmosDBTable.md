---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: c83e1d2edba5f34a4d8478ae97cee09b57f823ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889792"
---
# <span data-ttu-id="afaff-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="afaff-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="afaff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afaff-102">SYNOPSIS</span></span>
<span data-ttu-id="afaff-103">Obtém uma Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="afaff-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="afaff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="afaff-104">SYNTAX</span></span>

### <span data-ttu-id="afaff-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="afaff-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afaff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afaff-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afaff-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="afaff-107">DESCRIPTION</span></span>
<span data-ttu-id="afaff-108">O cmdlet **Get-AzCosmosDBTable** obtém um Table existente.</span><span class="sxs-lookup"><span data-stu-id="afaff-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="afaff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afaff-109">EXAMPLES</span></span>

### <span data-ttu-id="afaff-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afaff-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="afaff-111">O objeto Resource contém _rid, _ts, _ etag propriedades do Table.</span><span class="sxs-lookup"><span data-stu-id="afaff-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="afaff-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="afaff-112">PARAMETERS</span></span>

### <span data-ttu-id="afaff-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afaff-113">-AccountName</span></span>
<span data-ttu-id="afaff-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="afaff-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaff-115">-DefaultProfile</span></span>
<span data-ttu-id="afaff-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afaff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="afaff-117">-Name</span></span>
<span data-ttu-id="afaff-118">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="afaff-118">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaff-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="afaff-119">-ParentObject</span></span>
<span data-ttu-id="afaff-120">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="afaff-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afaff-121">-ResourceGroupName</span></span>
<span data-ttu-id="afaff-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="afaff-122">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afaff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaff-123">CommonParameters</span></span>
<span data-ttu-id="afaff-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaff-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afaff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaff-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afaff-126">INPUTS</span></span>

### <span data-ttu-id="afaff-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="afaff-127">None</span></span>

## <span data-ttu-id="afaff-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="afaff-128">OUTPUTS</span></span>

### <span data-ttu-id="afaff-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="afaff-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="afaff-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="afaff-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="afaff-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="afaff-131">NOTES</span></span>

## <span data-ttu-id="afaff-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afaff-132">RELATED LINKS</span></span>
