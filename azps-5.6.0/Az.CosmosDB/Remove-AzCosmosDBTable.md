---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ff294af7e4305facd3265d96151c97b82ff9c052
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892996"
---
# <span data-ttu-id="3107f-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="3107f-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="3107f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3107f-102">SYNOPSIS</span></span>
<span data-ttu-id="3107f-103">Exclui a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3107f-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="3107f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3107f-104">SYNTAX</span></span>

### <span data-ttu-id="3107f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3107f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3107f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3107f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3107f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3107f-107">DESCRIPTION</span></span>
<span data-ttu-id="3107f-108">O cmdlet **Remove-AzCosmosDBTable** exclui a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3107f-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="3107f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3107f-109">EXAMPLES</span></span>

### <span data-ttu-id="3107f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3107f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="3107f-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é true, se a exclusão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3107f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="3107f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3107f-112">PARAMETERS</span></span>

### <span data-ttu-id="3107f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3107f-113">-AccountName</span></span>
<span data-ttu-id="3107f-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="3107f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3107f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3107f-115">-Confirm</span></span>
<span data-ttu-id="3107f-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3107f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3107f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3107f-117">-DefaultProfile</span></span>
<span data-ttu-id="3107f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3107f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3107f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3107f-119">-InputObject</span></span>
<span data-ttu-id="3107f-120">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="3107f-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3107f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3107f-121">-Name</span></span>
<span data-ttu-id="3107f-122">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="3107f-122">Name of the Table.</span></span>

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

### <span data-ttu-id="3107f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3107f-123">-PassThru</span></span>
<span data-ttu-id="3107f-124">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="3107f-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3107f-125">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="3107f-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3107f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3107f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3107f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3107f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="3107f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3107f-128">-WhatIf</span></span>
<span data-ttu-id="3107f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3107f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3107f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3107f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3107f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3107f-131">CommonParameters</span></span>
<span data-ttu-id="3107f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3107f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3107f-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3107f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3107f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3107f-134">INPUTS</span></span>

### <span data-ttu-id="3107f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="3107f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="3107f-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3107f-136">OUTPUTS</span></span>

### <span data-ttu-id="3107f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="3107f-137">System.Void</span></span>

### <span data-ttu-id="3107f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3107f-138">System.Boolean</span></span>

## <span data-ttu-id="3107f-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="3107f-139">NOTES</span></span>

## <span data-ttu-id="3107f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3107f-140">RELATED LINKS</span></span>
