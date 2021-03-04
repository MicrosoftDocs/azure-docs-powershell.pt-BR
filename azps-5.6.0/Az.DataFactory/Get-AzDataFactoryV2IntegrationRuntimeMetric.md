---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888292"
---
# <span data-ttu-id="10942-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="10942-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="10942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10942-102">SYNOPSIS</span></span>
<span data-ttu-id="10942-103">Obtém dados métricos para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="10942-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="10942-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10942-104">SYNTAX</span></span>

### <span data-ttu-id="10942-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10942-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10942-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10942-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10942-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="10942-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10942-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10942-108">DESCRIPTION</span></span>
<span data-ttu-id="10942-109">O Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet obtém dados métricos sobre o tempo de execução de integração em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="10942-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="10942-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10942-110">EXAMPLES</span></span>

### <span data-ttu-id="10942-111">Exemplo 1: Obter métrica de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="10942-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="10942-112">Este comando exibe dados métricos sobre o tempo de execução de integração chamado 'test-selfhost-ir' na assinatura do grupo de recursos chamado 'rg-test-dfv2' e no data factory denominado 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="10942-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="10942-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10942-113">PARAMETERS</span></span>

### <span data-ttu-id="10942-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10942-114">-DataFactoryName</span></span>
<span data-ttu-id="10942-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="10942-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10942-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10942-116">-DefaultProfile</span></span>
<span data-ttu-id="10942-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="10942-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10942-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10942-118">-InputObject</span></span>
<span data-ttu-id="10942-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="10942-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10942-120">-Name</span><span class="sxs-lookup"><span data-stu-id="10942-120">-Name</span></span>
<span data-ttu-id="10942-121">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="10942-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10942-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10942-122">-ResourceGroupName</span></span>
<span data-ttu-id="10942-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10942-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10942-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10942-124">-ResourceId</span></span>
<span data-ttu-id="10942-125">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="10942-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10942-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10942-126">CommonParameters</span></span>
<span data-ttu-id="10942-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10942-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10942-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10942-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10942-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10942-129">INPUTS</span></span>

### <span data-ttu-id="10942-130">System.String</span><span class="sxs-lookup"><span data-stu-id="10942-130">System.String</span></span>

### <span data-ttu-id="10942-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10942-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="10942-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10942-132">OUTPUTS</span></span>

### <span data-ttu-id="10942-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="10942-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="10942-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="10942-134">NOTES</span></span>

## <span data-ttu-id="10942-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10942-135">RELATED LINKS</span></span>

[<span data-ttu-id="10942-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10942-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

