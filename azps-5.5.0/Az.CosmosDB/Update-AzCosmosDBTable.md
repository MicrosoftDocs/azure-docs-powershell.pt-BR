---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115898"
---
# <span data-ttu-id="f27ff-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="f27ff-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="f27ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f27ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f27ff-103">Atualiza a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f27ff-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="f27ff-104">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="f27ff-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="f27ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f27ff-105">SYNTAX</span></span>

### <span data-ttu-id="f27ff-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f27ff-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f27ff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f27ff-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f27ff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f27ff-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f27ff-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f27ff-109">DESCRIPTION</span></span>
<span data-ttu-id="f27ff-110">Atualiza a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f27ff-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="f27ff-111">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="f27ff-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="f27ff-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f27ff-112">EXAMPLES</span></span>

### <span data-ttu-id="f27ff-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f27ff-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="f27ff-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f27ff-114">PARAMETERS</span></span>

### <span data-ttu-id="f27ff-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f27ff-115">-AccountName</span></span>
<span data-ttu-id="f27ff-116">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="f27ff-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f27ff-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f27ff-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f27ff-118">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="f27ff-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f27ff-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f27ff-119">-Confirm</span></span>
<span data-ttu-id="f27ff-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f27ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f27ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27ff-121">-DefaultProfile</span></span>
<span data-ttu-id="f27ff-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f27ff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27ff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f27ff-123">-InputObject</span></span>
<span data-ttu-id="f27ff-124">Objeto table.</span><span class="sxs-lookup"><span data-stu-id="f27ff-124">Table Object.</span></span>

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

### <span data-ttu-id="f27ff-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f27ff-125">-Name</span></span>
<span data-ttu-id="f27ff-126">Nome da Tabela.</span><span class="sxs-lookup"><span data-stu-id="f27ff-126">Name of the Table.</span></span>

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

### <span data-ttu-id="f27ff-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f27ff-127">-ParentObject</span></span>
<span data-ttu-id="f27ff-128">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="f27ff-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f27ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="f27ff-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f27ff-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f27ff-131">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="f27ff-131">-Throughput</span></span>
<span data-ttu-id="f27ff-132">A produtividade da tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f27ff-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="f27ff-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="f27ff-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f27ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f27ff-134">-WhatIf</span></span>
<span data-ttu-id="f27ff-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f27ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f27ff-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f27ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f27ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27ff-137">CommonParameters</span></span>
<span data-ttu-id="f27ff-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27ff-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f27ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27ff-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="f27ff-140">INPUTS</span></span>

### <span data-ttu-id="f27ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f27ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f27ff-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f27ff-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="f27ff-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="f27ff-143">OUTPUTS</span></span>

### <span data-ttu-id="f27ff-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f27ff-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="f27ff-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f27ff-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f27ff-146">Notas</span><span class="sxs-lookup"><span data-stu-id="f27ff-146">NOTES</span></span>

## <span data-ttu-id="f27ff-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f27ff-147">RELATED LINKS</span></span>
