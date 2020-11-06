---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610480"
---
# <span data-ttu-id="8f6cc-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8f6cc-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="8f6cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6cc-103">Adiciona pontos de extremidade e metadados para uma instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f6cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f6cc-104">SYNTAX</span></span>

### <span data-ttu-id="8f6cc-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f6cc-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f6cc-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6cc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f6cc-107">DESCRIPTION</span></span>
<span data-ttu-id="8f6cc-108">O cmdlet Add-AzureRmEnvironment adiciona pontos de extremidade e metadados para habilitar cmdlets do Azure Resource Manager para se conectar a uma nova instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="8f6cc-109">Os ambientes internos AzureCloud e AzureChinaCloud direcionam as instâncias públicas existentes do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="8f6cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f6cc-110">EXAMPLES</span></span>

### <span data-ttu-id="8f6cc-111">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="8f6cc-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="8f6cc-112">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzureRmEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="8f6cc-113">OS</span><span class="sxs-lookup"><span data-stu-id="8f6cc-113">PARAMETERS</span></span>

### <span data-ttu-id="8f6cc-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="8f6cc-115">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="8f6cc-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6cc-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="8f6cc-117">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="8f6cc-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="8f6cc-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="8f6cc-118">-AdTenant</span></span>
<span data-ttu-id="8f6cc-119">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="8f6cc-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-120">-ARMEndpoint</span></span>
<span data-ttu-id="8f6cc-121">O ponto de extremidade do Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="8f6cc-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="8f6cc-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8f6cc-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="8f6cc-123">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8f6cc-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="8f6cc-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8f6cc-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="8f6cc-125">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="8f6cc-126">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="8f6cc-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="8f6cc-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8f6cc-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="8f6cc-128">Especifica o sufixo do nome de domínio dos serviços do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="8f6cc-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6cc-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="8f6cc-130">Especifica a audiência para tokens de acesso que autorizam solicitações de serviços de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6cc-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="8f6cc-131">-DataLakeAudience</span></span>
<span data-ttu-id="8f6cc-132">A audiência para tokens de autenticação com o ponto de extremidade de serviços de data Lake do AD.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="8f6cc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6cc-133">-DefaultProfile</span></span>
<span data-ttu-id="8f6cc-134">O credeetnails, locatário e assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8f6cc-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f6cc-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="8f6cc-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="8f6cc-136">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="8f6cc-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-137">-GalleryEndpoint</span></span>
<span data-ttu-id="8f6cc-138">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="8f6cc-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="8f6cc-139">-GraphAudience</span></span>
<span data-ttu-id="8f6cc-140">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="8f6cc-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-141">-GraphEndpoint</span></span>
<span data-ttu-id="8f6cc-142">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="8f6cc-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="8f6cc-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="8f6cc-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="8f6cc-144">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="8f6cc-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f6cc-145">-Name</span></span>
<span data-ttu-id="8f6cc-146">Especifica o nome do ambiente a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="8f6cc-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="8f6cc-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="8f6cc-148">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="8f6cc-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="8f6cc-150">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="8f6cc-151">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8f6cc-151">-Scope</span></span>
<span data-ttu-id="8f6cc-152">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8f6cc-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-153">-ServiceEndpoint</span></span>
<span data-ttu-id="8f6cc-154">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="8f6cc-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="8f6cc-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8f6cc-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="8f6cc-156">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="8f6cc-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f6cc-157">-StorageEndpoint</span></span>
<span data-ttu-id="8f6cc-158">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="8f6cc-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="8f6cc-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8f6cc-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="8f6cc-160">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="8f6cc-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f6cc-161">-Confirm</span></span>
<span data-ttu-id="8f6cc-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6cc-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6cc-163">-WhatIf</span></span>
<span data-ttu-id="8f6cc-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f6cc-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6cc-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6cc-166">CommonParameters</span></span>
<span data-ttu-id="8f6cc-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6cc-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6cc-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6cc-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f6cc-169">INPUTS</span></span>

## <span data-ttu-id="8f6cc-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f6cc-170">OUTPUTS</span></span>

### <span data-ttu-id="8f6cc-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8f6cc-171">PSAzureEnvironment</span></span>
<span data-ttu-id="8f6cc-172">Esse cmdlet retorna o conjunto de pontos de extremidade e metadados necessários para se comunicar com uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6cc-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="8f6cc-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f6cc-173">NOTES</span></span>

## <span data-ttu-id="8f6cc-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f6cc-174">RELATED LINKS</span></span>

[<span data-ttu-id="8f6cc-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8f6cc-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="8f6cc-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8f6cc-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="8f6cc-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8f6cc-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

