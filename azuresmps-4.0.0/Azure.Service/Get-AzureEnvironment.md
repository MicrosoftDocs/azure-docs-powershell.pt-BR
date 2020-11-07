---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946352"
---
# <span data-ttu-id="3a5b0-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a5b0-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="3a5b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5b0-103">Obtém ambientes do Azure</span><span class="sxs-lookup"><span data-stu-id="3a5b0-103">Gets Azure environments</span></span>

## <span data-ttu-id="3a5b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a5b0-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a5b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5b0-106">O cmdlet **Get-AzureEnvironment** Obtém os ambientes do Azure que estão disponíveis para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="3a5b0-107">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="3a5b0-108">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="3a5b0-109">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3a5b0-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="3a5b0-110">O cmdlet **Get-AzureEnvironment** Obtém ambientes do seu arquivo de dados de assinatura, e não do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="3a5b0-111">Se o arquivo de dados de assinatura estiver desatualizado, execute o cmdlet **Add-AzureAccount** ou **Import-PublishSettingsFile** para atualizá-lo.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="3a5b0-112">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a5b0-113">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a5b0-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3a5b0-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a5b0-114">EXAMPLES</span></span>

### <span data-ttu-id="3a5b0-115">Exemplo 1: obter todos os ambientes</span><span class="sxs-lookup"><span data-stu-id="3a5b0-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="3a5b0-116">Esse comando obtém todos os ambientes que estão disponíveis para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="3a5b0-117">Exemplo 2: obter um ambiente por nome</span><span class="sxs-lookup"><span data-stu-id="3a5b0-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="3a5b0-118">Este exemplo obtém o ambiente AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="3a5b0-119">Exemplo 3: obter todas as propriedades de todos os ambientes</span><span class="sxs-lookup"><span data-stu-id="3a5b0-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="3a5b0-120">Esse comando obtém todas as propriedades de todos os ambientes.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="3a5b0-121">O comando usa o cmdlet **Get-AzureEnvironment** para obter todos os ambientes do Azure para esta conta.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="3a5b0-122">Em seguida, ele usa o cmdlet **ForEach-Object** para executar um comando **Get-AzureEnvironment** com o parâmetro **Name** em cada ambiente.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="3a5b0-123">O valor do parâmetro **Name** é a propriedade **environmentname** de cada ambiente.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="3a5b0-124">Sem parâmetros, **Get-AzureEnvironment** obtém apenas as propriedades selecionadas de um ambiente.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="3a5b0-125">OS</span><span class="sxs-lookup"><span data-stu-id="3a5b0-125">PARAMETERS</span></span>

### <span data-ttu-id="3a5b0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a5b0-126">-Name</span></span>
<span data-ttu-id="3a5b0-127">Obtém apenas o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-127">Gets only the specified environment.</span></span>
<span data-ttu-id="3a5b0-128">Digite o nome do ambiente.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-128">Type the environment name.</span></span>
<span data-ttu-id="3a5b0-129">O valor do parâmetro diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="3a5b0-130">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="3a5b0-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3a5b0-131">-Profile</span></span>
<span data-ttu-id="3a5b0-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3a5b0-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a5b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5b0-134">CommonParameters</span></span>
<span data-ttu-id="3a5b0-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5b0-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5b0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5b0-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a5b0-137">INPUTS</span></span>

### <span data-ttu-id="3a5b0-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3a5b0-138">None</span></span>
<span data-ttu-id="3a5b0-139">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3a5b0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a5b0-140">OUTPUTS</span></span>

### <span data-ttu-id="3a5b0-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="3a5b0-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="3a5b0-142">Por padrão, **Get-AzureEnvironment** retorna um objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="3a5b0-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="3a5b0-143">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a5b0-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="3a5b0-144">Quando você executa **Get-AzureEnvironment** com o parâmetro **Name** , ele retorna um objeto  **WindowsAzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="3a5b0-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="3a5b0-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a5b0-145">NOTES</span></span>

## <span data-ttu-id="3a5b0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a5b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="3a5b0-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="3a5b0-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="3a5b0-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a5b0-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="3a5b0-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3a5b0-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="3a5b0-150">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3a5b0-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="3a5b0-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a5b0-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="3a5b0-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a5b0-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


