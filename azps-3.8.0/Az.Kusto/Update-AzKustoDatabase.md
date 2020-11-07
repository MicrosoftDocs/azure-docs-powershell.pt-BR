---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941114"
---
# <span data-ttu-id="abae5-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="abae5-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="abae5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abae5-102">SYNOPSIS</span></span>
<span data-ttu-id="abae5-103">Atualizar um banco de dados do Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="abae5-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="abae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abae5-104">SYNTAX</span></span>

### <span data-ttu-id="abae5-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="abae5-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abae5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abae5-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abae5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="abae5-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abae5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abae5-108">DESCRIPTION</span></span>
<span data-ttu-id="abae5-109">Atualizar um banco de dados do Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="abae5-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="abae5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abae5-110">EXAMPLES</span></span>

### <span data-ttu-id="abae5-111">Exemplo 1-atualize um banco de dados existente por nome</span><span class="sxs-lookup"><span data-stu-id="abae5-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="abae5-112">O comando acima atualiza o período de exclusão suave do banco de dados do Kusto "mykustodatabase" no cluster "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="abae5-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="abae5-113">Exemplo 2-atualizar um banco de dados existente por tubulação</span><span class="sxs-lookup"><span data-stu-id="abae5-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="abae5-114">O comando acima Obtém o banco de dados Kusto "mykustodatabase" no cluster "mykustocluster" localizado no grupo de recursos "testrg" usando o `Get-AzKustoDatabase` cmdlet e canaliza o resultado para `Update-AzKustoDatabase` atualizar o período de exclusão flexível do banco de dados para cinco dias.</span><span class="sxs-lookup"><span data-stu-id="abae5-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="abae5-115">OS</span><span class="sxs-lookup"><span data-stu-id="abae5-115">PARAMETERS</span></span>

### <span data-ttu-id="abae5-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="abae5-116">-ClusterName</span></span>
<span data-ttu-id="abae5-117">Nome do cluster sob o qual o banco de dados existe</span><span class="sxs-lookup"><span data-stu-id="abae5-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abae5-118">-DefaultProfile</span></span>
<span data-ttu-id="abae5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abae5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="abae5-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="abae5-121">O número de dias pelos quais os dados devem ser mantidos em cache para consultas rápidas</span><span class="sxs-lookup"><span data-stu-id="abae5-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abae5-122">-InputObject</span></span>
<span data-ttu-id="abae5-123">Objeto de banco de dados Kusto.</span><span class="sxs-lookup"><span data-stu-id="abae5-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="abae5-124">-Name</span></span>
<span data-ttu-id="abae5-125">Nome do banco de dados a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="abae5-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abae5-126">-ResourceGroupName</span></span>
<span data-ttu-id="abae5-127">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="abae5-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abae5-128">-ResourceId</span></span>
<span data-ttu-id="abae5-129">ResourceId de banco de dados Kusto.</span><span class="sxs-lookup"><span data-stu-id="abae5-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="abae5-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="abae5-131">O número de dias durante os quais os dados devem ser mantidos antes de deixar de ser acessível às consultas</span><span class="sxs-lookup"><span data-stu-id="abae5-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abae5-132">-Confirm</span></span>
<span data-ttu-id="abae5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abae5-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abae5-134">-WhatIf</span></span>
<span data-ttu-id="abae5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abae5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abae5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abae5-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abae5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abae5-137">CommonParameters</span></span>
<span data-ttu-id="abae5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abae5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abae5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abae5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abae5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abae5-140">INPUTS</span></span>

### <span data-ttu-id="abae5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abae5-141">System.String</span></span>

### <span data-ttu-id="abae5-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="abae5-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="abae5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abae5-143">OUTPUTS</span></span>

### <span data-ttu-id="abae5-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="abae5-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="abae5-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abae5-145">NOTES</span></span>

## <span data-ttu-id="abae5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abae5-146">RELATED LINKS</span></span>
