---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117772"
---
# <span data-ttu-id="96a49-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="96a49-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="96a49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96a49-102">SYNOPSIS</span></span>
<span data-ttu-id="96a49-103">Exclui a Tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96a49-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="96a49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96a49-104">SYNTAX</span></span>

### <span data-ttu-id="96a49-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a49-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a49-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a49-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a49-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96a49-107">DESCRIPTION</span></span>
<span data-ttu-id="96a49-108">O cmdlet **Remove-AzCosmosDBTable** exclui a Tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96a49-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="96a49-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96a49-109">EXAMPLES</span></span>

### <span data-ttu-id="96a49-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96a49-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="96a49-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="96a49-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="96a49-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96a49-112">PARAMETERS</span></span>

### <span data-ttu-id="96a49-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="96a49-113">-AccountName</span></span>
<span data-ttu-id="96a49-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="96a49-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="96a49-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96a49-115">-Confirm</span></span>
<span data-ttu-id="96a49-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a49-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a49-117">-DefaultProfile</span></span>
<span data-ttu-id="96a49-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96a49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a49-119">-InputObject</span></span>
<span data-ttu-id="96a49-120">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="96a49-120">Sql Database object.</span></span>

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

### <span data-ttu-id="96a49-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="96a49-121">-Name</span></span>
<span data-ttu-id="96a49-122">Nome da Tabela.</span><span class="sxs-lookup"><span data-stu-id="96a49-122">Name of the Table.</span></span>

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

### <span data-ttu-id="96a49-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96a49-123">-PassThru</span></span>
<span data-ttu-id="96a49-124">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="96a49-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="96a49-125">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="96a49-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="96a49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a49-126">-ResourceGroupName</span></span>
<span data-ttu-id="96a49-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96a49-127">Name of resource group.</span></span>

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

### <span data-ttu-id="96a49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a49-128">-WhatIf</span></span>
<span data-ttu-id="96a49-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96a49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a49-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a49-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a49-131">CommonParameters</span></span>
<span data-ttu-id="96a49-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a49-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a49-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96a49-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a49-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="96a49-134">INPUTS</span></span>

### <span data-ttu-id="96a49-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="96a49-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="96a49-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="96a49-136">OUTPUTS</span></span>

### <span data-ttu-id="96a49-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="96a49-137">System.Void</span></span>

### <span data-ttu-id="96a49-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96a49-138">System.Boolean</span></span>

## <span data-ttu-id="96a49-139">Notas</span><span class="sxs-lookup"><span data-stu-id="96a49-139">NOTES</span></span>

## <span data-ttu-id="96a49-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a49-140">RELATED LINKS</span></span>
