---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: 64d6f0bd604e8074d593f20a572768b54ced8a59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886484"
---
# <span data-ttu-id="66edf-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="66edf-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="66edf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66edf-102">SYNOPSIS</span></span>
<span data-ttu-id="66edf-103">Remover uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="66edf-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="66edf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="66edf-104">SYNTAX</span></span>

### <span data-ttu-id="66edf-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66edf-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66edf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66edf-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66edf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66edf-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66edf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="66edf-108">DESCRIPTION</span></span>
<span data-ttu-id="66edf-109">Remova uma conta do CosmosDB com um determinado Nome no ResourceGroup determinado.</span><span class="sxs-lookup"><span data-stu-id="66edf-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="66edf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66edf-110">EXAMPLES</span></span>

### <span data-ttu-id="66edf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66edf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="66edf-112">A conta com nome da conta dbname no rg ResourceGroup é excluída.</span><span class="sxs-lookup"><span data-stu-id="66edf-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="66edf-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="66edf-113">PARAMETERS</span></span>

### <span data-ttu-id="66edf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66edf-114">-AsJob</span></span>
<span data-ttu-id="66edf-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="66edf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66edf-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66edf-116">-Confirm</span></span>
<span data-ttu-id="66edf-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66edf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66edf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66edf-118">-DefaultProfile</span></span>
<span data-ttu-id="66edf-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66edf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66edf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66edf-120">-InputObject</span></span>
<span data-ttu-id="66edf-121">O objeto Database Account</span><span class="sxs-lookup"><span data-stu-id="66edf-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66edf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="66edf-122">-Name</span></span>
<span data-ttu-id="66edf-123">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="66edf-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66edf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66edf-124">-PassThru</span></span>
<span data-ttu-id="66edf-125">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="66edf-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="66edf-126">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="66edf-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="66edf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66edf-127">-ResourceGroupName</span></span>
<span data-ttu-id="66edf-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66edf-128">Name of resource group.</span></span>

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

### <span data-ttu-id="66edf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66edf-129">-ResourceId</span></span>
<span data-ttu-id="66edf-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="66edf-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66edf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66edf-131">-WhatIf</span></span>
<span data-ttu-id="66edf-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66edf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66edf-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66edf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66edf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66edf-134">CommonParameters</span></span>
<span data-ttu-id="66edf-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66edf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66edf-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66edf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66edf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66edf-137">INPUTS</span></span>

### <span data-ttu-id="66edf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="66edf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="66edf-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="66edf-139">OUTPUTS</span></span>

### <span data-ttu-id="66edf-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="66edf-140">System.Void</span></span>

## <span data-ttu-id="66edf-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="66edf-141">NOTES</span></span>

## <span data-ttu-id="66edf-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66edf-142">RELATED LINKS</span></span>
