---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262240"
---
# <span data-ttu-id="d039b-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="d039b-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="d039b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d039b-102">SYNOPSIS</span></span>
<span data-ttu-id="d039b-103">Lista os hosts do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d039b-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="d039b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d039b-104">SYNTAX</span></span>

### <span data-ttu-id="d039b-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d039b-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d039b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d039b-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d039b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d039b-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d039b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d039b-108">DESCRIPTION</span></span>
<span data-ttu-id="d039b-109">O cmdlet **Get-AzHDInsightHost** lista os hosts do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d039b-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="d039b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d039b-110">EXAMPLES</span></span>

### <span data-ttu-id="d039b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d039b-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="d039b-112">Este comando lista os hosts do cluster com nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d039b-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="d039b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d039b-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="d039b-114">Este comando lista os hosts do cluster com pipeline.</span><span class="sxs-lookup"><span data-stu-id="d039b-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="d039b-115">OS</span><span class="sxs-lookup"><span data-stu-id="d039b-115">PARAMETERS</span></span>

### <span data-ttu-id="d039b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d039b-116">-ClusterName</span></span>
<span data-ttu-id="d039b-117">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="d039b-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="d039b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d039b-118">-DefaultProfile</span></span>
<span data-ttu-id="d039b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d039b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d039b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d039b-120">-InputObject</span></span>
<span data-ttu-id="d039b-121">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d039b-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="d039b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d039b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d039b-123">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d039b-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="d039b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d039b-124">-ResourceId</span></span>
<span data-ttu-id="d039b-125">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d039b-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="d039b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d039b-126">CommonParameters</span></span>
<span data-ttu-id="d039b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d039b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d039b-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d039b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d039b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d039b-129">INPUTS</span></span>

### <span data-ttu-id="d039b-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d039b-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d039b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d039b-131">OUTPUTS</span></span>

### <span data-ttu-id="d039b-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="d039b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="d039b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d039b-133">NOTES</span></span>

## <span data-ttu-id="d039b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d039b-134">RELATED LINKS</span></span>
