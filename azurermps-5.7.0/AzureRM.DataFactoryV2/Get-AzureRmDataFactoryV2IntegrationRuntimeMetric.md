---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: a3ee8cdaabfc328574497f27a9b35c93992cb03b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430508"
---
# <span data-ttu-id="b5c10-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="b5c10-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="b5c10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5c10-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c10-103">Obtém dados métricos para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5c10-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5c10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5c10-104">SYNTAX</span></span>

### <span data-ttu-id="b5c10-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5c10-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c10-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c10-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c10-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b5c10-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5c10-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c10-109">O cmdlet Get-AzureRmDataFactoryV2IntegrationRuntimeMetric obtém dados métricos sobre o tempo de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b5c10-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="b5c10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5c10-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c10-111">Exemplo 1: obter métrica de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="b5c10-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="b5c10-112">Esse comando exibe dados métricos sobre o tempo de execução de integração chamado ' test-selfhost-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="b5c10-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="b5c10-113">OS</span><span class="sxs-lookup"><span data-stu-id="b5c10-113">PARAMETERS</span></span>

### <span data-ttu-id="b5c10-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b5c10-114">-DataFactoryName</span></span>
<span data-ttu-id="b5c10-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="b5c10-115">The data factory name.</span></span>

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

### <span data-ttu-id="b5c10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c10-116">-DefaultProfile</span></span>
<span data-ttu-id="b5c10-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c10-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5c10-118">-InputObject</span></span>
<span data-ttu-id="b5c10-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5c10-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="b5c10-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5c10-120">-Name</span></span>
<span data-ttu-id="b5c10-121">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="b5c10-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="b5c10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c10-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5c10-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5c10-123">The resource group name.</span></span>

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

### <span data-ttu-id="b5c10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c10-124">-ResourceId</span></span>
<span data-ttu-id="b5c10-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c10-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b5c10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c10-126">CommonParameters</span></span>
<span data-ttu-id="b5c10-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c10-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c10-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5c10-129">INPUTS</span></span>

### <span data-ttu-id="b5c10-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c10-130">System.String</span></span>
<span data-ttu-id="b5c10-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b5c10-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b5c10-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5c10-132">OUTPUTS</span></span>

### <span data-ttu-id="b5c10-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="b5c10-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="b5c10-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5c10-134">NOTES</span></span>

## <span data-ttu-id="b5c10-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5c10-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5c10-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b5c10-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

