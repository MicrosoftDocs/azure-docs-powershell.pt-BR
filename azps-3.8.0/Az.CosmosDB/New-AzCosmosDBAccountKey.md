---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941917"
---
# <span data-ttu-id="cc234-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="cc234-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="cc234-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc234-102">SYNOPSIS</span></span>
<span data-ttu-id="cc234-103">Regenere uma determinada chave de conta do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cc234-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="cc234-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc234-104">SYNTAX</span></span>

### <span data-ttu-id="cc234-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc234-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc234-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc234-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc234-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc234-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc234-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc234-108">DESCRIPTION</span></span>
<span data-ttu-id="cc234-109">Crie uma nova conta do CosmosDB em um determinado.</span><span class="sxs-lookup"><span data-stu-id="cc234-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="cc234-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc234-110">EXAMPLES</span></span>

### <span data-ttu-id="cc234-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc234-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="cc234-112">Novas chaves são geradas para a conta com o nome de conta dbname no nome de conta de Resource.</span><span class="sxs-lookup"><span data-stu-id="cc234-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="cc234-113">OS</span><span class="sxs-lookup"><span data-stu-id="cc234-113">PARAMETERS</span></span>

### <span data-ttu-id="cc234-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc234-114">-AsJob</span></span>
<span data-ttu-id="cc234-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cc234-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc234-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc234-116">-Confirm</span></span>
<span data-ttu-id="cc234-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc234-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc234-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc234-118">-DefaultProfile</span></span>
<span data-ttu-id="cc234-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc234-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc234-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc234-120">-InputObject</span></span>
<span data-ttu-id="cc234-121">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="cc234-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc234-122">-Keykind</span><span class="sxs-lookup"><span data-stu-id="cc234-122">-KeyKind</span></span>
<span data-ttu-id="cc234-123">A tecla de acesso a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="cc234-123">The access key to regenerate.</span></span>
<span data-ttu-id="cc234-124">Valores aceitos: principal, primaryReadonly, secundário, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="cc234-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc234-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc234-125">-Name</span></span>
<span data-ttu-id="cc234-126">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="cc234-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cc234-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc234-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc234-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc234-128">Name of resource group.</span></span>

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

### <span data-ttu-id="cc234-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc234-129">-ResourceId</span></span>
<span data-ttu-id="cc234-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="cc234-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="cc234-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc234-131">-WhatIf</span></span>
<span data-ttu-id="cc234-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc234-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc234-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc234-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc234-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc234-134">CommonParameters</span></span>
<span data-ttu-id="cc234-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc234-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc234-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc234-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc234-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc234-137">INPUTS</span></span>

### <span data-ttu-id="cc234-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cc234-138">None</span></span>

## <span data-ttu-id="cc234-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc234-139">OUTPUTS</span></span>

### <span data-ttu-id="cc234-140">System. void</span><span class="sxs-lookup"><span data-stu-id="cc234-140">System.Void</span></span>

## <span data-ttu-id="cc234-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc234-141">NOTES</span></span>

## <span data-ttu-id="cc234-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc234-142">RELATED LINKS</span></span>
