---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595766"
---
# <span data-ttu-id="2f3be-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f3be-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="2f3be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f3be-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3be-103">Define propriedades para um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="2f3be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f3be-104">SYNTAX</span></span>

### <span data-ttu-id="2f3be-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f3be-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f3be-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f3be-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f3be-107">DESCRIPTION</span></span>
<span data-ttu-id="2f3be-108">O cmdlet Set-AzEnvironment define pontos de extremidade e metadados para se conectar a uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="2f3be-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f3be-109">EXAMPLES</span></span>

### <span data-ttu-id="2f3be-110">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="2f3be-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="2f3be-111">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="2f3be-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="2f3be-112">OS</span><span class="sxs-lookup"><span data-stu-id="2f3be-112">PARAMETERS</span></span>

### <span data-ttu-id="2f3be-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="2f3be-114">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f3be-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="2f3be-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3be-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="2f3be-116">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="2f3be-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="2f3be-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="2f3be-117">-AdTenant</span></span>
<span data-ttu-id="2f3be-118">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f3be-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="2f3be-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-119">-ARMEndpoint</span></span>
<span data-ttu-id="2f3be-120">O ponto de extremidade do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2f3be-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="2f3be-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3be-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="2f3be-122">O identificador de recurso do recurso do Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="2f3be-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="2f3be-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="2f3be-124">O ponto de extremidade a ser usado ao se comunicar com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f3be-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="2f3be-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="2f3be-126">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="2f3be-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="2f3be-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="2f3be-128">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2f3be-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="2f3be-129">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="2f3be-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="2f3be-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="2f3be-131">Sufixo DNS do serviço de compartimento de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="2f3be-132">Exemplo é vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="2f3be-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="2f3be-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3be-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="2f3be-134">Identificador de recurso do serviço de dados de compartimento de chave do Azure que é o destinatário do token solicitado.</span><span class="sxs-lookup"><span data-stu-id="2f3be-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="2f3be-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="2f3be-136">O ponto de extremidade a ser usado ao se comunicar com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f3be-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="2f3be-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3be-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="2f3be-138">A audiência para tokens de autenticação com a API do Azure log Analytics.</span><span class="sxs-lookup"><span data-stu-id="2f3be-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="2f3be-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2f3be-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="2f3be-140">O identificador de recurso do serviço de lote do Azure que é o destinatário do token solicitado</span><span class="sxs-lookup"><span data-stu-id="2f3be-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="2f3be-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="2f3be-141">-DataLakeAudience</span></span>
<span data-ttu-id="2f3be-142">A audiência para tokens de autenticação com o ponto de extremidade de serviços de data Lake do AD.</span><span class="sxs-lookup"><span data-stu-id="2f3be-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="2f3be-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3be-143">-DefaultProfile</span></span>
<span data-ttu-id="2f3be-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f3be-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="2f3be-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="2f3be-146">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="2f3be-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="2f3be-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-147">-GalleryEndpoint</span></span>
<span data-ttu-id="2f3be-148">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2f3be-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="2f3be-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="2f3be-149">-GraphAudience</span></span>
<span data-ttu-id="2f3be-150">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="2f3be-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="2f3be-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-151">-GraphEndpoint</span></span>
<span data-ttu-id="2f3be-152">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="2f3be-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="2f3be-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="2f3be-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="2f3be-154">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2f3be-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="2f3be-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f3be-155">-Name</span></span>
<span data-ttu-id="2f3be-156">Especifica o nome do ambiente a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="2f3be-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="2f3be-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="2f3be-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="2f3be-158">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="2f3be-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="2f3be-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="2f3be-160">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2f3be-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="2f3be-161">-Escopo</span><span class="sxs-lookup"><span data-stu-id="2f3be-161">-Scope</span></span>
<span data-ttu-id="2f3be-162">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="2f3be-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2f3be-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-163">-ServiceEndpoint</span></span>
<span data-ttu-id="2f3be-164">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="2f3be-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="2f3be-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="2f3be-166">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="2f3be-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f3be-167">-StorageEndpoint</span></span>
<span data-ttu-id="2f3be-168">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="2f3be-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="2f3be-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2f3be-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="2f3be-170">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f3be-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="2f3be-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f3be-171">-Confirm</span></span>
<span data-ttu-id="2f3be-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f3be-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f3be-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f3be-173">-WhatIf</span></span>
<span data-ttu-id="2f3be-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f3be-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f3be-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f3be-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f3be-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3be-176">CommonParameters</span></span>
<span data-ttu-id="2f3be-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f3be-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3be-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f3be-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3be-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f3be-179">INPUTS</span></span>

### <span data-ttu-id="2f3be-180">System. String</span><span class="sxs-lookup"><span data-stu-id="2f3be-180">System.String</span></span>

### <span data-ttu-id="2f3be-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f3be-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f3be-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f3be-182">OUTPUTS</span></span>

### <span data-ttu-id="2f3be-183">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f3be-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="2f3be-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f3be-184">NOTES</span></span>

## <span data-ttu-id="2f3be-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f3be-185">RELATED LINKS</span></span>

[<span data-ttu-id="2f3be-186">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f3be-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="2f3be-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f3be-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="2f3be-188">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f3be-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

