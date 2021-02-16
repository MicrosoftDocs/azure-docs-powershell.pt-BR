---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117638"
---
# <span data-ttu-id="c1ad7-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="c1ad7-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="c1ad7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ad7-103">Obtém o status da instalação de monitoramento no cluster.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="c1ad7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1ad7-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1ad7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ad7-106">O cmdlet **Get-AzHDInsightMonitoring** obtém o status da instalação de monitoramento em um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="c1ad7-107">Se o monitoramento estiver habilitado, ele também retornará a ID do espaço de trabalho de análise de log.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="c1ad7-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1ad7-108">EXAMPLES</span></span>

### <span data-ttu-id="c1ad7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1ad7-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="c1ad7-110">O monitoramento está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="c1ad7-111">A ID do espaço de trabalho de monitoramento para onde os logs estão fluindo é 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="c1ad7-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="c1ad7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c1ad7-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="c1ad7-113">O monitoramento está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="c1ad7-114">A ID do espaço de trabalho de monitoramento para onde os logs estão fluindo é 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="c1ad7-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="c1ad7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c1ad7-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="c1ad7-116">O monitoramento está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="c1ad7-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c1ad7-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="c1ad7-118">O monitoramento está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="c1ad7-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1ad7-119">PARAMETERS</span></span>

### <span data-ttu-id="c1ad7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ad7-120">-DefaultProfile</span></span>
<span data-ttu-id="c1ad7-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c1ad7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1ad7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1ad7-122">-Name</span></span>
<span data-ttu-id="c1ad7-123">O nome do cluster para obter o status do monitoramento.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="c1ad7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ad7-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1ad7-125">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="c1ad7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ad7-126">CommonParameters</span></span>
<span data-ttu-id="c1ad7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ad7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ad7-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1ad7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ad7-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1ad7-129">INPUTS</span></span>

### <span data-ttu-id="c1ad7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c1ad7-130">System.String</span></span>

## <span data-ttu-id="c1ad7-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1ad7-131">OUTPUTS</span></span>

### <span data-ttu-id="c1ad7-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="c1ad7-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="c1ad7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="c1ad7-133">NOTES</span></span>

## <span data-ttu-id="c1ad7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1ad7-134">RELATED LINKS</span></span>
