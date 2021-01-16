---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262190"
---
# <span data-ttu-id="a38b5-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="a38b5-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="a38b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a38b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a38b5-103">Exclui a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a38b5-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="a38b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a38b5-104">SYNTAX</span></span>

### <span data-ttu-id="a38b5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a38b5-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a38b5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a38b5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a38b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a38b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a38b5-108">O cmdlet **Remove-AzCosmosDBTable** exclui a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a38b5-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="a38b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a38b5-109">EXAMPLES</span></span>

### <span data-ttu-id="a38b5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a38b5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="a38b5-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a38b5-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="a38b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="a38b5-112">PARAMETERS</span></span>

### <span data-ttu-id="a38b5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a38b5-113">-AccountName</span></span>
<span data-ttu-id="a38b5-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a38b5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a38b5-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a38b5-115">-Confirm</span></span>
<span data-ttu-id="a38b5-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a38b5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a38b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38b5-117">-DefaultProfile</span></span>
<span data-ttu-id="a38b5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a38b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a38b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a38b5-119">-InputObject</span></span>
<span data-ttu-id="a38b5-120">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a38b5-120">Sql Database object.</span></span>

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

### <span data-ttu-id="a38b5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a38b5-121">-Name</span></span>
<span data-ttu-id="a38b5-122">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="a38b5-122">Name of the Table.</span></span>

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

### <span data-ttu-id="a38b5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a38b5-123">-PassThru</span></span>
<span data-ttu-id="a38b5-124">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="a38b5-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a38b5-125">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="a38b5-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a38b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="a38b5-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a38b5-127">Name of resource group.</span></span>

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

### <span data-ttu-id="a38b5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a38b5-128">-WhatIf</span></span>
<span data-ttu-id="a38b5-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a38b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a38b5-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a38b5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a38b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38b5-131">CommonParameters</span></span>
<span data-ttu-id="a38b5-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38b5-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a38b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38b5-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a38b5-134">INPUTS</span></span>

### <span data-ttu-id="a38b5-135">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a38b5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="a38b5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a38b5-136">OUTPUTS</span></span>

### <span data-ttu-id="a38b5-137">System. void</span><span class="sxs-lookup"><span data-stu-id="a38b5-137">System.Void</span></span>

### <span data-ttu-id="a38b5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a38b5-138">System.Boolean</span></span>

## <span data-ttu-id="a38b5-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a38b5-139">NOTES</span></span>

## <span data-ttu-id="a38b5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a38b5-140">RELATED LINKS</span></span>
