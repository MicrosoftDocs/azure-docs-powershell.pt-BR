---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945730"
---
# <span data-ttu-id="3e3b0-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e3b0-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="3e3b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3b0-103">Cria um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="3e3b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e3b0-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e3b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3b0-106">O cmdlet **Add-AzureEnvironment** cria um novo ambiente de conta do Azure personalizado e o salva em seu perfil de usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="3e3b0-107">O cmdlet retorna um objeto que representa o novo ambiente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="3e3b0-108">Quando o comando é concluído, você pode usar o ambiente no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="3e3b0-109">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="3e3b0-110">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="3e3b0-111">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="3e3b0-112">Somente o parâmetro **Name** desse cmdlet é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="3e3b0-113">Se você omitir um parâmetro, seu valor será NULL ($Null) e o serviço que usa esse ponto de extremidade poderá não funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="3e3b0-114">Para adicionar ou alterar o valor de uma propriedade de ambiente, use o cmdlet **set-AzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="3e3b0-115">Observação: alterar seu ambiente pode causar uma falha na sua conta.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="3e3b0-116">Geralmente, os ambientes são adicionados somente para fins de teste ou solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="3e3b0-117">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3e3b0-118">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3e3b0-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e3b0-119">EXAMPLES</span></span>

### <span data-ttu-id="3e3b0-120">Exemplo 1: adicionar um ambiente do Azure</span><span class="sxs-lookup"><span data-stu-id="3e3b0-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="3e3b0-121">Esse comando cria o ambiente ContosoEnv do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="3e3b0-122">OS</span><span class="sxs-lookup"><span data-stu-id="3e3b0-122">PARAMETERS</span></span>

### <span data-ttu-id="3e3b0-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3e3b0-124">Especifica o ponto de extremidade da autenticação do Azure Active Directory no novo ambiente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3e3b0-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3e3b0-126">Especifica a ID do recurso de uma API de gerenciamento cujo acesso é gerenciado pelo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3e3b0-127">-AdTenant</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3e3b0-128">-AzureKeyVaultDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3e3b0-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3e3b0-130">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-131">-GalleryEndpoint</span></span>
<span data-ttu-id="3e3b0-132">Especifica o ponto de extremidade para a galeria do Gerenciador de recursos do Azure, que armazena modelos da Galeria de grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="3e3b0-133">Para obter mais informações sobre os grupos de recursos e modelos de galeria do Azure, consulte o tópico da ajuda para Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-134">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3e3b0-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="3e3b0-136">Especifica a URL do portal de gerenciamento do Azure no novo ambiente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e3b0-137">-Name</span></span>
<span data-ttu-id="3e3b0-138">Especifica um nome para o ambiente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="3e3b0-139">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-139">This parameter is required.</span></span>
<span data-ttu-id="3e3b0-140">Não use os nomes dos ambientes padrão, AzureCloud e AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3e3b0-141">-Profile</span></span>
<span data-ttu-id="3e3b0-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3e3b0-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3e3b0-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3e3b0-145">Especifica a URL dos arquivos de configurações de publicação para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="3e3b0-146">Um arquivo de configurações de publicação do Azure é um arquivo XML que contém informações sobre a sua conta e um certificado de gerenciamento que permite que o Windows PowerShell entre em sua conta do Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3e3b0-148">Especifica o ponto de extremidade dos dados do Azure Resource Manager, incluindo dados sobre grupos de recursos associados à conta.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="3e3b0-149">Para obter mais informações sobre o Azure Resource Manager, consulte [cmdlets do Azure Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e [uso do Windows PowerShell com o Gerenciador de recursos](https://go.microsoft.com/fwlink/?LinkID=394767) https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-150">-ServiceEndpoint</span></span>
<span data-ttu-id="3e3b0-151">Especifica a URL do ponto de extremidade do serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="3e3b0-152">O ponto de extremidade do serviço do Azure determina se o aplicativo é gerenciado pela plataforma global do Azure, Azure operado pela 21Vianet na China ou uma instalação particular do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3e3b0-153">-SqlDatabaseDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e3b0-154">-StorageEndpoint</span></span>
<span data-ttu-id="3e3b0-155">Especifica o ponto de extremidade padrão dos serviços de armazenamento no novo ambiente.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-155">Specifies the default endpoint of storage services in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3e3b0-156">-TrafficManagerDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3b0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3b0-157">CommonParameters</span></span>
<span data-ttu-id="3e3b0-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3b0-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3b0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3b0-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e3b0-160">INPUTS</span></span>

### <span data-ttu-id="3e3b0-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e3b0-161">None</span></span>
<span data-ttu-id="3e3b0-162">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="3e3b0-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3e3b0-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e3b0-163">OUTPUTS</span></span>

### <span data-ttu-id="3e3b0-164">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e3b0-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="3e3b0-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e3b0-165">NOTES</span></span>

## <span data-ttu-id="3e3b0-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e3b0-166">RELATED LINKS</span></span>

[<span data-ttu-id="3e3b0-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e3b0-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="3e3b0-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e3b0-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="3e3b0-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e3b0-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


