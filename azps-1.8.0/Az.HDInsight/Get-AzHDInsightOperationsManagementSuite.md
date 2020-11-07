---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770807"
---
# <span data-ttu-id="db1eb-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="db1eb-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="db1eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="db1eb-103">Obtém o status da instalação do Operations Management Suite (OMS) no cluster.</span><span class="sxs-lookup"><span data-stu-id="db1eb-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="db1eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db1eb-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db1eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="db1eb-106">O cmdlet **Get-AzHDInsightOperationsManagementSuite** Obtém o status da instalação do OMS em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db1eb-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="db1eb-107">Se o OMS estiver habilitado, também retornará a ID do espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="db1eb-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="db1eb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db1eb-108">EXAMPLES</span></span>

### <span data-ttu-id="db1eb-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db1eb-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="db1eb-110">O Operations Management Suite (OMS) está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é true.</span><span class="sxs-lookup"><span data-stu-id="db1eb-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="db1eb-111">A ID do espaço de trabalho do OMS em que os logs estão fluindo são 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="db1eb-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="db1eb-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db1eb-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="db1eb-113">O Operations Management Suite (OMS) está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é true.</span><span class="sxs-lookup"><span data-stu-id="db1eb-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="db1eb-114">A ID do espaço de trabalho do OMS em que os logs estão fluindo são 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="db1eb-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="db1eb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db1eb-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="db1eb-116">O Operations Management Suite (OMS) está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="db1eb-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="db1eb-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="db1eb-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="db1eb-118">O Operations Management Suite (OMS) está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="db1eb-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="db1eb-119">OS</span><span class="sxs-lookup"><span data-stu-id="db1eb-119">PARAMETERS</span></span>

### <span data-ttu-id="db1eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1eb-120">-DefaultProfile</span></span>
<span data-ttu-id="db1eb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db1eb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db1eb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="db1eb-122">-Name</span></span>
<span data-ttu-id="db1eb-123">O nome do cluster para obter o status do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="db1eb-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db1eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="db1eb-125">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="db1eb-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="db1eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1eb-126">CommonParameters</span></span>
<span data-ttu-id="db1eb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1eb-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1eb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db1eb-129">INPUTS</span></span>

### <span data-ttu-id="db1eb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="db1eb-130">System.String</span></span>

## <span data-ttu-id="db1eb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db1eb-131">OUTPUTS</span></span>

### <span data-ttu-id="db1eb-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="db1eb-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="db1eb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db1eb-133">NOTES</span></span>

## <span data-ttu-id="db1eb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db1eb-134">RELATED LINKS</span></span>
