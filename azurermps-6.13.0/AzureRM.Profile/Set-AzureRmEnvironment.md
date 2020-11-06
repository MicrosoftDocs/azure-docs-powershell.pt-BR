---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 073126f3f750f2decf7189c53733c5fcaaabee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429396"
---
# <span data-ttu-id="3cbdc-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cbdc-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="3cbdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbdc-103">Define propriedades para um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cbdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cbdc-104">SYNTAX</span></span>

### <span data-ttu-id="3cbdc-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="3cbdc-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureAnalysisServicesEndpointSuffix] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cbdc-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cbdc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cbdc-107">DESCRIPTION</span></span>
<span data-ttu-id="3cbdc-108">O cmdlet Set-AzureRMEnvironment define pontos de extremidade e metadados para se conectar a uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="3cbdc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cbdc-109">EXAMPLES</span></span>

### <span data-ttu-id="3cbdc-110">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="3cbdc-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
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

<span data-ttu-id="3cbdc-111">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzureRmEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3cbdc-112">OS</span><span class="sxs-lookup"><span data-stu-id="3cbdc-112">PARAMETERS</span></span>

### <span data-ttu-id="3cbdc-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3cbdc-114">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3cbdc-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbdc-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3cbdc-116">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="3cbdc-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3cbdc-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3cbdc-117">-AdTenant</span></span>
<span data-ttu-id="3cbdc-118">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3cbdc-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-119">-ARMEndpoint</span></span>
<span data-ttu-id="3cbdc-120">O ponto de extremidade do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="3cbdc-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="3cbdc-122">Sufixo DNS dos pontos de extremidade do serviço do Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3cbdc-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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

### <span data-ttu-id="3cbdc-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3cbdc-124">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3cbdc-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3cbdc-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3cbdc-126">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="3cbdc-127">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3cbdc-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3cbdc-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3cbdc-129">Especifica o sufixo do nome de domínio dos serviços do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="3cbdc-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbdc-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3cbdc-131">Especifica a audiência para tokens de acesso que autorizam solicitações de serviços de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="3cbdc-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="3cbdc-133">Especifica o ponto de extremidade para o acesso à consulta de insights operacionais.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="3cbdc-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbdc-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="3cbdc-135">Especifica o público-alvo para tokens de acesso que autorizam solicitações de serviços de insights operacionais.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="3cbdc-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cbdc-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="3cbdc-137">O identificador de recurso do serviço de lote do Azure que é o destinatário do token solicitado</span><span class="sxs-lookup"><span data-stu-id="3cbdc-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="3cbdc-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3cbdc-138">-DataLakeAudience</span></span>
<span data-ttu-id="3cbdc-139">A audiência para tokens de autenticação com o ponto de extremidade de serviços de data Lake do AD.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3cbdc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbdc-140">-DefaultProfile</span></span>
<span data-ttu-id="3cbdc-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-141">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cbdc-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3cbdc-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3cbdc-143">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3cbdc-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-144">-GalleryEndpoint</span></span>
<span data-ttu-id="3cbdc-145">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3cbdc-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="3cbdc-146">-GraphAudience</span></span>
<span data-ttu-id="3cbdc-147">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3cbdc-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-148">-GraphEndpoint</span></span>
<span data-ttu-id="3cbdc-149">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="3cbdc-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3cbdc-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3cbdc-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="3cbdc-151">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3cbdc-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cbdc-152">-Name</span></span>
<span data-ttu-id="3cbdc-153">Especifica o nome do ambiente a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-153">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="3cbdc-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3cbdc-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3cbdc-155">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3cbdc-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3cbdc-157">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3cbdc-158">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3cbdc-158">-Scope</span></span>
<span data-ttu-id="3cbdc-159">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3cbdc-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-160">-ServiceEndpoint</span></span>
<span data-ttu-id="3cbdc-161">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3cbdc-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3cbdc-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3cbdc-163">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3cbdc-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cbdc-164">-StorageEndpoint</span></span>
<span data-ttu-id="3cbdc-165">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="3cbdc-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3cbdc-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cbdc-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3cbdc-167">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3cbdc-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cbdc-168">-Confirm</span></span>
<span data-ttu-id="3cbdc-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cbdc-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cbdc-170">-WhatIf</span></span>
<span data-ttu-id="3cbdc-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cbdc-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cbdc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbdc-173">CommonParameters</span></span>
<span data-ttu-id="3cbdc-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cbdc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbdc-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cbdc-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbdc-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cbdc-176">INPUTS</span></span>

### <span data-ttu-id="3cbdc-177">System. String</span><span class="sxs-lookup"><span data-stu-id="3cbdc-177">System.String</span></span>

### <span data-ttu-id="3cbdc-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cbdc-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3cbdc-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cbdc-179">OUTPUTS</span></span>

### <span data-ttu-id="3cbdc-180">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cbdc-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="3cbdc-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cbdc-181">NOTES</span></span>

## <span data-ttu-id="3cbdc-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cbdc-182">RELATED LINKS</span></span>

[<span data-ttu-id="3cbdc-183">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cbdc-183">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="3cbdc-184">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cbdc-184">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="3cbdc-185">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cbdc-185">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

