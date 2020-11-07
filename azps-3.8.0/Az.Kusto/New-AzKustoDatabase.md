---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: ed039eefe46a1527948e7fffc3030f209a91b0c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941131"
---
# <span data-ttu-id="ce39c-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ce39c-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="ce39c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce39c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce39c-103">Cria um novo banco de dados do Kusto em um cluster existente.</span><span class="sxs-lookup"><span data-stu-id="ce39c-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="ce39c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce39c-104">SYNTAX</span></span>

### <span data-ttu-id="ce39c-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce39c-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce39c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce39c-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce39c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce39c-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce39c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce39c-108">DESCRIPTION</span></span>
<span data-ttu-id="ce39c-109">Cria um novo banco de dados do Kusto em um cluster existente.</span><span class="sxs-lookup"><span data-stu-id="ce39c-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="ce39c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce39c-110">EXAMPLES</span></span>

### <span data-ttu-id="ce39c-111">Exemplo 1-criar um novo banco de dados do Kusto por nome</span><span class="sxs-lookup"><span data-stu-id="ce39c-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="ce39c-112">O comando acima cria um novo banco de dados Kusto chamado "mykustodatabase" no cluster existente "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="ce39c-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="ce39c-113">OS</span><span class="sxs-lookup"><span data-stu-id="ce39c-113">PARAMETERS</span></span>

### <span data-ttu-id="ce39c-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ce39c-114">-ClusterName</span></span>
<span data-ttu-id="ce39c-115">Nome do cluster sob o qual você deseja criar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ce39c-115">Name of cluster under which you want to create the database.</span></span>

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

### <span data-ttu-id="ce39c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce39c-116">-DefaultProfile</span></span>
<span data-ttu-id="ce39c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce39c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce39c-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ce39c-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="ce39c-119">O número de dias de dados que devem ser mantidos em cache para consultas rápidas.</span><span class="sxs-lookup"><span data-stu-id="ce39c-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce39c-120">-InputObject</span></span>
<span data-ttu-id="ce39c-121">Objeto de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce39c-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce39c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce39c-122">-Name</span></span>
<span data-ttu-id="ce39c-123">Nome do banco de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ce39c-123">Name of the database to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce39c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce39c-125">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="ce39c-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="ce39c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce39c-126">-ResourceId</span></span>
<span data-ttu-id="ce39c-127">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce39c-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="ce39c-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ce39c-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="ce39c-129">O número de dias durante os quais os dados devem ser mantidos antes de deixar de ser acessível às consultas.</span><span class="sxs-lookup"><span data-stu-id="ce39c-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce39c-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce39c-130">-Confirm</span></span>
<span data-ttu-id="ce39c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce39c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce39c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce39c-132">-WhatIf</span></span>
<span data-ttu-id="ce39c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce39c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce39c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce39c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce39c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce39c-135">CommonParameters</span></span>
<span data-ttu-id="ce39c-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce39c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce39c-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce39c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce39c-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce39c-138">INPUTS</span></span>

### <span data-ttu-id="ce39c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ce39c-139">System.String</span></span>

### <span data-ttu-id="ce39c-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ce39c-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="ce39c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce39c-141">OUTPUTS</span></span>

### <span data-ttu-id="ce39c-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="ce39c-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="ce39c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce39c-143">NOTES</span></span>

## <span data-ttu-id="ce39c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce39c-144">RELATED LINKS</span></span>
