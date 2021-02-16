---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117786"
---
# <span data-ttu-id="8e443-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="8e443-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="8e443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e443-102">SYNOPSIS</span></span>
<span data-ttu-id="8e443-103">Cria uma nova Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8e443-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="8e443-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e443-104">SYNTAX</span></span>

### <span data-ttu-id="8e443-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e443-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e443-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e443-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e443-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e443-107">DESCRIPTION</span></span>
<span data-ttu-id="8e443-108">Cria uma nova Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8e443-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="8e443-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e443-109">EXAMPLES</span></span>

### <span data-ttu-id="8e443-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e443-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="8e443-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e443-111">PARAMETERS</span></span>

### <span data-ttu-id="8e443-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8e443-112">-AccountName</span></span>
<span data-ttu-id="8e443-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="8e443-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8e443-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8e443-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8e443-115">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8e443-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e443-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e443-116">-Confirm</span></span>
<span data-ttu-id="8e443-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e443-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e443-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e443-118">-DefaultProfile</span></span>
<span data-ttu-id="8e443-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e443-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e443-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e443-120">-Name</span></span>
<span data-ttu-id="8e443-121">Nome da Tabela.</span><span class="sxs-lookup"><span data-stu-id="8e443-121">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e443-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e443-122">-ParentObject</span></span>
<span data-ttu-id="8e443-123">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="8e443-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e443-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e443-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e443-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e443-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8e443-126">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="8e443-126">-Throughput</span></span>
<span data-ttu-id="8e443-127">A produtividade da tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8e443-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="8e443-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8e443-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e443-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e443-129">-WhatIf</span></span>
<span data-ttu-id="8e443-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e443-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e443-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e443-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e443-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e443-132">CommonParameters</span></span>
<span data-ttu-id="8e443-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e443-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e443-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e443-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e443-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e443-135">INPUTS</span></span>

### <span data-ttu-id="8e443-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8e443-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8e443-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e443-137">OUTPUTS</span></span>

### <span data-ttu-id="8e443-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8e443-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="8e443-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="8e443-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="8e443-140">Notas</span><span class="sxs-lookup"><span data-stu-id="8e443-140">NOTES</span></span>

## <span data-ttu-id="8e443-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e443-141">RELATED LINKS</span></span>
