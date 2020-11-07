---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945633"
---
# <span data-ttu-id="a9189-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a9189-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="a9189-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9189-102">SYNOPSIS</span></span>
<span data-ttu-id="a9189-103">Baixa o arquivo de configurações de publicação para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="a9189-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9189-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9189-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9189-105">DESCRIPTION</span></span>
<span data-ttu-id="a9189-106">O cmdlet **Get-AzurePublishSettingsFile** faz o download de um arquivo de configurações de publicação para uma assinatura na sua conta.</span><span class="sxs-lookup"><span data-stu-id="a9189-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="a9189-107">Quando o comando é concluído, você pode usar o cmdlet **Import-PublishSettingsFile** para fazer as configurações no arquivo disponíveis para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9189-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="a9189-108">Para disponibilizar sua conta do Azure para o Windows PowerShell, você pode usar um arquivo de configurações de publicação ou o cmdlet **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="a9189-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="a9189-109">Os arquivos de configurações de publicação permitem que você prepare a sessão antecipadamente para poder executar scripts e trabalhos em segundo plano autônomos.</span><span class="sxs-lookup"><span data-stu-id="a9189-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="a9189-110">No entanto, nem todos os serviços dão suporte a arquivos de configurações de publicação.</span><span class="sxs-lookup"><span data-stu-id="a9189-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="a9189-111">Por exemplo, o módulo **AzureResourceManager** não dá suporte a arquivos de configurações de publicação.</span><span class="sxs-lookup"><span data-stu-id="a9189-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="a9189-112">Quando você executa o **Get-AzurePublishSettingsFile** , ele abre o navegador padrão e solicita que você entre na sua conta do Azure, selecione uma assinatura e selecione um local do sistema de arquivos para o arquivo de configurações de publicação.</span><span class="sxs-lookup"><span data-stu-id="a9189-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="a9189-113">Em seguida, ele baixa o arquivo de configurações de publicação para a sua assinatura no arquivo que você selecionou.</span><span class="sxs-lookup"><span data-stu-id="a9189-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="a9189-114">Um "arquivo de configurações de publicação" é um arquivo XML com uma extensão de nome de arquivo. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="a9189-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="a9189-115">O arquivo contém um certificado codificado que fornece credenciais de gerenciamento para suas assinaturas do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="a9189-116">**Observação de segurança:** Os arquivos de configurações de publicação contêm credenciais usadas para administrar suas assinaturas e serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="a9189-117">Se usuários mal-intencionados acessarem o arquivo de configurações de publicação, poderão editar, criar e excluir seus serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="a9189-118">Como prática recomendada de segurança, salve o arquivo em um local na sua pasta downloads ou documentos e, em seguida, exclua-o depois de usar o cmdlet **Import-AzurePublishSettingsFile** para importar as configurações.</span><span class="sxs-lookup"><span data-stu-id="a9189-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="a9189-119">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9189-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a9189-120">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a9189-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a9189-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9189-121">EXAMPLES</span></span>

### <span data-ttu-id="a9189-122">Exemplo 1: baixar um arquivo de configurações de publicação</span><span class="sxs-lookup"><span data-stu-id="a9189-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="a9189-123">Esse comando abre o navegador padrão, se conecta à sua conta do Windows Azure e, em seguida, baixa o arquivo. publishsettings para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="a9189-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="a9189-124">Exemplo 2: especificar um território</span><span class="sxs-lookup"><span data-stu-id="a9189-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="a9189-125">Esse comando baixa o arquivo de configurações de publicação de uma conta no domínio contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a9189-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="a9189-126">Use um comando com o parâmetro de **território** quando você se conectar ao Azure com uma conta organizacional, em vez de uma conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9189-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="a9189-127">OS</span><span class="sxs-lookup"><span data-stu-id="a9189-127">PARAMETERS</span></span>

### <span data-ttu-id="a9189-128">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="a9189-128">-Environment</span></span>
<span data-ttu-id="a9189-129">Especifica um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="a9189-130">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="a9189-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a9189-131">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="a9189-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a9189-132">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9189-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="a9189-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9189-133">-PassThru</span></span>
<span data-ttu-id="a9189-134">Retorna $True se o comando tiver êxito e $False se falhar.</span><span class="sxs-lookup"><span data-stu-id="a9189-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="a9189-135">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a9189-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9189-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a9189-136">-Profile</span></span>
<span data-ttu-id="a9189-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a9189-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a9189-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a9189-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9189-139">-Território</span><span class="sxs-lookup"><span data-stu-id="a9189-139">-Realm</span></span>
<span data-ttu-id="a9189-140">Especifica a organização em uma ID organizacional.</span><span class="sxs-lookup"><span data-stu-id="a9189-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="a9189-141">Por exemplo, se você se conectar ao Azure como admin@contoso.com , o valor do parâmetro de **território** será contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a9189-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="a9189-142">Use esse parâmetro quando usar uma ID da organização para entrar no portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9189-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="a9189-143">Esse parâmetro não é necessário quando você usa uma conta da Microsoft, como uma conta do outlook.com ou do live.com.</span><span class="sxs-lookup"><span data-stu-id="a9189-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="a9189-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9189-144">CommonParameters</span></span>
<span data-ttu-id="a9189-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9189-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9189-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9189-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9189-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9189-147">INPUTS</span></span>

### <span data-ttu-id="a9189-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9189-148">None</span></span>
<span data-ttu-id="a9189-149">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="a9189-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a9189-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9189-150">OUTPUTS</span></span>

### <span data-ttu-id="a9189-151">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9189-151">None or System.Boolean</span></span>
<span data-ttu-id="a9189-152">Quando você usa o parâmetro *PassThru* , esse cmdlet retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="a9189-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="a9189-153">Caso contrário, esse cmdlet não retorna nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="a9189-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="a9189-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9189-154">NOTES</span></span>

## <span data-ttu-id="a9189-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9189-155">RELATED LINKS</span></span>

[<span data-ttu-id="a9189-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a9189-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="a9189-157">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a9189-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


