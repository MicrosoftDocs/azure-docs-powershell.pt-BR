---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: c39b61ab51296231b0952d1f12bd18e6d3aa13d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440983"
---
# <span data-ttu-id="f2852-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2852-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="f2852-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2852-102">SYNOPSIS</span></span>
<span data-ttu-id="f2852-103">Define propriedades para um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2852-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2852-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2852-104">SYNTAX</span></span>

### <span data-ttu-id="f2852-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2852-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2852-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2852-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2852-107">DESCRIPTION</span></span>
<span data-ttu-id="f2852-108">O cmdlet Set-AzureRMEnvironment define pontos de extremidade e metadados para se conectar a uma instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2852-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="f2852-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2852-109">EXAMPLES</span></span>

### <span data-ttu-id="f2852-110">Exemplo 1: Criando e modificando um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="f2852-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="f2852-111">Neste exemplo, estamos criando um novo ambiente do Azure com exemplos de pontos de extremidade usando Add-AzureRmEnvironment, e estamos alterando o valor dos atributos ActiveDirectoryEndpoint e GraphEndpoint do ambiente criado usando o cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="f2852-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="f2852-112">OS</span><span class="sxs-lookup"><span data-stu-id="f2852-112">PARAMETERS</span></span>

### <span data-ttu-id="f2852-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f2852-114">Especifica a autoridade base para a autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2852-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f2852-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f2852-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f2852-116">Especifica a audiência para tokens que autenticam solicitações de pontos de extremidade do Azure Resource Manager ou RDFE (gerenciamento de serviço).</span><span class="sxs-lookup"><span data-stu-id="f2852-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f2852-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f2852-117">-AdTenant</span></span>
<span data-ttu-id="f2852-118">Especifica o locatário padrão do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2852-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f2852-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-119">-ARMEndpoint</span></span>
<span data-ttu-id="f2852-120">O ponto de extremidade do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f2852-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="f2852-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f2852-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f2852-122">Sufixo DNS do trabalho e dos serviços de catálogo do Azure data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f2852-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f2852-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f2852-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f2852-124">Sufixo DNS do sistema de arquivos do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2852-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f2852-125">Exemplo: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f2852-125">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f2852-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f2852-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f2852-127">Especifica o sufixo do nome de domínio dos serviços do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f2852-127">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f2852-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f2852-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f2852-129">Especifica a audiência para tokens de acesso que autorizam solicitações de serviços de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f2852-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="f2852-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f2852-130">-DataLakeAudience</span></span>
<span data-ttu-id="f2852-131">A audiência para tokens de autenticação com o ponto de extremidade de serviços de data Lake do AD.</span><span class="sxs-lookup"><span data-stu-id="f2852-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="f2852-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2852-132">-DefaultProfile</span></span>
<span data-ttu-id="f2852-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2852-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2852-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f2852-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f2852-135">Indica que o ADFS (serviços de Federação do Active Directory) Authentication local é permitido.</span><span class="sxs-lookup"><span data-stu-id="f2852-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f2852-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-136">-GalleryEndpoint</span></span>
<span data-ttu-id="f2852-137">Especifica o ponto de extremidade para a Galeria de modelos de implantação do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f2852-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f2852-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f2852-138">-GraphAudience</span></span>
<span data-ttu-id="f2852-139">A audiência para tokens de autenticação com o ponto de extremidade do gráfico do AD.</span><span class="sxs-lookup"><span data-stu-id="f2852-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f2852-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-140">-GraphEndpoint</span></span>
<span data-ttu-id="f2852-141">Especifica a URL para solicitações de gráfico (metadados do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f2852-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f2852-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f2852-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="f2852-143">Especifica a URL para o portal de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f2852-143">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f2852-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2852-144">-Name</span></span>
<span data-ttu-id="f2852-145">Especifica o nome do ambiente a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="f2852-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="f2852-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f2852-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f2852-147">Especifica a URL na qual os arquivos. publishsettings podem ser baixados.</span><span class="sxs-lookup"><span data-stu-id="f2852-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f2852-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f2852-149">Especifica a URL para as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f2852-149">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f2852-150">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f2852-150">-Scope</span></span>
<span data-ttu-id="f2852-151">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="f2852-151">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f2852-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-152">-ServiceEndpoint</span></span>
<span data-ttu-id="f2852-153">Especifica o ponto de extremidade para solicitações de gerenciamento de serviço (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f2852-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f2852-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f2852-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f2852-155">Especifica o sufixo de nome de domínio dos servidores de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2852-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f2852-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2852-156">-StorageEndpoint</span></span>
<span data-ttu-id="f2852-157">Especifica o ponto de extremidade do armazenamento (BLOB, tabela, fila e arquivo).</span><span class="sxs-lookup"><span data-stu-id="f2852-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f2852-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f2852-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f2852-159">Especifica o sufixo de nome de domínio dos serviços do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2852-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f2852-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2852-160">-Confirm</span></span>
<span data-ttu-id="f2852-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2852-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2852-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2852-162">-WhatIf</span></span>
<span data-ttu-id="f2852-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2852-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2852-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2852-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2852-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2852-165">CommonParameters</span></span>
<span data-ttu-id="f2852-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2852-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2852-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2852-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2852-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2852-168">INPUTS</span></span>

## <span data-ttu-id="f2852-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2852-169">OUTPUTS</span></span>

### <span data-ttu-id="f2852-170">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2852-170">PSAzureEnvironment</span></span>

## <span data-ttu-id="f2852-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2852-171">NOTES</span></span>

## <span data-ttu-id="f2852-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2852-172">RELATED LINKS</span></span>

[<span data-ttu-id="f2852-173">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2852-173">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="f2852-174">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2852-174">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="f2852-175">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2852-175">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

