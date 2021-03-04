---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893166"
---
# <span data-ttu-id="667c9-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="667c9-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="667c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667c9-102">SYNOPSIS</span></span>
<span data-ttu-id="667c9-103">Lista os hosts do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="667c9-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="667c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="667c9-104">SYNTAX</span></span>

### <span data-ttu-id="667c9-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="667c9-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="667c9-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="667c9-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="667c9-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667c9-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="667c9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="667c9-108">DESCRIPTION</span></span>
<span data-ttu-id="667c9-109">O cmdlet **Get-AzHDInsightHost** lista os hosts do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="667c9-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="667c9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="667c9-110">EXAMPLES</span></span>

### <span data-ttu-id="667c9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="667c9-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="667c9-112">Este comando lista os hosts do cluster com o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="667c9-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="667c9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="667c9-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="667c9-114">Este comando lista os hosts do cluster com pipeline.</span><span class="sxs-lookup"><span data-stu-id="667c9-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="667c9-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="667c9-115">PARAMETERS</span></span>

### <span data-ttu-id="667c9-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="667c9-116">-ClusterName</span></span>
<span data-ttu-id="667c9-117">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="667c9-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667c9-118">-DefaultProfile</span></span>
<span data-ttu-id="667c9-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="667c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="667c9-120">-InputObject</span></span>
<span data-ttu-id="667c9-121">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="667c9-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="667c9-123">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="667c9-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667c9-124">-ResourceId</span></span>
<span data-ttu-id="667c9-125">Obtém ou define a id do recurso.</span><span class="sxs-lookup"><span data-stu-id="667c9-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667c9-126">CommonParameters</span></span>
<span data-ttu-id="667c9-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667c9-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="667c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667c9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="667c9-129">INPUTS</span></span>

### <span data-ttu-id="667c9-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="667c9-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="667c9-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="667c9-131">OUTPUTS</span></span>

### <span data-ttu-id="667c9-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="667c9-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="667c9-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="667c9-133">NOTES</span></span>

## <span data-ttu-id="667c9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="667c9-134">RELATED LINKS</span></span>
