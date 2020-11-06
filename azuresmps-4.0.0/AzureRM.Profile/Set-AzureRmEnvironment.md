---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425727"
---
# <span data-ttu-id="614c2-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="614c2-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="614c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="614c2-102">SYNOPSIS</span></span>
<span data-ttu-id="614c2-103">Define propriedades para um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="614c2-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="614c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="614c2-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="614c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="614c2-105">DESCRIPTION</span></span>
<span data-ttu-id="614c2-106">O cmdlet Set-AzureRMEnvironment define pontos de extremidade e metadados para se conectar a uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="614c2-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="614c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="614c2-107">EXAMPLES</span></span>

### <span data-ttu-id="614c2-108">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="614c2-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="614c2-109">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzureRmEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="614c2-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="614c2-110">OS</span><span class="sxs-lookup"><span data-stu-id="614c2-110">PARAMETERS</span></span>

### <span data-ttu-id="614c2-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="614c2-112">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="614c2-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="614c2-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="614c2-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="614c2-114">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="614c2-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="614c2-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="614c2-115">-AdTenant</span></span>
<span data-ttu-id="614c2-116">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="614c2-116">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="614c2-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="614c2-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="614c2-118">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="614c2-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="614c2-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="614c2-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="614c2-120">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="614c2-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="614c2-121">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="614c2-121">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="614c2-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="614c2-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="614c2-123">Especifica o sufixo do nome de domínio dos serviços do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="614c2-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="614c2-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="614c2-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="614c2-125">Especifica a audiência para tokens de acesso que autorizam solicitações de serviços de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="614c2-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="614c2-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="614c2-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="614c2-127">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="614c2-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="614c2-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-128">-GalleryEndpoint</span></span>
<span data-ttu-id="614c2-129">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="614c2-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="614c2-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="614c2-130">-GraphAudience</span></span>
<span data-ttu-id="614c2-131">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="614c2-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="614c2-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-132">-GraphEndpoint</span></span>
<span data-ttu-id="614c2-133">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="614c2-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="614c2-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="614c2-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="614c2-135">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="614c2-135">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="614c2-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="614c2-136">-Name</span></span>
<span data-ttu-id="614c2-137">Especifica o nome do ambiente a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="614c2-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="614c2-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="614c2-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="614c2-139">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="614c2-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="614c2-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="614c2-141">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="614c2-141">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="614c2-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-142">-ServiceEndpoint</span></span>
<span data-ttu-id="614c2-143">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="614c2-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="614c2-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="614c2-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="614c2-145">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="614c2-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="614c2-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="614c2-146">-StorageEndpoint</span></span>
<span data-ttu-id="614c2-147">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="614c2-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="614c2-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="614c2-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="614c2-149">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="614c2-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="614c2-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="614c2-150">-Confirm</span></span>
<span data-ttu-id="614c2-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="614c2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="614c2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614c2-152">-WhatIf</span></span>
<span data-ttu-id="614c2-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="614c2-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="614c2-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="614c2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="614c2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614c2-155">CommonParameters</span></span>
<span data-ttu-id="614c2-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614c2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614c2-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614c2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614c2-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="614c2-158">INPUTS</span></span>

## <span data-ttu-id="614c2-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="614c2-159">OUTPUTS</span></span>

### <span data-ttu-id="614c2-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="614c2-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="614c2-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="614c2-161">NOTES</span></span>

## <span data-ttu-id="614c2-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="614c2-162">RELATED LINKS</span></span>

[<span data-ttu-id="614c2-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="614c2-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="614c2-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="614c2-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="614c2-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="614c2-165">Remove-AzureRMEnvironment</span></span>]()

