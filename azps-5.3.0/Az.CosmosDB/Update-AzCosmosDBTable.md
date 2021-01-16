---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429993"
---
# <span data-ttu-id="1c14d-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="1c14d-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="1c14d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c14d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c14d-103">Atualiza a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1c14d-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1c14d-104">Executa uma operação de patch do lado do cliente lendo a tabela existente.</span><span class="sxs-lookup"><span data-stu-id="1c14d-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1c14d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c14d-105">SYNTAX</span></span>

### <span data-ttu-id="1c14d-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c14d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c14d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c14d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c14d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c14d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c14d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c14d-109">DESCRIPTION</span></span>
<span data-ttu-id="1c14d-110">Atualiza a tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1c14d-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1c14d-111">Executa uma operação de patch do lado do cliente lendo a tabela existente.</span><span class="sxs-lookup"><span data-stu-id="1c14d-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1c14d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c14d-112">EXAMPLES</span></span>

### <span data-ttu-id="1c14d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c14d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="1c14d-114">OS</span><span class="sxs-lookup"><span data-stu-id="1c14d-114">PARAMETERS</span></span>

### <span data-ttu-id="1c14d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c14d-115">-AccountName</span></span>
<span data-ttu-id="1c14d-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="1c14d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1c14d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1c14d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1c14d-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="1c14d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1c14d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c14d-119">-Confirm</span></span>
<span data-ttu-id="1c14d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c14d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c14d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c14d-121">-DefaultProfile</span></span>
<span data-ttu-id="1c14d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c14d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c14d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c14d-123">-InputObject</span></span>
<span data-ttu-id="1c14d-124">Objeto Table.</span><span class="sxs-lookup"><span data-stu-id="1c14d-124">Table Object.</span></span>

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

### <span data-ttu-id="1c14d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c14d-125">-Name</span></span>
<span data-ttu-id="1c14d-126">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="1c14d-126">Name of the Table.</span></span>

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

### <span data-ttu-id="1c14d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1c14d-127">-ParentObject</span></span>
<span data-ttu-id="1c14d-128">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1c14d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1c14d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c14d-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c14d-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c14d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="1c14d-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1c14d-131">-Throughput</span></span>
<span data-ttu-id="1c14d-132">A taxa de transferência da tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1c14d-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="1c14d-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="1c14d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="1c14d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c14d-134">-WhatIf</span></span>
<span data-ttu-id="1c14d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c14d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c14d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c14d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c14d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c14d-137">CommonParameters</span></span>
<span data-ttu-id="1c14d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c14d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c14d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c14d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c14d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c14d-140">INPUTS</span></span>

### <span data-ttu-id="1c14d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1c14d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="1c14d-142">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1c14d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="1c14d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c14d-143">OUTPUTS</span></span>

### <span data-ttu-id="1c14d-144">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1c14d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="1c14d-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1c14d-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1c14d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c14d-146">NOTES</span></span>

## <span data-ttu-id="1c14d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c14d-147">RELATED LINKS</span></span>
