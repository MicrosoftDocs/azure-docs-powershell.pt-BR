---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281371"
---
# <span data-ttu-id="8484d-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="8484d-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="8484d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8484d-102">SYNOPSIS</span></span>
<span data-ttu-id="8484d-103">Obtém uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8484d-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="8484d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8484d-104">SYNTAX</span></span>

### <span data-ttu-id="8484d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8484d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8484d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8484d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8484d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8484d-107">DESCRIPTION</span></span>
<span data-ttu-id="8484d-108">O cmdlet **Get-AzCosmosDBTable** Obtém uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="8484d-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="8484d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8484d-109">EXAMPLES</span></span>

### <span data-ttu-id="8484d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8484d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="8484d-111">Objeto Resource contém as propriedades _rid, _ts, _ ETag da tabela.</span><span class="sxs-lookup"><span data-stu-id="8484d-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="8484d-112">OS</span><span class="sxs-lookup"><span data-stu-id="8484d-112">PARAMETERS</span></span>

### <span data-ttu-id="8484d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8484d-113">-AccountName</span></span>
<span data-ttu-id="8484d-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="8484d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8484d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8484d-115">-DefaultProfile</span></span>
<span data-ttu-id="8484d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8484d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8484d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8484d-117">-Name</span></span>
<span data-ttu-id="8484d-118">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="8484d-118">Name of the Table.</span></span>

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

### <span data-ttu-id="8484d-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8484d-119">-ParentObject</span></span>
<span data-ttu-id="8484d-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8484d-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8484d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8484d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8484d-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8484d-122">Name of resource group.</span></span>

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

### <span data-ttu-id="8484d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8484d-123">CommonParameters</span></span>
<span data-ttu-id="8484d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8484d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8484d-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8484d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8484d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8484d-126">INPUTS</span></span>

### <span data-ttu-id="8484d-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8484d-127">None</span></span>

## <span data-ttu-id="8484d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8484d-128">OUTPUTS</span></span>

### <span data-ttu-id="8484d-129">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8484d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="8484d-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8484d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8484d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8484d-131">NOTES</span></span>

## <span data-ttu-id="8484d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8484d-132">RELATED LINKS</span></span>
