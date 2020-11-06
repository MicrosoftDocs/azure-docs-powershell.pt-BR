---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: ef5b99a27c547ec1e71c2339de8f4c9536549981
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441133"
---
# <span data-ttu-id="1aeee-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aeee-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1aeee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aeee-102">SYNOPSIS</span></span>
<span data-ttu-id="1aeee-103">Obtém informações sobre os recursos do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1aeee-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aeee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aeee-104">SYNTAX</span></span>

### <span data-ttu-id="1aeee-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1aeee-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="1aeee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1aeee-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
```

### <span data-ttu-id="1aeee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1aeee-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="1aeee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1aeee-108">DESCRIPTION</span></span>
<span data-ttu-id="1aeee-109">O cmdlet Get-AzureRmDataFactoryV2IntegrationRuntime Obtém informações sobre os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1aeee-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="1aeee-110">Se você especificar o nome de um tempo de execução de integração, esse cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1aeee-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="1aeee-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1aeee-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="1aeee-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aeee-112">EXAMPLES</span></span>

### <span data-ttu-id="1aeee-113">Exemplo 1: listar todos os tempos de execução de integração em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="1aeee-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="1aeee-114">Liste todos os tempos de execução de integração na fábrica de dados chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="1aeee-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1aeee-115">Exemplo 2: obter tempo de execução de integração dedicada gerenciado</span><span class="sxs-lookup"><span data-stu-id="1aeee-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="1aeee-116">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="1aeee-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1aeee-117">Exemplo 3: obter tempo de execução de integração dedicada gerenciado com status detalhado</span><span class="sxs-lookup"><span data-stu-id="1aeee-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="1aeee-118">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="1aeee-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="1aeee-119">Exemplo 4: obter o tempo de execução de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="1aeee-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="1aeee-120">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="1aeee-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="1aeee-121">OS</span><span class="sxs-lookup"><span data-stu-id="1aeee-121">PARAMETERS</span></span>

### <span data-ttu-id="1aeee-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1aeee-122">-DataFactoryName</span></span>
<span data-ttu-id="1aeee-123">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="1aeee-123">The data factory name.</span></span>

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

### <span data-ttu-id="1aeee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aeee-124">-InputObject</span></span>
<span data-ttu-id="1aeee-125">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1aeee-125">The integration runtime object.</span></span>

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

### <span data-ttu-id="1aeee-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aeee-126">-Name</span></span>
<span data-ttu-id="1aeee-127">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="1aeee-127">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aeee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aeee-128">-ResourceGroupName</span></span>
<span data-ttu-id="1aeee-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aeee-129">The resource group name.</span></span>

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

### <span data-ttu-id="1aeee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aeee-130">-ResourceId</span></span>
<span data-ttu-id="1aeee-131">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1aeee-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1aeee-132">-Status</span><span class="sxs-lookup"><span data-stu-id="1aeee-132">-Status</span></span>
<span data-ttu-id="1aeee-133">O status do detalhe do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="1aeee-133">The integration runtime detail status.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1aeee-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1aeee-134">INPUTS</span></span>

### <span data-ttu-id="1aeee-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1aeee-135">System.String</span></span>
<span data-ttu-id="1aeee-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aeee-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="1aeee-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1aeee-137">OUTPUTS</span></span>

### <span data-ttu-id="1aeee-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1aeee-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1aeee-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aeee-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>


## <span data-ttu-id="1aeee-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1aeee-140">NOTES</span></span>
<span data-ttu-id="1aeee-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="1aeee-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1aeee-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aeee-142">RELATED LINKS</span></span>
[<span data-ttu-id="1aeee-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aeee-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1aeee-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1aeee-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
