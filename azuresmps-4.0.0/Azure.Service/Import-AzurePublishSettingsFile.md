---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946261"
---
# <span data-ttu-id="f01bb-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f01bb-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="f01bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f01bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f01bb-103">Importa um arquivo de configurações de publicação que permite que você gerencie suas contas do Azure no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f01bb-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="f01bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f01bb-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f01bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f01bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f01bb-106">O cmdlet **Import-AzurePublishSettingsFile** importa um arquivo de configurações de publicação (\*. publishsettings) que contém informações sobre suas contas do Azure e salva um arquivo de dados de assinatura em seu computador.</span><span class="sxs-lookup"><span data-stu-id="f01bb-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="f01bb-107">Quando o cmdlet é concluído, você pode gerenciar suas contas do Azure no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f01bb-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="f01bb-108">Antes de executar **Import-AzurePublishSettingsFile** , execute **Get-AzurePublishSettingsFile** , que baixa e salva o arquivo de configurações de publicação para que você possa importá-lo.</span><span class="sxs-lookup"><span data-stu-id="f01bb-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="f01bb-109">Para disponibilizar sua conta do Azure para o Windows PowerShell, você pode usar um arquivo de configurações de publicação ou o cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="f01bb-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="f01bb-110">Os arquivos de configurações de publicação permitem que você prepare a sessão antecipadamente para poder executar scripts e trabalhos em segundo plano autônomos.</span><span class="sxs-lookup"><span data-stu-id="f01bb-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="f01bb-111">No entanto, nem todos os serviços dão suporte a arquivos de configurações de publicação.</span><span class="sxs-lookup"><span data-stu-id="f01bb-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="f01bb-112">Por exemplo, o módulo **AzureResourceManager** não dá suporte a arquivos de configurações de publicação.</span><span class="sxs-lookup"><span data-stu-id="f01bb-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="f01bb-113">**Observação de segurança:** Os arquivos de configurações de publicação contêm um certificado de gerenciamento codificado, mas não criptografado.</span><span class="sxs-lookup"><span data-stu-id="f01bb-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="f01bb-114">Se usuários mal-intencionados acessarem o arquivo de configurações de publicação, eles poderão editar, criar e excluir seus serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="f01bb-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="f01bb-115">Como prática recomendada de segurança, salve o arquivo em um local na sua pasta downloads ou documentos e, em seguida, exclua-o depois de usar o cmdlet **Import-AzurePublishSettingsFile** para importar as configurações.</span><span class="sxs-lookup"><span data-stu-id="f01bb-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="f01bb-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f01bb-116">EXAMPLES</span></span>

### <span data-ttu-id="f01bb-117">Exemplo 1: importar um arquivo</span><span class="sxs-lookup"><span data-stu-id="f01bb-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="f01bb-118">Esse comando importa o arquivo "C:\Temp\MyAccount.publishsettings".</span><span class="sxs-lookup"><span data-stu-id="f01bb-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="f01bb-119">OS</span><span class="sxs-lookup"><span data-stu-id="f01bb-119">PARAMETERS</span></span>

### <span data-ttu-id="f01bb-120">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="f01bb-120">-Environment</span></span>
<span data-ttu-id="f01bb-121">Especifica um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="f01bb-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="f01bb-122">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="f01bb-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f01bb-123">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="f01bb-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f01bb-124">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f01bb-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f01bb-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f01bb-125">-Profile</span></span>
<span data-ttu-id="f01bb-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f01bb-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f01bb-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f01bb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f01bb-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f01bb-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="f01bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01bb-129">CommonParameters</span></span>
<span data-ttu-id="f01bb-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f01bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01bb-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f01bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01bb-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f01bb-132">INPUTS</span></span>

### <span data-ttu-id="f01bb-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f01bb-133">None</span></span>
<span data-ttu-id="f01bb-134">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="f01bb-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f01bb-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f01bb-135">OUTPUTS</span></span>

### <span data-ttu-id="f01bb-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f01bb-136">None</span></span>
<span data-ttu-id="f01bb-137">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f01bb-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f01bb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f01bb-138">NOTES</span></span>
* <span data-ttu-id="f01bb-139">Um "arquivo de configurações de publicação" é um arquivo XML com uma extensão de nome de arquivo. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f01bb-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="f01bb-140">O arquivo contém um certificado codificado que fornece credenciais de gerenciamento para suas assinaturas do Azure.</span><span class="sxs-lookup"><span data-stu-id="f01bb-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="f01bb-141">Depois de importar esse arquivo, exclua-o para evitar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="f01bb-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="f01bb-142">Um "arquivo de dados de assinatura" é um arquivo XML que pode ser salvo em seu computador com segurança.</span><span class="sxs-lookup"><span data-stu-id="f01bb-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="f01bb-143">Por padrão, ele é salvo no perfil de usuário móvel ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="f01bb-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="f01bb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f01bb-144">RELATED LINKS</span></span>

[<span data-ttu-id="f01bb-145">Como instalar e configurar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f01bb-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="f01bb-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f01bb-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="f01bb-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f01bb-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


