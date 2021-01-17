---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429909"
---
# <span data-ttu-id="2f81c-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="2f81c-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="2f81c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f81c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f81c-103">Obtém dados métricos para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2f81c-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="2f81c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f81c-104">SYNTAX</span></span>

### <span data-ttu-id="2f81c-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f81c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f81c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f81c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f81c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2f81c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f81c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f81c-108">DESCRIPTION</span></span>
<span data-ttu-id="2f81c-109">O cmdlet Get-AzDataFactoryV2IntegrationRuntimeMetric obtém dados métricos sobre o tempo de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2f81c-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="2f81c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f81c-110">EXAMPLES</span></span>

### <span data-ttu-id="2f81c-111">Exemplo 1: obter métrica de tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="2f81c-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="2f81c-112">Esse comando exibe dados métricos sobre o tempo de execução de integração chamado ' test-selfhost-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="2f81c-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="2f81c-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f81c-113">PARAMETERS</span></span>

### <span data-ttu-id="2f81c-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2f81c-114">-DataFactoryName</span></span>
<span data-ttu-id="2f81c-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="2f81c-115">The data factory name.</span></span>

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

### <span data-ttu-id="2f81c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f81c-116">-DefaultProfile</span></span>
<span data-ttu-id="2f81c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f81c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f81c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f81c-118">-InputObject</span></span>
<span data-ttu-id="2f81c-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2f81c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="2f81c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f81c-120">-Name</span></span>
<span data-ttu-id="2f81c-121">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="2f81c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="2f81c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f81c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f81c-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f81c-123">The resource group name.</span></span>

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

### <span data-ttu-id="2f81c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f81c-124">-ResourceId</span></span>
<span data-ttu-id="2f81c-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f81c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2f81c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f81c-126">CommonParameters</span></span>
<span data-ttu-id="2f81c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f81c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f81c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f81c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f81c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f81c-129">INPUTS</span></span>

### <span data-ttu-id="2f81c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f81c-130">System.String</span></span>

### <span data-ttu-id="2f81c-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f81c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2f81c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f81c-132">OUTPUTS</span></span>

### <span data-ttu-id="2f81c-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="2f81c-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="2f81c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f81c-134">NOTES</span></span>

## <span data-ttu-id="2f81c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f81c-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f81c-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f81c-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

