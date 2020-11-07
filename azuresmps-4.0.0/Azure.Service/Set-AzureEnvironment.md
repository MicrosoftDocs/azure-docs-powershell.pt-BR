---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945967"
---
# <span data-ttu-id="39faf-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="39faf-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="39faf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39faf-102">SYNOPSIS</span></span>
<span data-ttu-id="39faf-103">Altera as propriedades de um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="39faf-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="39faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39faf-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39faf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39faf-105">DESCRIPTION</span></span>
<span data-ttu-id="39faf-106">O cmdlet **set-AzureEnvironment** altera as propriedades de um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="39faf-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="39faf-107">Ele retorna um objeto que representa o ambiente com seus novos valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39faf-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="39faf-108">Use o parâmetro **Name** para identificar o ambiente e os outros parâmetros para alterar os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="39faf-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="39faf-109">Você não pode usar **set-AzureEnvironment** para alterar o nome de um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="39faf-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="39faf-110">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="39faf-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="39faf-111">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="39faf-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="39faf-112">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="39faf-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="39faf-113">Observação: não altere as propriedades dos ambientes AzureCloud ou AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="39faf-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="39faf-114">Use esse cmdlet para alterar os valores de ambientes privados que você criar.</span><span class="sxs-lookup"><span data-stu-id="39faf-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="39faf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39faf-115">EXAMPLES</span></span>

### <span data-ttu-id="39faf-116">Exemplo 1: alterar as propriedades do ambiente</span><span class="sxs-lookup"><span data-stu-id="39faf-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="39faf-117">Esse comando altera os valores das propriedades **PublishSettingsFileUrl** e **StorageEndpoint** do ambiente ContosoEnv.</span><span class="sxs-lookup"><span data-stu-id="39faf-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="39faf-118">OS</span><span class="sxs-lookup"><span data-stu-id="39faf-118">PARAMETERS</span></span>

### <span data-ttu-id="39faf-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="39faf-120">Altera o ponto de extremidade da autenticação do Azure Active Directory para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

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

### <span data-ttu-id="39faf-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="39faf-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="39faf-122">Especifica a ID do recurso de uma API de gerenciamento cujo acesso é gerenciado pelo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39faf-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="39faf-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="39faf-123">-AdTenant</span></span>
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

### <span data-ttu-id="39faf-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="39faf-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="39faf-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="39faf-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="39faf-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="39faf-126">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="39faf-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-127">-GalleryEndpoint</span></span>
<span data-ttu-id="39faf-128">Altera o ponto de extremidade da galeria do Gerenciador de recursos do Azure para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="39faf-129">O ponto de extremidade da galeria é o local dos modelos da Galeria de grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="39faf-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="39faf-130">Para obter mais informações sobre os grupos de recursos e modelos de galeria do Azure, consulte o tópico da ajuda para [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="39faf-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

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

### <span data-ttu-id="39faf-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-131">-GraphEndpoint</span></span>
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

### <span data-ttu-id="39faf-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="39faf-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="39faf-133">Altera a URL do portal de gerenciamento do Azure para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="39faf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="39faf-134">-Name</span></span>
<span data-ttu-id="39faf-135">Identifica o ambiente que está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="39faf-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="39faf-136">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="39faf-136">This parameter is required.</span></span>
<span data-ttu-id="39faf-137">O valor do parâmetro diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39faf-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="39faf-138">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="39faf-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="39faf-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="39faf-139">-Profile</span></span>
<span data-ttu-id="39faf-140">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="39faf-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="39faf-141">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="39faf-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39faf-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="39faf-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="39faf-143">Altera a URL de arquivos de configurações de publicação no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="39faf-144">Um arquivo de configurações de publicação do Azure é um arquivo XML que contém informações sobre a sua conta e um certificado de gerenciamento que permite que o Windows PowerShell entre em sua conta do Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="39faf-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="39faf-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="39faf-146">Altera o ponto de extremidade dos dados do Azure Resource Manager, incluindo dados sobre grupos de recursos associados à conta.</span><span class="sxs-lookup"><span data-stu-id="39faf-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="39faf-147">Para obter mais informações sobre o Azure Resource Manager, consulte [cmdlets do Azure Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e [uso do Windows PowerShell com o Gerenciador de recursos](https://go.microsoft.com/fwlink/?LinkID=394767) https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="39faf-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="39faf-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-148">-ServiceEndpoint</span></span>
<span data-ttu-id="39faf-149">Altera a URL do ponto de extremidade do serviço do Azure no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="39faf-150">O ponto de extremidade do serviço do Azure determina se o aplicativo é gerenciado pela plataforma global do Azure, Azure operado pela 21Vianet na China ou uma instalação particular do Azure.</span><span class="sxs-lookup"><span data-stu-id="39faf-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="39faf-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="39faf-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="39faf-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="39faf-152">-StorageEndpoint</span></span>
<span data-ttu-id="39faf-153">Altera o ponto de extremidade padrão dos serviços de armazenamento no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="39faf-153">Changes the default endpoint of storage services in the specified environment.</span></span>

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

### <span data-ttu-id="39faf-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="39faf-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="39faf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39faf-155">CommonParameters</span></span>
<span data-ttu-id="39faf-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39faf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39faf-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39faf-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39faf-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39faf-158">INPUTS</span></span>

### <span data-ttu-id="39faf-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="39faf-159">None</span></span>
<span data-ttu-id="39faf-160">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="39faf-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="39faf-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39faf-161">OUTPUTS</span></span>

### <span data-ttu-id="39faf-162">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="39faf-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="39faf-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39faf-163">NOTES</span></span>

## <span data-ttu-id="39faf-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39faf-164">RELATED LINKS</span></span>

[<span data-ttu-id="39faf-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="39faf-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="39faf-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="39faf-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="39faf-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="39faf-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


