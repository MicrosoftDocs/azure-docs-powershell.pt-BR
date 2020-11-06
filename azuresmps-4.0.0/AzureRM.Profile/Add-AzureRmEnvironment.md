---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425673"
---
# <span data-ttu-id="df529-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="df529-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="df529-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df529-102">SYNOPSIS</span></span>
<span data-ttu-id="df529-103">Adiciona pontos de extremidade e metadados para uma instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df529-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="df529-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df529-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df529-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df529-105">DESCRIPTION</span></span>
<span data-ttu-id="df529-106">O cmdlet Add-AzureRmEnvironment adiciona pontos de extremidade e metadados para habilitar cmdlets do Azure Resource Manager para se conectar a uma nova instância do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df529-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="df529-107">Os ambientes internos AzureCloud e AzureChinaCloud direcionam as instâncias públicas existentes do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df529-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="df529-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df529-108">EXAMPLES</span></span>

### <span data-ttu-id="df529-109">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="df529-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="df529-110">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzureRmEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="df529-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="df529-111">OS</span><span class="sxs-lookup"><span data-stu-id="df529-111">PARAMETERS</span></span>

### <span data-ttu-id="df529-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="df529-113">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df529-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="df529-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="df529-115">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="df529-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="df529-116">-AdTenant</span></span>
<span data-ttu-id="df529-117">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df529-117">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="df529-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="df529-119">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="df529-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="df529-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="df529-121">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="df529-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="df529-122">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="df529-122">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="df529-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="df529-124">Especifica o sufixo do nome de domínio dos serviços do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="df529-124">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="df529-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="df529-126">Especifica a audiência para tokens de acesso que autorizam solicitações de serviços de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="df529-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="df529-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="df529-128">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="df529-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-129">-GalleryEndpoint</span></span>
<span data-ttu-id="df529-130">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df529-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="df529-131">-GraphAudience</span></span>
<span data-ttu-id="df529-132">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="df529-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-133">-GraphEndpoint</span></span>
<span data-ttu-id="df529-134">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="df529-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="df529-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="df529-136">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="df529-136">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="df529-137">-Name</span></span>
<span data-ttu-id="df529-138">Especifica o nome do ambiente a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="df529-138">Specifies the name of the environment to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="df529-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="df529-140">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="df529-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="df529-142">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df529-142">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-143">-ServiceEndpoint</span></span>
<span data-ttu-id="df529-144">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="df529-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="df529-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="df529-146">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df529-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="df529-147">-StorageEndpoint</span></span>
<span data-ttu-id="df529-148">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="df529-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df529-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="df529-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="df529-150">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="df529-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df529-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df529-151">-Confirm</span></span>
<span data-ttu-id="df529-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df529-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df529-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df529-153">-WhatIf</span></span>
<span data-ttu-id="df529-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df529-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df529-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df529-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df529-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df529-156">CommonParameters</span></span>
<span data-ttu-id="df529-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df529-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df529-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df529-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df529-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df529-159">INPUTS</span></span>

## <span data-ttu-id="df529-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df529-160">OUTPUTS</span></span>

### <span data-ttu-id="df529-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="df529-161">PSAzureEnvironment</span></span>
<span data-ttu-id="df529-162">Esse cmdlet retorna o conjunto de pontos de extremidade e metadados necessários para se comunicar com uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="df529-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="df529-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df529-163">NOTES</span></span>

## <span data-ttu-id="df529-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df529-164">RELATED LINKS</span></span>

[<span data-ttu-id="df529-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="df529-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="df529-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="df529-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="df529-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="df529-167">Set-AzureRMEnvironment</span></span>]()

