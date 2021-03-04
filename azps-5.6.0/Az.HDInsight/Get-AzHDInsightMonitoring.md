---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892793"
---
# <span data-ttu-id="3510b-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="3510b-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="3510b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3510b-102">SYNOPSIS</span></span>
<span data-ttu-id="3510b-103">Obtém o status da instalação de monitoramento no cluster.</span><span class="sxs-lookup"><span data-stu-id="3510b-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="3510b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3510b-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3510b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3510b-105">DESCRIPTION</span></span>
<span data-ttu-id="3510b-106">O cmdlet **Get-AzHDInsightMonitoring** obtém o status da instalação de monitoramento em um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="3510b-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="3510b-107">Se o monitoramento estiver habilitado, ele também retornará a ID do espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="3510b-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="3510b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3510b-108">EXAMPLES</span></span>

### <span data-ttu-id="3510b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3510b-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3510b-110">O monitoramento está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="3510b-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3510b-111">A ID do espaço de trabalho de monitoramento onde os logs estão fluindo é 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3510b-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3510b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3510b-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3510b-113">O monitoramento está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="3510b-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3510b-114">A ID do espaço de trabalho de monitoramento onde os logs estão fluindo é 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3510b-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3510b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3510b-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="3510b-116">O monitoramento está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é false.</span><span class="sxs-lookup"><span data-stu-id="3510b-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="3510b-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="3510b-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="3510b-118">O monitoramento está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é false.</span><span class="sxs-lookup"><span data-stu-id="3510b-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="3510b-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3510b-119">PARAMETERS</span></span>

### <span data-ttu-id="3510b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3510b-120">-DefaultProfile</span></span>
<span data-ttu-id="3510b-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3510b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3510b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3510b-122">-Name</span></span>
<span data-ttu-id="3510b-123">O nome do cluster para obter o status do monitoramento.</span><span class="sxs-lookup"><span data-stu-id="3510b-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3510b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3510b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3510b-125">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="3510b-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3510b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3510b-126">CommonParameters</span></span>
<span data-ttu-id="3510b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3510b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3510b-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3510b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3510b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3510b-129">INPUTS</span></span>

### <span data-ttu-id="3510b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3510b-130">System.String</span></span>

## <span data-ttu-id="3510b-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3510b-131">OUTPUTS</span></span>

### <span data-ttu-id="3510b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="3510b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="3510b-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="3510b-133">NOTES</span></span>

## <span data-ttu-id="3510b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3510b-134">RELATED LINKS</span></span>
