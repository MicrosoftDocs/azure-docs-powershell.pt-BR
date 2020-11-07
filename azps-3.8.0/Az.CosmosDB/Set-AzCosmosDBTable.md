---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942193"
---
# <span data-ttu-id="d5333-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="d5333-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="d5333-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5333-102">SYNOPSIS</span></span>
<span data-ttu-id="d5333-103">Define a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d5333-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="d5333-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5333-104">SYNTAX</span></span>

### <span data-ttu-id="d5333-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5333-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5333-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5333-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5333-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5333-107">DESCRIPTION</span></span>
<span data-ttu-id="d5333-108">O cmdlet **set-AzCosmosDBTable** cria uma nova tabela ou atualiza uma tabela existente, substituindo toda a tabela existente.</span><span class="sxs-lookup"><span data-stu-id="d5333-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="d5333-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5333-109">EXAMPLES</span></span>

### <span data-ttu-id="d5333-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5333-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="d5333-111">Objeto Resource contém as propriedades _rid, _ts, _ ETag da tabela.</span><span class="sxs-lookup"><span data-stu-id="d5333-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="d5333-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5333-112">PARAMETERS</span></span>

### <span data-ttu-id="d5333-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5333-113">-AccountName</span></span>
<span data-ttu-id="d5333-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="d5333-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d5333-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5333-115">-Confirm</span></span>
<span data-ttu-id="d5333-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5333-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5333-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5333-117">-DefaultProfile</span></span>
<span data-ttu-id="d5333-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5333-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5333-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5333-119">-InputObject</span></span>
<span data-ttu-id="d5333-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d5333-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5333-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5333-121">-Name</span></span>
<span data-ttu-id="d5333-122">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="d5333-122">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5333-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5333-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5333-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5333-124">Name of resource group.</span></span>

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

### <span data-ttu-id="d5333-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d5333-125">-Throughput</span></span>
<span data-ttu-id="d5333-126">A taxa de transferência da tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d5333-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="d5333-127">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="d5333-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5333-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5333-128">-WhatIf</span></span>
<span data-ttu-id="d5333-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5333-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5333-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5333-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5333-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5333-131">CommonParameters</span></span>
<span data-ttu-id="d5333-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5333-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5333-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5333-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5333-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5333-134">INPUTS</span></span>

### <span data-ttu-id="d5333-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d5333-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d5333-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5333-136">OUTPUTS</span></span>

### <span data-ttu-id="d5333-137">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d5333-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d5333-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5333-138">NOTES</span></span>

## <span data-ttu-id="d5333-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5333-139">RELATED LINKS</span></span>
