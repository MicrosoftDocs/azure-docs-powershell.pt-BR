---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281278"
---
# <span data-ttu-id="ce716-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="ce716-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="ce716-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce716-102">SYNOPSIS</span></span>
<span data-ttu-id="ce716-103">Remova uma conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ce716-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="ce716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce716-104">SYNTAX</span></span>

### <span data-ttu-id="ce716-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce716-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce716-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce716-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce716-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce716-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce716-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce716-108">DESCRIPTION</span></span>
<span data-ttu-id="ce716-109">Remova uma conta do CosmosDB com um nome específico em um determinado nome de Resource.</span><span class="sxs-lookup"><span data-stu-id="ce716-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="ce716-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce716-110">EXAMPLES</span></span>

### <span data-ttu-id="ce716-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce716-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="ce716-112">A conta com o nome de conta dbname no nome de conta de Resource é excluída.</span><span class="sxs-lookup"><span data-stu-id="ce716-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="ce716-113">OS</span><span class="sxs-lookup"><span data-stu-id="ce716-113">PARAMETERS</span></span>

### <span data-ttu-id="ce716-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce716-114">-AsJob</span></span>
<span data-ttu-id="ce716-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ce716-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce716-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce716-116">-Confirm</span></span>
<span data-ttu-id="ce716-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce716-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce716-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce716-118">-DefaultProfile</span></span>
<span data-ttu-id="ce716-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce716-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce716-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce716-120">-InputObject</span></span>
<span data-ttu-id="ce716-121">O objeto da conta de banco de dados</span><span class="sxs-lookup"><span data-stu-id="ce716-121">The Database Account object</span></span>

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

### <span data-ttu-id="ce716-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce716-122">-Name</span></span>
<span data-ttu-id="ce716-123">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="ce716-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ce716-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce716-124">-PassThru</span></span>
<span data-ttu-id="ce716-125">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="ce716-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ce716-126">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="ce716-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ce716-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce716-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce716-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce716-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ce716-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce716-129">-ResourceId</span></span>
<span data-ttu-id="ce716-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce716-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="ce716-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce716-131">-WhatIf</span></span>
<span data-ttu-id="ce716-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce716-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce716-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce716-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce716-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce716-134">CommonParameters</span></span>
<span data-ttu-id="ce716-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce716-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce716-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce716-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce716-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce716-137">INPUTS</span></span>

### <span data-ttu-id="ce716-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ce716-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ce716-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce716-139">OUTPUTS</span></span>

### <span data-ttu-id="ce716-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ce716-140">System.Void</span></span>

## <span data-ttu-id="ce716-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce716-141">NOTES</span></span>

## <span data-ttu-id="ce716-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce716-142">RELATED LINKS</span></span>
