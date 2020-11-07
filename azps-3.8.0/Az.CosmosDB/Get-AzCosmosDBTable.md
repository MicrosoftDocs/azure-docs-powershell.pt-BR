---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944882"
---
# <span data-ttu-id="af243-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="af243-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="af243-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af243-102">SYNOPSIS</span></span>
<span data-ttu-id="af243-103">Obtém uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="af243-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="af243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af243-104">SYNTAX</span></span>

### <span data-ttu-id="af243-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af243-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af243-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af243-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af243-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af243-107">DESCRIPTION</span></span>
<span data-ttu-id="af243-108">O cmdlet **Get-AzCosmosDBTable** Obtém uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="af243-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="af243-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af243-109">EXAMPLES</span></span>

### <span data-ttu-id="af243-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af243-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="af243-111">Objeto Resource contém as propriedades _rid, _ts, _ ETag da tabela.</span><span class="sxs-lookup"><span data-stu-id="af243-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="af243-112">OS</span><span class="sxs-lookup"><span data-stu-id="af243-112">PARAMETERS</span></span>

### <span data-ttu-id="af243-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af243-113">-AccountName</span></span>
<span data-ttu-id="af243-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="af243-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af243-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af243-115">-DefaultProfile</span></span>
<span data-ttu-id="af243-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af243-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af243-117">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="af243-117">-Detailed</span></span>
<span data-ttu-id="af243-118">Se fornecido, o cmdlet retornará a tabela com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="af243-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af243-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af243-119">-InputObject</span></span>
<span data-ttu-id="af243-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="af243-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af243-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="af243-121">-Name</span></span>
<span data-ttu-id="af243-122">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="af243-122">Name of the Table.</span></span>

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

### <span data-ttu-id="af243-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af243-123">-ResourceGroupName</span></span>
<span data-ttu-id="af243-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af243-124">Name of resource group.</span></span>

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

### <span data-ttu-id="af243-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af243-125">CommonParameters</span></span>
<span data-ttu-id="af243-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af243-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af243-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af243-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af243-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af243-128">INPUTS</span></span>

### <span data-ttu-id="af243-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af243-129">None</span></span>

## <span data-ttu-id="af243-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af243-130">OUTPUTS</span></span>

### <span data-ttu-id="af243-131">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="af243-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="af243-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="af243-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="af243-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af243-133">NOTES</span></span>

## <span data-ttu-id="af243-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af243-134">RELATED LINKS</span></span>
