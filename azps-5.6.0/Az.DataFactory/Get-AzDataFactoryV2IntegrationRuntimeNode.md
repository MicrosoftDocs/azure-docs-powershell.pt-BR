---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a3b3c25ce424085597de7396be469356f3d3f1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888282"
---
# <span data-ttu-id="b5110-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b5110-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="b5110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5110-102">SYNOPSIS</span></span>
<span data-ttu-id="b5110-103">Obtém informações de nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="b5110-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b5110-104">SYNTAX</span></span>

### <span data-ttu-id="b5110-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b5110-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5110-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5110-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5110-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b5110-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5110-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b5110-108">DESCRIPTION</span></span>
<span data-ttu-id="b5110-109">O cmdlet **Get-AzDataFactoryV2IntegrationRuntimeNode** obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="b5110-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5110-110">EXAMPLES</span></span>

### <span data-ttu-id="b5110-111">Exemplo 1: obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="b5110-112">O cmdlet obtém informações do nó chamado 'Node_1' no tempo de execução de integração auto-hospedado 'test-selfhost-ir' no data factory 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="b5110-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="b5110-113">Exemplo 2: obtém as informações detalhadas de um nó de tempo de execução de integração juntamente com o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="b5110-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="b5110-114">O cmdlet obtém informações do nó chamado 'Node_1' no tempo de execução de integração auto-hospedado 'test-selfhost-ir' no data factory 'test-df-eu2', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="b5110-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="b5110-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b5110-115">PARAMETERS</span></span>

### <span data-ttu-id="b5110-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b5110-116">-DataFactoryName</span></span>
<span data-ttu-id="b5110-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b5110-117">The data factory name.</span></span>

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

### <span data-ttu-id="b5110-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5110-118">-DefaultProfile</span></span>
<span data-ttu-id="b5110-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b5110-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5110-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5110-120">-InputObject</span></span>
<span data-ttu-id="b5110-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="b5110-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b5110-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b5110-123">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5110-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b5110-124">-IpAddress</span></span>
<span data-ttu-id="b5110-125">O endereço IP do nó tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="b5110-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b5110-126">-Name</span></span>
<span data-ttu-id="b5110-127">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b5110-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5110-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5110-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5110-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5110-129">The resource group name.</span></span>

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

### <span data-ttu-id="b5110-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5110-130">-ResourceId</span></span>
<span data-ttu-id="b5110-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5110-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b5110-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5110-132">CommonParameters</span></span>
<span data-ttu-id="b5110-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5110-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5110-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5110-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5110-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5110-135">INPUTS</span></span>

### <span data-ttu-id="b5110-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b5110-136">System.String</span></span>

### <span data-ttu-id="b5110-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b5110-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b5110-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b5110-138">OUTPUTS</span></span>

### <span data-ttu-id="b5110-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b5110-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="b5110-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b5110-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b5110-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="b5110-141">NOTES</span></span>
<span data-ttu-id="b5110-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="b5110-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b5110-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5110-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5110-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b5110-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
