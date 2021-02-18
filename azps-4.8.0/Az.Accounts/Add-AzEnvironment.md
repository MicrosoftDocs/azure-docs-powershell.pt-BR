---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 2db2e90dc1292bdfe67907e5a180b08a09a54718
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406002"
---
# <span data-ttu-id="a1b91-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1b91-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="a1b91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1b91-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b91-103">Adiciona pontos de extremidade e metadados para uma instância do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="a1b91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1b91-104">SYNTAX</span></span>

### <span data-ttu-id="a1b91-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1b91-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b91-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b91-107">Descoberta</span><span class="sxs-lookup"><span data-stu-id="a1b91-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b91-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1b91-108">DESCRIPTION</span></span>
<span data-ttu-id="a1b91-109">O cmdlet Add-AzEnvironment adiciona pontos de extremidade e metadados para permitir que cmdlets do Gerenciador de Recursos do Azure se conectem a uma nova instância do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="a1b91-110">Os ambientes integrados do AzureCloud e do AzureChinaCloud visam instâncias públicas existentes do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a1b91-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="a1b91-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1b91-111">EXAMPLES</span></span>

### <span data-ttu-id="a1b91-112">Exemplo 1: criar e modificar um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="a1b91-112">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
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
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="a1b91-113">Neste exemplo, estamos criando um novo ambiente do Azure com pontos de extremidade de exemplo usando o Add-AzEnvironment e, em seguida, estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="a1b91-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="a1b91-114">Exemplo 2: descobrir um novo ambiente por meio do Uri</span><span class="sxs-lookup"><span data-stu-id="a1b91-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="a1b91-115">Neste exemplo, estamos descobrindo um novo ambiente do Azure a partir do `https://configuredmetadata.net` Uri.</span><span class="sxs-lookup"><span data-stu-id="a1b91-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="a1b91-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1b91-116">PARAMETERS</span></span>

