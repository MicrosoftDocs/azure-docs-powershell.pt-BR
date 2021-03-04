---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887275"
---
# <span data-ttu-id="bfa81-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfa81-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="bfa81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa81-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa81-103">Define propriedades para um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="bfa81-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfa81-104">SYNTAX</span></span>

### <span data-ttu-id="bfa81-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bfa81-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa81-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa81-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfa81-107">DESCRIPTION</span></span>
<span data-ttu-id="bfa81-108">O Set-AzEnvironment cmdlet define pontos de extremidade e metadados para se conectar a uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="bfa81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfa81-109">EXAMPLES</span></span>

### <span data-ttu-id="bfa81-110">Exemplo 1: criar e modificar um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="bfa81-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="bfa81-111">Neste exemplo, estamos criando um novo ambiente do Azure com pontos de extremidade de exemplo usando Add-AzEnvironment e, em seguida, estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="bfa81-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="bfa81-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfa81-112">PARAMETERS</span></span>

### <span data-ttu-id="bfa81-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="bfa81-114">Especifica a autoridade base para autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bfa81-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="bfa81-116">Especifica a audiência para tokens que autenticam solicitações para pontos de extremidade do Gerenciador de Recursos do Azure ou gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="bfa81-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="bfa81-117">-AdTenant</span></span>
<span data-ttu-id="bfa81-118">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bfa81-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-119">-ARMEndpoint</span></span>
<span data-ttu-id="bfa81-120">O ponto de extremidade do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-120">The Azure Resource Manager endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="bfa81-122">O identificador de recursos do recurso serviços de análise do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="bfa81-124">O ponto de extremidade a ser usado ao se comunicar com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="bfa81-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="bfa81-126">O identificador de recurso do serviço de Atestado do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="bfa81-128">Sufixo dns do serviço de Atestado do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="bfa81-130">Sufixo dns dos serviços de catálogo e trabalho do Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bfa81-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="bfa81-132">Sufixo dns do Arquivo do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bfa81-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="bfa81-133">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="bfa81-133">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="bfa81-135">Sufixo dns do serviço do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bfa81-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="bfa81-136">Exemplo é vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="bfa81-136">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="bfa81-138">Identificador de recurso do serviço de dados do Azure Key Vault que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="bfa81-140">O ponto de extremidade a ser usado ao se comunicar com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="bfa81-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="bfa81-142">A audiência de tokens autenticando com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="bfa81-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="bfa81-144">O identificador de recurso do Azure Synapse Analytics que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="bfa81-146">Sufixo dns do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bfa81-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa81-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="bfa81-148">O identificador de recurso do serviço batch do Azure que é o destinatário do token solicitado</span><span class="sxs-lookup"><span data-stu-id="bfa81-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="bfa81-150">Sufixo do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="bfa81-151">-DataLakeAudience</span></span>
<span data-ttu-id="bfa81-152">A audiência para tokens autenticando com o Ponto de Extremidade dos serviços do AD Data Lake.</span><span class="sxs-lookup"><span data-stu-id="bfa81-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa81-153">-DefaultProfile</span></span>
<span data-ttu-id="bfa81-154">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfa81-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="bfa81-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="bfa81-156">Indica que a autenticação local dos Serviços de Federação do Active Directory (ADFS) é permitida.</span><span class="sxs-lookup"><span data-stu-id="bfa81-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-157">-GalleryEndpoint</span></span>
<span data-ttu-id="bfa81-158">Especifica o ponto de extremidade para a galeria do Gerenciador de Recursos do Azure de modelos de implantação.</span><span class="sxs-lookup"><span data-stu-id="bfa81-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="bfa81-159">-GraphAudience</span></span>
<span data-ttu-id="bfa81-160">A audiência para tokens autenticando com o Ponto de Extremidade do AD Graph.</span><span class="sxs-lookup"><span data-stu-id="bfa81-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-161">-GraphEndpoint</span></span>
<span data-ttu-id="bfa81-162">Especifica a URL para solicitações do Graph (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="bfa81-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="bfa81-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="bfa81-164">Especifica a URL do Portal de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bfa81-164">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-165">-Name</span><span class="sxs-lookup"><span data-stu-id="bfa81-165">-Name</span></span>
<span data-ttu-id="bfa81-166">Especifica o nome do ambiente a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-166">Specifies the name of the environment to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="bfa81-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="bfa81-168">Especifica a URL da qual os arquivos .publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="bfa81-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="bfa81-170">Especifica a URL para solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-170">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="bfa81-171">-Scope</span></span>
<span data-ttu-id="bfa81-172">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="bfa81-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-173">-ServiceEndpoint</span></span>
<span data-ttu-id="bfa81-174">Especifica o ponto de extremidade para solicitações de Gerenciamento de Serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="bfa81-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="bfa81-176">Especifica o sufixo de nome de domínio para servidores de banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfa81-177">-StorageEndpoint</span></span>
<span data-ttu-id="bfa81-178">Especifica o ponto de extremidade para o acesso de armazenamento (blob, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="bfa81-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfa81-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="bfa81-180">Especifica o sufixo de nome de domínio para os serviços do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa81-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa81-181">-Confirm</span></span>
<span data-ttu-id="bfa81-182">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa81-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa81-183">-WhatIf</span></span>
<span data-ttu-id="bfa81-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfa81-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfa81-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa81-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa81-186">CommonParameters</span></span>
<span data-ttu-id="bfa81-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa81-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa81-188">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfa81-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa81-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa81-189">INPUTS</span></span>

### <span data-ttu-id="bfa81-190">System.String</span><span class="sxs-lookup"><span data-stu-id="bfa81-190">System.String</span></span>

### <span data-ttu-id="bfa81-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfa81-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfa81-192">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfa81-192">OUTPUTS</span></span>

### <span data-ttu-id="bfa81-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfa81-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="bfa81-194">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfa81-194">NOTES</span></span>

## <span data-ttu-id="bfa81-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfa81-195">RELATED LINKS</span></span>

[<span data-ttu-id="bfa81-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfa81-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="bfa81-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfa81-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="bfa81-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfa81-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

