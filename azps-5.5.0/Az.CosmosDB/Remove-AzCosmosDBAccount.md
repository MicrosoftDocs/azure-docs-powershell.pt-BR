---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115906"
---
# <span data-ttu-id="172d9-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="172d9-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="172d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="172d9-102">SYNOPSIS</span></span>
<span data-ttu-id="172d9-103">Remover uma Conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="172d9-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="172d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="172d9-104">SYNTAX</span></span>

### <span data-ttu-id="172d9-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="172d9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="172d9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="172d9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="172d9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="172d9-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="172d9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="172d9-108">DESCRIPTION</span></span>
<span data-ttu-id="172d9-109">Remover uma Conta do CosmosDB com um determinado Nome no Determinado Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="172d9-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="172d9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="172d9-110">EXAMPLES</span></span>

### <span data-ttu-id="172d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="172d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="172d9-112">A Conta com nome de conta dbname no ResourceGroup rg é excluída.</span><span class="sxs-lookup"><span data-stu-id="172d9-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="172d9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="172d9-113">PARAMETERS</span></span>

### <span data-ttu-id="172d9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="172d9-114">-AsJob</span></span>
<span data-ttu-id="172d9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="172d9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="172d9-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="172d9-116">-Confirm</span></span>
<span data-ttu-id="172d9-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="172d9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="172d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172d9-118">-DefaultProfile</span></span>
<span data-ttu-id="172d9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="172d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="172d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="172d9-120">-InputObject</span></span>
<span data-ttu-id="172d9-121">O objeto Conta de Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="172d9-121">The Database Account object</span></span>

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

### <span data-ttu-id="172d9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="172d9-122">-Name</span></span>
<span data-ttu-id="172d9-123">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="172d9-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="172d9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="172d9-124">-PassThru</span></span>
<span data-ttu-id="172d9-125">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="172d9-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="172d9-126">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="172d9-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="172d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="172d9-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="172d9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="172d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="172d9-129">-ResourceId</span></span>
<span data-ttu-id="172d9-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="172d9-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="172d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="172d9-131">-WhatIf</span></span>
<span data-ttu-id="172d9-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="172d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="172d9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="172d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="172d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172d9-134">CommonParameters</span></span>
<span data-ttu-id="172d9-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172d9-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="172d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172d9-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="172d9-137">INPUTS</span></span>

### <span data-ttu-id="172d9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="172d9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="172d9-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="172d9-139">OUTPUTS</span></span>

### <span data-ttu-id="172d9-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="172d9-140">System.Void</span></span>

## <span data-ttu-id="172d9-141">Notas</span><span class="sxs-lookup"><span data-stu-id="172d9-141">NOTES</span></span>

## <span data-ttu-id="172d9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="172d9-142">RELATED LINKS</span></span>
