---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258322"
---
# <span data-ttu-id="52915-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="52915-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="52915-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52915-102">SYNOPSIS</span></span>
<span data-ttu-id="52915-103">Obtém informações sobre o nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="52915-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52915-104">SYNTAX</span></span>

### <span data-ttu-id="52915-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="52915-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52915-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="52915-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52915-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="52915-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52915-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52915-108">DESCRIPTION</span></span>
<span data-ttu-id="52915-109">O cmdlet **Get-AzDataFactoryV2IntegrationRuntimeNode** Obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="52915-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52915-110">EXAMPLES</span></span>

### <span data-ttu-id="52915-111">Exemplo 1: Obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="52915-112">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' na fábrica de dados ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="52915-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="52915-113">Exemplo 2: Obtém as informações detalhadas de um nó de tempo de execução de integração juntamente com o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="52915-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="52915-114">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' na fábrica de dados ' test-DF-EU2 ', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="52915-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="52915-115">OS</span><span class="sxs-lookup"><span data-stu-id="52915-115">PARAMETERS</span></span>

### <span data-ttu-id="52915-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="52915-116">-DataFactoryName</span></span>
<span data-ttu-id="52915-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="52915-117">The data factory name.</span></span>

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

### <span data-ttu-id="52915-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52915-118">-DefaultProfile</span></span>
<span data-ttu-id="52915-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52915-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52915-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52915-120">-InputObject</span></span>
<span data-ttu-id="52915-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="52915-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="52915-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="52915-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="52915-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="52915-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="52915-124">-IpAddress</span></span>
<span data-ttu-id="52915-125">O endereço IP do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="52915-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="52915-126">-Name</span></span>
<span data-ttu-id="52915-127">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="52915-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="52915-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52915-128">-ResourceGroupName</span></span>
<span data-ttu-id="52915-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52915-129">The resource group name.</span></span>

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

### <span data-ttu-id="52915-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52915-130">-ResourceId</span></span>
<span data-ttu-id="52915-131">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="52915-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="52915-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52915-132">CommonParameters</span></span>
<span data-ttu-id="52915-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52915-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52915-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52915-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52915-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52915-135">INPUTS</span></span>

### <span data-ttu-id="52915-136">System. String</span><span class="sxs-lookup"><span data-stu-id="52915-136">System.String</span></span>

### <span data-ttu-id="52915-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="52915-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="52915-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52915-138">OUTPUTS</span></span>

### <span data-ttu-id="52915-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="52915-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="52915-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="52915-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="52915-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52915-141">NOTES</span></span>
<span data-ttu-id="52915-142">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="52915-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="52915-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52915-143">RELATED LINKS</span></span>

[<span data-ttu-id="52915-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="52915-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
