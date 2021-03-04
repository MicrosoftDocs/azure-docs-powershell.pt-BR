---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5997ca072ae11407500ceb254dbd16be13382ac8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888294"
---
# <span data-ttu-id="32d73-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="32d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d73-102">SYNOPSIS</span></span>
<span data-ttu-id="32d73-103">Obtém informações sobre recursos de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="32d73-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="32d73-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32d73-104">SYNTAX</span></span>

### <span data-ttu-id="32d73-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32d73-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="32d73-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d73-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="32d73-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d73-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32d73-108">DESCRIPTION</span></span>
<span data-ttu-id="32d73-109">O Get-AzDataFactoryV2IntegrationRuntime cmdlet obtém informações sobre tempos de execução de integração em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="32d73-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="32d73-110">Se você especificar o nome de um tempo de execução de integração, este cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="32d73-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="32d73-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="32d73-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="32d73-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32d73-112">EXAMPLES</span></span>

### <span data-ttu-id="32d73-113">Exemplo 1: listar todos os tempos de execução de integração em um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="32d73-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="32d73-114">Listar todos os tempos de execução de integração no fábrica de dados chamado 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="32d73-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32d73-115">Exemplo 2: Obter tempo de execução de integração dedicado gerenciado</span><span class="sxs-lookup"><span data-stu-id="32d73-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="32d73-116">Este comando exibe informações sobre o tempo de execução de integração chamado 'test-dedicated-ir' na assinatura do grupo de recursos chamado 'rg-test-dfv2' e no data factory denominado 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="32d73-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32d73-117">Exemplo 3: Obter tempo de execução de integração dedicada gerenciada com status de detalhes</span><span class="sxs-lookup"><span data-stu-id="32d73-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="32d73-118">Este comando exibe informações sobre o tempo de execução de integração chamado 'test-dedicated-ir' na assinatura do grupo de recursos chamado 'rg-test-dfv2' e no data factory denominado 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="32d73-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32d73-119">Exemplo 4: obter tempo de execução de integração auto-hospedado</span><span class="sxs-lookup"><span data-stu-id="32d73-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="32d73-120">Este comando exibe informações sobre o tempo de execução de integração chamado 'test-dedicated-ir' na assinatura do grupo de recursos chamado 'rg-test-dfv2' e no data factory denominado 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="32d73-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="32d73-121">Exemplo 5: Obter tempo de execução de integração auto-hospedado com status de detalhes</span><span class="sxs-lookup"><span data-stu-id="32d73-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="32d73-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32d73-122">PARAMETERS</span></span>

### <span data-ttu-id="32d73-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="32d73-123">-DataFactoryName</span></span>
<span data-ttu-id="32d73-124">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="32d73-124">The data factory name.</span></span>

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

### <span data-ttu-id="32d73-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d73-125">-DefaultProfile</span></span>
<span data-ttu-id="32d73-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32d73-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d73-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32d73-127">-InputObject</span></span>
<span data-ttu-id="32d73-128">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="32d73-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="32d73-129">-Name</span><span class="sxs-lookup"><span data-stu-id="32d73-129">-Name</span></span>
<span data-ttu-id="32d73-130">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="32d73-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="32d73-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d73-131">-ResourceGroupName</span></span>
<span data-ttu-id="32d73-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32d73-132">The resource group name.</span></span>

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

### <span data-ttu-id="32d73-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32d73-133">-ResourceId</span></span>
<span data-ttu-id="32d73-134">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="32d73-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="32d73-135">-Status</span><span class="sxs-lookup"><span data-stu-id="32d73-135">-Status</span></span>
<span data-ttu-id="32d73-136">O status de detalhes do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="32d73-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="32d73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d73-137">CommonParameters</span></span>
<span data-ttu-id="32d73-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d73-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d73-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d73-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32d73-140">INPUTS</span></span>

### <span data-ttu-id="32d73-141">System.String</span><span class="sxs-lookup"><span data-stu-id="32d73-141">System.String</span></span>

### <span data-ttu-id="32d73-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="32d73-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32d73-143">OUTPUTS</span></span>

### <span data-ttu-id="32d73-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="32d73-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="32d73-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="32d73-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="32d73-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="32d73-148">NOTES</span></span>
<span data-ttu-id="32d73-149">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="32d73-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="32d73-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32d73-150">RELATED LINKS</span></span>

[<span data-ttu-id="32d73-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="32d73-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="32d73-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
