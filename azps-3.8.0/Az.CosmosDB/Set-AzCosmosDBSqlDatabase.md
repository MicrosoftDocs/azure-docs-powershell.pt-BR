---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940554"
---
# <span data-ttu-id="01bdc-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="01bdc-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="01bdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="01bdc-103">Cria um novo ou atualiza um banco de dados SQL do CosmosDB existente.</span><span class="sxs-lookup"><span data-stu-id="01bdc-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="01bdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01bdc-104">SYNTAX</span></span>

### <span data-ttu-id="01bdc-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="01bdc-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01bdc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01bdc-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bdc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="01bdc-108">O cmdlet **set-AzCosmosDBSqlDatabase** cria um novo ou atualiza um banco de dados SQL existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="01bdc-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="01bdc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="01bdc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01bdc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="01bdc-111">OS</span><span class="sxs-lookup"><span data-stu-id="01bdc-111">PARAMETERS</span></span>

### <span data-ttu-id="01bdc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01bdc-112">-AccountName</span></span>
<span data-ttu-id="01bdc-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="01bdc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01bdc-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01bdc-114">-Confirm</span></span>
<span data-ttu-id="01bdc-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01bdc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bdc-116">-DefaultProfile</span></span>
<span data-ttu-id="01bdc-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01bdc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01bdc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01bdc-118">-InputObject</span></span>
<span data-ttu-id="01bdc-119">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="01bdc-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="01bdc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="01bdc-120">-Name</span></span>
<span data-ttu-id="01bdc-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01bdc-121">Database name.</span></span>

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

### <span data-ttu-id="01bdc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01bdc-122">-ResourceGroupName</span></span>
<span data-ttu-id="01bdc-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01bdc-123">Name of resource group.</span></span>

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

### <span data-ttu-id="01bdc-124">-Throughput</span><span class="sxs-lookup"><span data-stu-id="01bdc-124">-Throughput</span></span>
<span data-ttu-id="01bdc-125">O throughput do banco de dados SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="01bdc-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="01bdc-126">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="01bdc-126">Default value is 400.</span></span>

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

### <span data-ttu-id="01bdc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01bdc-127">-WhatIf</span></span>
<span data-ttu-id="01bdc-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01bdc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01bdc-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01bdc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bdc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bdc-130">CommonParameters</span></span>
<span data-ttu-id="01bdc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bdc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bdc-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01bdc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bdc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01bdc-133">INPUTS</span></span>

### <span data-ttu-id="01bdc-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="01bdc-134">None</span></span>

## <span data-ttu-id="01bdc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01bdc-135">OUTPUTS</span></span>

### <span data-ttu-id="01bdc-136">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01bdc-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="01bdc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01bdc-137">NOTES</span></span>

## <span data-ttu-id="01bdc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01bdc-138">RELATED LINKS</span></span>
