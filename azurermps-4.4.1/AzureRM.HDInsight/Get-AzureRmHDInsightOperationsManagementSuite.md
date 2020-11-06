---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610792"
---
# <span data-ttu-id="f8b7f-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="f8b7f-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="f8b7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b7f-103">Obtém o status da instalação do Operations Management Suite (OMS) no cluster.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8b7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b7f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b7f-106">O cmdlet **Get-AzureRmHDInsightOperationsManagementSuite** Obtém o status da instalação do OMS em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="f8b7f-107">Se o OMS estiver habilitado, também retornará a ID do espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="f8b7f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-108">EXAMPLES</span></span>

### <span data-ttu-id="f8b7f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8b7f-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="f8b7f-110">O Operations Management Suite (OMS) está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é true.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="f8b7f-111">A ID do espaço de trabalho do OMS em que os logs estão fluindo são 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="f8b7f-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="f8b7f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f8b7f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="f8b7f-113">O Operations Management Suite (OMS) está habilitado no cluster porque a propriedade ClusterMonitoringEnabled é true.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="f8b7f-114">A ID do espaço de trabalho do OMS em que os logs estão fluindo são 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="f8b7f-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="f8b7f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f8b7f-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="f8b7f-116">O Operations Management Suite (OMS) está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="f8b7f-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="f8b7f-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="f8b7f-118">O Operations Management Suite (OMS) está desabilitado no cluster porque a propriedade ClusterMonitoringEnabled é falsa.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="f8b7f-119">OS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-119">PARAMETERS</span></span>

### <span data-ttu-id="f8b7f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b7f-120">-Name</span></span>
<span data-ttu-id="f8b7f-121">O nome do cluster para obter o status do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="f8b7f-121">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="f8b7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f8b7f-123">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-123">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="f8b7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b7f-124">-DefaultProfile</span></span>
<span data-ttu-id="f8b7f-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b7f-126">CommonParameters</span></span>
<span data-ttu-id="f8b7f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b7f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b7f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b7f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8b7f-129">INPUTS</span></span>

### <span data-ttu-id="f8b7f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b7f-130">System.String</span></span>

## <span data-ttu-id="f8b7f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8b7f-131">OUTPUTS</span></span>

### <span data-ttu-id="f8b7f-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="f8b7f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8b7f-133">NOTES</span></span>

## <span data-ttu-id="f8b7f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b7f-134">RELATED LINKS</span></span>

