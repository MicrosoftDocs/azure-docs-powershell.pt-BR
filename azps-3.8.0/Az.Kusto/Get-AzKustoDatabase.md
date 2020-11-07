---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: f78dd41283312434f8a3ea833f9c96df6527cb95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941133"
---
# <span data-ttu-id="78305-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="78305-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="78305-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78305-102">SYNOPSIS</span></span>
<span data-ttu-id="78305-103">Liste todos os bancos de dados do Kusto em um cluster ou obtenha um banco de dados específico do Kusto.</span><span class="sxs-lookup"><span data-stu-id="78305-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="78305-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78305-104">SYNTAX</span></span>

### <span data-ttu-id="78305-105">ByClusterOrResourceGroupOrSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="78305-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78305-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78305-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78305-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78305-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78305-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78305-108">DESCRIPTION</span></span>
<span data-ttu-id="78305-109">Liste todos os bancos de dados do Kusto em um cluster ou obtenha um banco de dados específico do Kusto.</span><span class="sxs-lookup"><span data-stu-id="78305-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="78305-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78305-110">EXAMPLES</span></span>

### <span data-ttu-id="78305-111">Exemplo 1-listar todos os bancos de dados do Kusto em um cluster por nome</span><span class="sxs-lookup"><span data-stu-id="78305-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="78305-112">O comando acima retorna todos os bancos de dados do Kusto no cluster "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="78305-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="78305-113">Exemplo 2-listar todos os bancos de dados do Kusto em um cluster por tubulação</span><span class="sxs-lookup"><span data-stu-id="78305-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="78305-114">O comando acima obterá o cluster Kusto chamado "mykustocluster" localizado no grupo de recursos "testrg" usando o `Get-AzKustoCluster` cmdlet e canalizará o resultado para o `Get-AzKustoDatabase` cmdlet para listar todos os bancos de dados nesse cluster.</span><span class="sxs-lookup"><span data-stu-id="78305-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="78305-115">Exemplo 3-obter um banco de dados do Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="78305-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="78305-116">O comando acima retorna o banco de dados Kusto chamado "mykustodatabase" no cluster "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="78305-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="78305-117">OS</span><span class="sxs-lookup"><span data-stu-id="78305-117">PARAMETERS</span></span>

### <span data-ttu-id="78305-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="78305-118">-ClusterName</span></span>
<span data-ttu-id="78305-119">Nome do cluster sob o qual o banco de dados existe.</span><span class="sxs-lookup"><span data-stu-id="78305-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78305-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78305-120">-DefaultProfile</span></span>
<span data-ttu-id="78305-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78305-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78305-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78305-122">-InputObject</span></span>
<span data-ttu-id="78305-123">Objeto de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="78305-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78305-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="78305-124">-Name</span></span>
<span data-ttu-id="78305-125">o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="78305-125">the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78305-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78305-126">-ResourceGroupName</span></span>
<span data-ttu-id="78305-127">Nome do grupo de recursos sob o qual o usuário quer recuperar o cluster.</span><span class="sxs-lookup"><span data-stu-id="78305-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78305-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78305-128">-ResourceId</span></span>
<span data-ttu-id="78305-129">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="78305-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78305-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78305-130">CommonParameters</span></span>
<span data-ttu-id="78305-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78305-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78305-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78305-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78305-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78305-133">INPUTS</span></span>

### <span data-ttu-id="78305-134">System. String</span><span class="sxs-lookup"><span data-stu-id="78305-134">System.String</span></span>

### <span data-ttu-id="78305-135">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="78305-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="78305-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78305-136">OUTPUTS</span></span>

### <span data-ttu-id="78305-137">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="78305-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="78305-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78305-138">NOTES</span></span>

## <span data-ttu-id="78305-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78305-139">RELATED LINKS</span></span>