### <span data-ttu-id="a1b91-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="a1b91-118">Especifica a autoridade base para autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1b91-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="a1b91-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="a1b91-120">Especifica a audiência para tokens que autenticam solicitações para pontos de extremidade do Azure Resource Manager ou RDFE (Gerenciamento de Serviços).</span><span class="sxs-lookup"><span data-stu-id="a1b91-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="a1b91-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="a1b91-121">-AdTenant</span></span>
<span data-ttu-id="a1b91-122">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1b91-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="a1b91-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-123">-ARMEndpoint</span></span>
<span data-ttu-id="a1b91-124">O ponto de extremidade do Gerenciador de Recursos do Azure</span><span class="sxs-lookup"><span data-stu-id="a1b91-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="a1b91-125">-Descoberta Automática</span><span class="sxs-lookup"><span data-stu-id="a1b91-125">-AutoDiscover</span></span>
<span data-ttu-id="a1b91-126">Descobre ambientes por padrão ou ponto de extremidade configurado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="a1b91-128">O identificador de recursos do recurso do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="a1b91-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="a1b91-130">O ponto de extremidade a ser usado ao se comunicar com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1b91-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="a1b91-132">O identificador de recurso do serviço Azure Attestation que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="a1b91-134">Sufixo DNS do serviço Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="a1b91-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="a1b91-136">Sufixo DNS dos serviços de trabalho e catálogo do Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a1b91-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="a1b91-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="a1b91-138">Sufixo DNS do FileSystem do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1b91-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="a1b91-139">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="a1b91-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="a1b91-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="a1b91-141">Sufixo DNS do serviço Cofre de Chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="a1b91-142">Exemplo é vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="a1b91-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="a1b91-144">Identificador de recurso do serviço de dados do Cofre de Chaves do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="a1b91-146">O ponto de extremidade a ser usado ao se comunicar com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1b91-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="a1b91-148">A audiência de tokens autenticando com a API do Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1b91-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="a1b91-150">O identificador de recurso da Análise Synapse do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="a1b91-152">Sufixo DNS do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1b91-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b91-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="a1b91-154">O identificador de recurso do serviço Lote do Azure que é o destinatário do token solicitado</span><span class="sxs-lookup"><span data-stu-id="a1b91-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="a1b91-155">-DataLakeAudience</span></span>
<span data-ttu-id="a1b91-156">A audiência para tokens autenticando com o ponto de extremidade do AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="a1b91-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b91-157">-DefaultProfile</span></span>
<span data-ttu-id="a1b91-158">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a1b91-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1b91-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a1b91-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="a1b91-160">Indica que a autenticação local dos Serviços de Federação do Active Directory (ADFS) é permitida.</span><span class="sxs-lookup"><span data-stu-id="a1b91-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="a1b91-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-161">-GalleryEndpoint</span></span>
<span data-ttu-id="a1b91-162">Especifica o ponto de extremidade da galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a1b91-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="a1b91-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="a1b91-163">-GraphAudience</span></span>
<span data-ttu-id="a1b91-164">A audiência para tokens autenticando com o Ponto de Extremidade do AD Graph.</span><span class="sxs-lookup"><span data-stu-id="a1b91-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="a1b91-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-165">-GraphEndpoint</span></span>
<span data-ttu-id="a1b91-166">Especifica a URL das solicitações de Graph (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="a1b91-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="a1b91-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="a1b91-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="a1b91-168">Especifica a URL do Portal de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="a1b91-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="a1b91-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b91-169">-Name</span></span>
<span data-ttu-id="a1b91-170">Especifica o nome do ambiente a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-170">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="a1b91-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="a1b91-172">Especifica a URL a partir da qual os arquivos .publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="a1b91-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="a1b91-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="a1b91-174">Especifica a URL das solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="a1b91-175">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a1b91-175">-Scope</span></span>
<span data-ttu-id="a1b91-176">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a1b91-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a1b91-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-177">-ServiceEndpoint</span></span>
<span data-ttu-id="a1b91-178">Especifica o ponto de extremidade para solicitações de Gerenciamento de Serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="a1b91-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="a1b91-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="a1b91-180">Especifica o sufixo de nome de domínio para servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="a1b91-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1b91-181">-StorageEndpoint</span></span>
<span data-ttu-id="a1b91-182">Especifica o ponto de extremidade para acesso de armazenamento (blob, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="a1b91-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a1b91-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="a1b91-184">Especifica o sufixo de nome de domínio para os serviços do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b91-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="a1b91-185">-Uri</span><span class="sxs-lookup"><span data-stu-id="a1b91-185">-Uri</span></span>
<span data-ttu-id="a1b91-186">Especifica o URI do recurso da Internet para buscar ambientes.</span><span class="sxs-lookup"><span data-stu-id="a1b91-186">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b91-187">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1b91-187">-Confirm</span></span>
<span data-ttu-id="a1b91-188">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b91-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b91-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b91-189">-WhatIf</span></span>
<span data-ttu-id="a1b91-190">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1b91-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1b91-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b91-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b91-192">CommonParameters</span></span>
<span data-ttu-id="a1b91-193">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b91-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b91-194">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1b91-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b91-195">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1b91-195">INPUTS</span></span>

### <span data-ttu-id="a1b91-196">System.String</span><span class="sxs-lookup"><span data-stu-id="a1b91-196">System.String</span></span>

### <span data-ttu-id="a1b91-197">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1b91-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1b91-198">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1b91-198">OUTPUTS</span></span>

### <span data-ttu-id="a1b91-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1b91-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a1b91-200">Notas</span><span class="sxs-lookup"><span data-stu-id="a1b91-200">NOTES</span></span>

## <span data-ttu-id="a1b91-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1b91-201">RELATED LINKS</span></span>

[<span data-ttu-id="a1b91-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1b91-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="a1b91-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1b91-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="a1b91-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a1b91-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

