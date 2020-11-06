---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 83e6de07f7796e49732a35cfea4573002e6208df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432016"
---
# <span data-ttu-id="4d56a-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4d56a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d56a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d56a-103">Obtém informações sobre os recursos do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4d56a-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d56a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d56a-104">SYNTAX</span></span>

### <span data-ttu-id="4d56a-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d56a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d56a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d56a-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d56a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d56a-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d56a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d56a-108">DESCRIPTION</span></span>
<span data-ttu-id="4d56a-109">O cmdlet Get-AzureRmDataFactoryV2IntegrationRuntime Obtém informações sobre os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4d56a-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="4d56a-110">Se você especificar o nome de um tempo de execução de integração, esse cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4d56a-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="4d56a-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4d56a-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="4d56a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d56a-112">EXAMPLES</span></span>

### <span data-ttu-id="4d56a-113">Exemplo 1: listar todos os tempos de execução de integração em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="4d56a-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="4d56a-114">Liste todos os tempos de execução de integração na fábrica de dados chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="4d56a-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4d56a-115">Exemplo 2: obter tempo de execução de integração dedicada gerenciado</span><span class="sxs-lookup"><span data-stu-id="4d56a-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="4d56a-116">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="4d56a-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4d56a-117">Exemplo 3: obter tempo de execução de integração dedicada gerenciado com status detalhado</span><span class="sxs-lookup"><span data-stu-id="4d56a-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="4d56a-118">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="4d56a-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4d56a-119">Exemplo 4: obter o tempo de execução de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="4d56a-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="4d56a-120">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="4d56a-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="4d56a-121">OS</span><span class="sxs-lookup"><span data-stu-id="4d56a-121">PARAMETERS</span></span>

### <span data-ttu-id="4d56a-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4d56a-122">-DataFactoryName</span></span>
<span data-ttu-id="4d56a-123">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4d56a-123">The data factory name.</span></span>

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

### <span data-ttu-id="4d56a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d56a-124">-DefaultProfile</span></span>
<span data-ttu-id="4d56a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d56a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d56a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d56a-126">-InputObject</span></span>
<span data-ttu-id="4d56a-127">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4d56a-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="4d56a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d56a-128">-Name</span></span>
<span data-ttu-id="4d56a-129">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="4d56a-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d56a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d56a-130">-ResourceGroupName</span></span>
<span data-ttu-id="4d56a-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d56a-131">The resource group name.</span></span>

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

### <span data-ttu-id="4d56a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d56a-132">-ResourceId</span></span>
<span data-ttu-id="4d56a-133">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d56a-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4d56a-134">-Status</span><span class="sxs-lookup"><span data-stu-id="4d56a-134">-Status</span></span>
<span data-ttu-id="4d56a-135">O status do detalhe do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4d56a-135">The integration runtime detail status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d56a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d56a-136">CommonParameters</span></span>
<span data-ttu-id="4d56a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d56a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d56a-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d56a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d56a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d56a-139">INPUTS</span></span>

### <span data-ttu-id="4d56a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4d56a-140">System.String</span></span>

### <span data-ttu-id="4d56a-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="4d56a-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d56a-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4d56a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d56a-143">OUTPUTS</span></span>

### <span data-ttu-id="4d56a-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="4d56a-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="4d56a-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="4d56a-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="4d56a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d56a-148">NOTES</span></span>
<span data-ttu-id="4d56a-149">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="4d56a-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4d56a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d56a-150">RELATED LINKS</span></span>

[<span data-ttu-id="4d56a-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4d56a-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d56a-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
