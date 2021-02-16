---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113286"
---
# <span data-ttu-id="ad7bd-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ad7bd-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ad7bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7bd-103">Obtém informações de nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="ad7bd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad7bd-104">SYNTAX</span></span>

### <span data-ttu-id="ad7bd-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad7bd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad7bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad7bd-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad7bd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ad7bd-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad7bd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad7bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ad7bd-109">O cmdlet **Get-AzDataFactoryV2IntegrationRuntimeNode** obtém as informações de detalhes de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="ad7bd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad7bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ad7bd-111">Exemplo 1: Obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="ad7bd-112">O cmdlet obtém informações do nó chamado "Node_1" em tempo de execução de integração hospedada auto-hospedado 'test-selfhost-ir' no data factory 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="ad7bd-113">Exemplo 2: Obtém as informações detalhadas de um nó de tempo de execução de integração com o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="ad7bd-114">O cmdlet obtém informações do nó chamado "Node_1" em tempo de execução de integração hospedada auto-hospedado 'test-selfhost-ir' no data factory 'test-df-eu2', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="ad7bd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad7bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ad7bd-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ad7bd-116">-DataFactoryName</span></span>
<span data-ttu-id="ad7bd-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-117">The data factory name.</span></span>

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

### <span data-ttu-id="ad7bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7bd-118">-DefaultProfile</span></span>
<span data-ttu-id="ad7bd-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad7bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad7bd-120">-InputObject</span></span>
<span data-ttu-id="ad7bd-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="ad7bd-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ad7bd-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ad7bd-123">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="ad7bd-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ad7bd-124">-IpAddress</span></span>
<span data-ttu-id="ad7bd-125">O Endereço IP do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="ad7bd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad7bd-126">-Name</span></span>
<span data-ttu-id="ad7bd-127">O nome do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="ad7bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad7bd-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-129">The resource group name.</span></span>

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

### <span data-ttu-id="ad7bd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad7bd-130">-ResourceId</span></span>
<span data-ttu-id="ad7bd-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ad7bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7bd-132">CommonParameters</span></span>
<span data-ttu-id="ad7bd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7bd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7bd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7bd-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad7bd-135">INPUTS</span></span>

### <span data-ttu-id="ad7bd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ad7bd-136">System.String</span></span>

### <span data-ttu-id="ad7bd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ad7bd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ad7bd-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad7bd-138">OUTPUTS</span></span>

### <span data-ttu-id="ad7bd-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ad7bd-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="ad7bd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ad7bd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ad7bd-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ad7bd-141">NOTES</span></span>
<span data-ttu-id="ad7bd-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, keyword, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="ad7bd-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ad7bd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad7bd-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad7bd-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ad7bd-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
