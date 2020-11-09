---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281264"
---
# <span data-ttu-id="f5ce1-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f5ce1-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f5ce1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ce1-103">Exclui o contêiner SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f5ce1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5ce1-104">SYNTAX</span></span>

### <span data-ttu-id="f5ce1-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5ce1-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5ce1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5ce1-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ce1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5ce1-107">DESCRIPTION</span></span>
<span data-ttu-id="f5ce1-108">O cmdlet **Remove-AzCosmosDBSqlContainer** exclui o contêiner SQL CosmosDB correspondente a um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="f5ce1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5ce1-109">EXAMPLES</span></span>

### <span data-ttu-id="f5ce1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5ce1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="f5ce1-111">OS</span><span class="sxs-lookup"><span data-stu-id="f5ce1-111">PARAMETERS</span></span>

### <span data-ttu-id="f5ce1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5ce1-112">-AccountName</span></span>
<span data-ttu-id="f5ce1-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5ce1-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5ce1-114">-Confirm</span></span>
<span data-ttu-id="f5ce1-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ce1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5ce1-116">-DatabaseName</span></span>
<span data-ttu-id="f5ce1-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-117">Database name.</span></span>

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

### <span data-ttu-id="f5ce1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ce1-118">-DefaultProfile</span></span>
<span data-ttu-id="f5ce1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ce1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ce1-120">-InputObject</span></span>
<span data-ttu-id="f5ce1-121">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ce1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5ce1-122">-Name</span></span>
<span data-ttu-id="f5ce1-123">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-123">Container name.</span></span>

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

### <span data-ttu-id="f5ce1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5ce1-124">-PassThru</span></span>
<span data-ttu-id="f5ce1-125">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f5ce1-126">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f5ce1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ce1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5ce1-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="f5ce1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ce1-129">-WhatIf</span></span>
<span data-ttu-id="f5ce1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ce1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ce1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ce1-132">CommonParameters</span></span>
<span data-ttu-id="f5ce1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ce1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ce1-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5ce1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ce1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5ce1-135">INPUTS</span></span>

### <span data-ttu-id="f5ce1-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5ce1-136">None</span></span>

## <span data-ttu-id="f5ce1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5ce1-137">OUTPUTS</span></span>

### <span data-ttu-id="f5ce1-138">System. void</span><span class="sxs-lookup"><span data-stu-id="f5ce1-138">System.Void</span></span>

### <span data-ttu-id="f5ce1-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5ce1-139">System.Boolean</span></span>

## <span data-ttu-id="f5ce1-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5ce1-140">NOTES</span></span>

## <span data-ttu-id="f5ce1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5ce1-141">RELATED LINKS</span></span>
