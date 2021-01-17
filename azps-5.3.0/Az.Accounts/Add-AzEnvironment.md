---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429079"
---
# <span data-ttu-id="3c3ae-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c3ae-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="3c3ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3c3ae-103">Adiciona pontos de extremidade e metadados para uma instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="3c3ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c3ae-104">SYNTAX</span></span>

### <span data-ttu-id="3c3ae-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c3ae-105">Name (Default)</span></span>
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
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c3ae-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c3ae-107">Descobertas</span><span class="sxs-lookup"><span data-stu-id="3c3ae-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c3ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c3ae-108">DESCRIPTION</span></span>
<span data-ttu-id="3c3ae-109">O cmdlet Add-AzEnvironment adiciona pontos de extremidade e metadados para habilitar cmdlets do Azure Resource Manager para se conectar a uma nova instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="3c3ae-110">Os ambientes internos AzureCloud e AzureChinaCloud direcionam as instâncias públicas existentes do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="3c3ae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c3ae-111">EXAMPLES</span></span>

### <span data-ttu-id="3c3ae-112">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="3c3ae-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="3c3ae-113">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="3c3ae-114">Exemplo 2: descobrindo um novo ambiente via URI</span><span class="sxs-lookup"><span data-stu-id="3c3ae-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="3c3ae-115">Neste exemplo, estamos descobrindo um novo ambiente do Azure do `https://configuredmetadata.net` URI.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="3c3ae-116">OS</span><span class="sxs-lookup"><span data-stu-id="3c3ae-116">PARAMETERS</span></span>

### <span data-ttu-id="3c3ae-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3c3ae-118">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3c3ae-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-120">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="3c3ae-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3c3ae-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3c3ae-121">-AdTenant</span></span>
<span data-ttu-id="3c3ae-122">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3c3ae-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-123">-ARMEndpoint</span></span>
<span data-ttu-id="3c3ae-124">O ponto de extremidade do Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="3c3ae-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="3c3ae-125">-Descoberta automática</span><span class="sxs-lookup"><span data-stu-id="3c3ae-125">-AutoDiscover</span></span>
<span data-ttu-id="3c3ae-126">Descobre ambientes por meio de um ponto de extremidade padrão ou configurado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="3c3ae-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-128">O identificador de recurso do recurso do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="3c3ae-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-130">O ponto de extremidade a ser usado ao se comunicar com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="3c3ae-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-132">O identificador de recurso do serviço de atestado do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="3c3ae-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-134">Sufixo DNS do serviço de atestado do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="3c3ae-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-136">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3c3ae-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3c3ae-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-138">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="3c3ae-139">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3c3ae-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3c3ae-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3c3ae-141">Sufixo DNS do serviço de compartimento de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="3c3ae-142">Exemplo é vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="3c3ae-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="3c3ae-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-144">Identificador de recurso do serviço de dados de compartimento de chave do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="3c3ae-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="3c3ae-146">O ponto de extremidade a ser usado ao se comunicar com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="3c3ae-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-148">A audiência para tokens de autenticação com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="3c3ae-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-150">O identificador de recurso da análise do Azure Synapse que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="3c3ae-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-152">Sufixo DNS da análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="3c3ae-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c3ae-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="3c3ae-154">O identificador de recurso do serviço de lote do Azure que é o destinatário do token solicitado</span><span class="sxs-lookup"><span data-stu-id="3c3ae-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="3c3ae-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="3c3ae-156">Sufixo do registro do contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-156">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="3c3ae-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3c3ae-157">-DataLakeAudience</span></span>
<span data-ttu-id="3c3ae-158">A audiência para tokens de autenticação com o ponto de extremidade de serviços de data Lake do AD.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3c3ae-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c3ae-159">-DefaultProfile</span></span>
<span data-ttu-id="3c3ae-160">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3c3ae-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c3ae-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c3ae-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3c3ae-162">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3c3ae-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-163">-GalleryEndpoint</span></span>
<span data-ttu-id="3c3ae-164">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3c3ae-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="3c3ae-165">-GraphAudience</span></span>
<span data-ttu-id="3c3ae-166">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3c3ae-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-167">-GraphEndpoint</span></span>
<span data-ttu-id="3c3ae-168">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="3c3ae-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3c3ae-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3c3ae-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="3c3ae-170">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-170">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3c3ae-171">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c3ae-171">-Name</span></span>
<span data-ttu-id="3c3ae-172">Especifica o nome do ambiente a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-172">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="3c3ae-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3c3ae-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3c3ae-174">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3c3ae-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3c3ae-176">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-176">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3c3ae-177">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3c3ae-177">-Scope</span></span>
<span data-ttu-id="3c3ae-178">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3c3ae-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-179">-ServiceEndpoint</span></span>
<span data-ttu-id="3c3ae-180">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3c3ae-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3c3ae-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3c3ae-182">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3c3ae-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c3ae-183">-StorageEndpoint</span></span>
<span data-ttu-id="3c3ae-184">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="3c3ae-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3c3ae-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c3ae-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3c3ae-186">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3c3ae-187">-URI</span><span class="sxs-lookup"><span data-stu-id="3c3ae-187">-Uri</span></span>
<span data-ttu-id="3c3ae-188">Especifica o URI do recurso de Internet para buscar ambientes.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-188">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="3c3ae-189">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c3ae-189">-Confirm</span></span>
<span data-ttu-id="3c3ae-190">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c3ae-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c3ae-191">-WhatIf</span></span>
<span data-ttu-id="3c3ae-192">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c3ae-193">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c3ae-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c3ae-194">CommonParameters</span></span>
<span data-ttu-id="3c3ae-195">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c3ae-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c3ae-196">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c3ae-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c3ae-197">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c3ae-197">INPUTS</span></span>

### <span data-ttu-id="3c3ae-198">System. String</span><span class="sxs-lookup"><span data-stu-id="3c3ae-198">System.String</span></span>

### <span data-ttu-id="3c3ae-199">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c3ae-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c3ae-200">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c3ae-200">OUTPUTS</span></span>

### <span data-ttu-id="3c3ae-201">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c3ae-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="3c3ae-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c3ae-202">NOTES</span></span>

## <span data-ttu-id="3c3ae-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c3ae-203">RELATED LINKS</span></span>

[<span data-ttu-id="3c3ae-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c3ae-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="3c3ae-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c3ae-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="3c3ae-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c3ae-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

