---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116478"
---
# <span data-ttu-id="59854-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="59854-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="59854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59854-102">SYNOPSIS</span></span>
<span data-ttu-id="59854-103">Obtém o valor de produtividade da Tabela Desarmável.</span><span class="sxs-lookup"><span data-stu-id="59854-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="59854-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59854-104">SYNTAX</span></span>

### <span data-ttu-id="59854-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="59854-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59854-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59854-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59854-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="59854-107">DESCRIPTION</span></span>
<span data-ttu-id="59854-108">O cmdlet **Get-AzCosmosDBCasstableThroughput** obtém o objeto de produtividade correspondente a um determinado Espaço de Teclas.</span><span class="sxs-lookup"><span data-stu-id="59854-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="59854-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="59854-109">EXAMPLES</span></span>

### <span data-ttu-id="59854-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59854-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="59854-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59854-111">PARAMETERS</span></span>

### <span data-ttu-id="59854-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="59854-112">-AccountName</span></span>
<span data-ttu-id="59854-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="59854-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59854-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="59854-114">-Confirm</span></span>
<span data-ttu-id="59854-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59854-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59854-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59854-116">-DefaultProfile</span></span>
<span data-ttu-id="59854-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59854-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59854-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59854-118">-InputObject</span></span>
<span data-ttu-id="59854-119">Object Table Desarmado.</span><span class="sxs-lookup"><span data-stu-id="59854-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59854-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="59854-120">-KeyspaceName</span></span>
<span data-ttu-id="59854-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59854-121">Database name.</span></span>

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

### <span data-ttu-id="59854-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="59854-122">-Name</span></span>
<span data-ttu-id="59854-123">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="59854-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="59854-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59854-124">-ResourceGroupName</span></span>
<span data-ttu-id="59854-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59854-125">Name of resource group.</span></span>

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

### <span data-ttu-id="59854-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59854-126">-WhatIf</span></span>
<span data-ttu-id="59854-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="59854-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59854-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59854-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59854-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59854-129">CommonParameters</span></span>
<span data-ttu-id="59854-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59854-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59854-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59854-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59854-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="59854-132">INPUTS</span></span>

### <span data-ttu-id="59854-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="59854-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="59854-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="59854-134">OUTPUTS</span></span>

### <span data-ttu-id="59854-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="59854-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="59854-136">Notas</span><span class="sxs-lookup"><span data-stu-id="59854-136">NOTES</span></span>

## <span data-ttu-id="59854-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59854-137">RELATED LINKS</span></span>
