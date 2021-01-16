---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434027"
---
# <span data-ttu-id="a1888-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="a1888-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="a1888-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1888-102">SYNOPSIS</span></span>
<span data-ttu-id="a1888-103">Exclui a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a1888-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="a1888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1888-104">SYNTAX</span></span>

### <span data-ttu-id="a1888-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1888-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1888-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1888-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1888-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1888-107">DESCRIPTION</span></span>
<span data-ttu-id="a1888-108">O cmdlet **Remove-AzCosmosDBTable** exclui a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a1888-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="a1888-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1888-109">EXAMPLES</span></span>

### <span data-ttu-id="a1888-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1888-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="a1888-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a1888-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="a1888-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1888-112">PARAMETERS</span></span>

### <span data-ttu-id="a1888-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a1888-113">-AccountName</span></span>
<span data-ttu-id="a1888-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a1888-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a1888-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1888-115">-Confirm</span></span>
<span data-ttu-id="a1888-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1888-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1888-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1888-117">-DefaultProfile</span></span>
<span data-ttu-id="a1888-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1888-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1888-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1888-119">-InputObject</span></span>
<span data-ttu-id="a1888-120">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a1888-120">Sql Database object.</span></span>

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

### <span data-ttu-id="a1888-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1888-121">-Name</span></span>
<span data-ttu-id="a1888-122">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="a1888-122">Name of the Table.</span></span>

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

### <span data-ttu-id="a1888-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1888-123">-PassThru</span></span>
<span data-ttu-id="a1888-124">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="a1888-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a1888-125">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="a1888-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a1888-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1888-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1888-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1888-127">Name of resource group.</span></span>

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

### <span data-ttu-id="a1888-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1888-128">-WhatIf</span></span>
<span data-ttu-id="a1888-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1888-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1888-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1888-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1888-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1888-131">CommonParameters</span></span>
<span data-ttu-id="a1888-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1888-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1888-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1888-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1888-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1888-134">INPUTS</span></span>

### <span data-ttu-id="a1888-135">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a1888-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="a1888-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1888-136">OUTPUTS</span></span>

### <span data-ttu-id="a1888-137">System. void</span><span class="sxs-lookup"><span data-stu-id="a1888-137">System.Void</span></span>

### <span data-ttu-id="a1888-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1888-138">System.Boolean</span></span>

## <span data-ttu-id="a1888-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1888-139">NOTES</span></span>

## <span data-ttu-id="a1888-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1888-140">RELATED LINKS</span></span>
