---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261785"
---
# <span data-ttu-id="abe4b-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="abe4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="abe4b-103">Obtém informações sobre os recursos do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="abe4b-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="abe4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abe4b-104">SYNTAX</span></span>

### <span data-ttu-id="abe4b-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="abe4b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abe4b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abe4b-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abe4b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="abe4b-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abe4b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abe4b-108">DESCRIPTION</span></span>
<span data-ttu-id="abe4b-109">O cmdlet Get-AzDataFactoryV2IntegrationRuntime Obtém informações sobre os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="abe4b-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="abe4b-110">Se você especificar o nome de um tempo de execução de integração, esse cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="abe4b-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="abe4b-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="abe4b-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="abe4b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abe4b-112">EXAMPLES</span></span>

### <span data-ttu-id="abe4b-113">Exemplo 1: listar todos os tempos de execução de integração em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="abe4b-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="abe4b-114">Liste todos os tempos de execução de integração na fábrica de dados chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="abe4b-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="abe4b-115">Exemplo 2: obter tempo de execução de integração dedicada gerenciado</span><span class="sxs-lookup"><span data-stu-id="abe4b-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="abe4b-116">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="abe4b-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="abe4b-117">Exemplo 3: obter tempo de execução de integração dedicada gerenciado com status detalhado</span><span class="sxs-lookup"><span data-stu-id="abe4b-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="abe4b-118">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="abe4b-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="abe4b-119">Exemplo 4: obter o tempo de execução de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="abe4b-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="abe4b-120">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="abe4b-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="abe4b-121">Exemplo 5: obter o tempo de execução de integração de hospedagem interna com status detalhado</span><span class="sxs-lookup"><span data-stu-id="abe4b-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
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

## <span data-ttu-id="abe4b-122">OS</span><span class="sxs-lookup"><span data-stu-id="abe4b-122">PARAMETERS</span></span>

### <span data-ttu-id="abe4b-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="abe4b-123">-DataFactoryName</span></span>
<span data-ttu-id="abe4b-124">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="abe4b-124">The data factory name.</span></span>

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

### <span data-ttu-id="abe4b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe4b-125">-DefaultProfile</span></span>
<span data-ttu-id="abe4b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abe4b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe4b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abe4b-127">-InputObject</span></span>
<span data-ttu-id="abe4b-128">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="abe4b-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="abe4b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="abe4b-129">-Name</span></span>
<span data-ttu-id="abe4b-130">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="abe4b-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="abe4b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe4b-131">-ResourceGroupName</span></span>
<span data-ttu-id="abe4b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abe4b-132">The resource group name.</span></span>

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

### <span data-ttu-id="abe4b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abe4b-133">-ResourceId</span></span>
<span data-ttu-id="abe4b-134">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="abe4b-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="abe4b-135">-Status</span><span class="sxs-lookup"><span data-stu-id="abe4b-135">-Status</span></span>
<span data-ttu-id="abe4b-136">O status do detalhe do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="abe4b-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="abe4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe4b-137">CommonParameters</span></span>
<span data-ttu-id="abe4b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe4b-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe4b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe4b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abe4b-140">INPUTS</span></span>

### <span data-ttu-id="abe4b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abe4b-141">System.String</span></span>

### <span data-ttu-id="abe4b-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="abe4b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abe4b-143">OUTPUTS</span></span>

### <span data-ttu-id="abe4b-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="abe4b-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="abe4b-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="abe4b-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="abe4b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abe4b-148">NOTES</span></span>
<span data-ttu-id="abe4b-149">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="abe4b-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="abe4b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abe4b-150">RELATED LINKS</span></span>

[<span data-ttu-id="abe4b-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="abe4b-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abe4b-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
