---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281262"
---
# <span data-ttu-id="f2d8f-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f2d8f-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f2d8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d8f-103">Exclui o banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f2d8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2d8f-104">SYNTAX</span></span>

### <span data-ttu-id="f2d8f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2d8f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d8f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2d8f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d8f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="f2d8f-108">O cmdlet **Remove-AzCosmosDBSqlDatabase** exclui o banco de dados SQL CosmosDB correspondente ao ResourceGroupName, AccountName e DatabaseName fornecido.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="f2d8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="f2d8f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2d8f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="f2d8f-111">OS</span><span class="sxs-lookup"><span data-stu-id="f2d8f-111">PARAMETERS</span></span>

### <span data-ttu-id="f2d8f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2d8f-112">-AccountName</span></span>
<span data-ttu-id="f2d8f-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f2d8f-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2d8f-114">-Confirm</span></span>
<span data-ttu-id="f2d8f-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d8f-116">-DefaultProfile</span></span>
<span data-ttu-id="f2d8f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2d8f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2d8f-118">-InputObject</span></span>
<span data-ttu-id="f2d8f-119">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d8f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2d8f-120">-Name</span></span>
<span data-ttu-id="f2d8f-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-121">Database name.</span></span>

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

### <span data-ttu-id="f2d8f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2d8f-122">-PassThru</span></span>
<span data-ttu-id="f2d8f-123">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f2d8f-124">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f2d8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2d8f-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f2d8f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d8f-127">-WhatIf</span></span>
<span data-ttu-id="f2d8f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2d8f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d8f-130">CommonParameters</span></span>
<span data-ttu-id="f2d8f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d8f-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2d8f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d8f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2d8f-133">INPUTS</span></span>

### <span data-ttu-id="f2d8f-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f2d8f-134">None</span></span>

## <span data-ttu-id="f2d8f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2d8f-135">OUTPUTS</span></span>

### <span data-ttu-id="f2d8f-136">System. void</span><span class="sxs-lookup"><span data-stu-id="f2d8f-136">System.Void</span></span>

### <span data-ttu-id="f2d8f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2d8f-137">System.Boolean</span></span>

## <span data-ttu-id="f2d8f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2d8f-138">NOTES</span></span>

## <span data-ttu-id="f2d8f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2d8f-139">RELATED LINKS</span></span>
