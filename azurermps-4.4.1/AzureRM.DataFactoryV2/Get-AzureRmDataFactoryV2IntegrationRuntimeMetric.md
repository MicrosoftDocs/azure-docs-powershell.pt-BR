---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611136"
---
# <span data-ttu-id="e5b82-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="e5b82-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="e5b82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5b82-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b82-103">Obtém dados métricos para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e5b82-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5b82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5b82-104">SYNTAX</span></span>

### <span data-ttu-id="e5b82-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5b82-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="e5b82-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b82-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="e5b82-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e5b82-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="e5b82-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5b82-108">DESCRIPTION</span></span>
<span data-ttu-id="e5b82-109">O cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric obtém dados métricos sobre o tempo de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e5b82-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="e5b82-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5b82-110">EXAMPLES</span></span>

### <span data-ttu-id="e5b82-111">Exemplo 1: obter métrica de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="e5b82-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="e5b82-112">Esse comando exibe dados métricos sobre o tempo de execução de integração chamado ' test-selfhost-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="e5b82-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="e5b82-113">OS</span><span class="sxs-lookup"><span data-stu-id="e5b82-113">PARAMETERS</span></span>

### <span data-ttu-id="e5b82-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e5b82-114">-DataFactoryName</span></span>
<span data-ttu-id="e5b82-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e5b82-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b82-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b82-116">-InputObject</span></span>
<span data-ttu-id="e5b82-117">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e5b82-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b82-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5b82-118">-Name</span></span>
<span data-ttu-id="e5b82-119">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="e5b82-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b82-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5b82-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5b82-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b82-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b82-122">-ResourceId</span></span>
<span data-ttu-id="e5b82-123">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b82-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e5b82-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5b82-124">INPUTS</span></span>

### <span data-ttu-id="e5b82-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b82-125">System.String</span></span>
<span data-ttu-id="e5b82-126">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5b82-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="e5b82-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5b82-127">OUTPUTS</span></span>

### <span data-ttu-id="e5b82-128">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="e5b82-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="e5b82-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5b82-129">NOTES</span></span>

## <span data-ttu-id="e5b82-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5b82-130">RELATED LINKS</span></span>
[<span data-ttu-id="e5b82-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5b82-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

