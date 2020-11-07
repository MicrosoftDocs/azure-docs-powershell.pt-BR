---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946396"
---
# <span data-ttu-id="4f4f1-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="4f4f1-101">Add-AzureAccount</span></span>

## <span data-ttu-id="4f4f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4f1-103">Adiciona a conta do Azure ao Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="4f4f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f4f1-104">SYNTAX</span></span>

### <span data-ttu-id="4f4f1-105">Usuário (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f4f1-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f4f1-106">ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4f4f1-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f4f1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f4f1-107">DESCRIPTION</span></span>
<span data-ttu-id="4f4f1-108">O cmdlet **Add-AzureAccount** torna sua conta do Azure e suas assinaturas disponíveis no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="4f4f1-109">É como se conectar à sua conta do Azure no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="4f4f1-110">Para fazer logout da conta, use o cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="4f4f1-111">**Add-AzureAccount** baixa informações sobre a sua conta do Azure e salva-as em um arquivo de dados de assinatura em seu perfil de usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="4f4f1-112">Ele também obtém um token de acesso que permite que o Windows PowerShell acesse sua conta do Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="4f4f1-113">Quando o comando é concluído, você pode gerenciar sua conta do Azure no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="4f4f1-114">Há duas maneiras diferentes de disponibilizar sua conta do Azure para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="4f4f1-115">Você pode usar o cmdlet **Add-AzureAccount** , que usa tokens de acesso de autenticação do Azure Active Directory (Azure AD) ou **Import-AzurePublishSettingsFile** , que usa um certificado de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="4f4f1-116">Para obter orientação sobre qual método usar, consulte [como: conectar-se à sua assinatura](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="4f4f1-117">Quando você executa **Add-AzureAccount** , ele exibe uma janela interativa que solicita que você entre na sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="4f4f1-118">Esta entrada é válida até que o token de acesso expire.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="4f4f1-119">Quando expira, os cmdlets que exigem acesso à sua conta solicitam que você execute **Add-AzureAccount** novamente.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="4f4f1-120">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4f4f1-121">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="4f4f1-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f4f1-122">EXAMPLES</span></span>

### <span data-ttu-id="4f4f1-123">Exemplo 1: adicionar uma conta</span><span class="sxs-lookup"><span data-stu-id="4f4f1-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="4f4f1-124">Esse comando adiciona uma conta do Azure ao Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="4f4f1-125">Quando você executa o comando, um Windows é exibido para solicitar o nome de usuário e a senha da conta.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="4f4f1-126">Exemplo 2: usar um arquivo de dados de assinatura alternativo</span><span class="sxs-lookup"><span data-stu-id="4f4f1-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="4f4f1-127">Esse comando usa o parâmetro **SubscriptionDataFile** para o **Add-AzureAccount** direto para armazenar os dados da conta no arquivo C:\Testing\SDF.xml, em vez do arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="4f4f1-128">OS</span><span class="sxs-lookup"><span data-stu-id="4f4f1-128">PARAMETERS</span></span>

### <span data-ttu-id="4f4f1-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="4f4f1-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f1-130">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="4f4f1-130">-Environment</span></span>
<span data-ttu-id="4f4f1-131">Especifica um ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="4f4f1-132">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="4f4f1-133">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="4f4f1-134">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="4f4f1-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4f4f1-135">-Profile</span></span>
<span data-ttu-id="4f4f1-136">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4f4f1-137">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f4f1-138">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="4f4f1-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f1-139">-Locatário</span><span class="sxs-lookup"><span data-stu-id="4f4f1-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4f1-140">CommonParameters</span></span>
<span data-ttu-id="4f4f1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4f1-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4f1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f4f1-143">INPUTS</span></span>

### <span data-ttu-id="4f4f1-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f4f1-144">None</span></span>
<span data-ttu-id="4f4f1-145">Não é possível canalizar a entrada para este cmdlet</span><span class="sxs-lookup"><span data-stu-id="4f4f1-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="4f4f1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f4f1-146">OUTPUTS</span></span>

### <span data-ttu-id="4f4f1-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f4f1-147">None</span></span>
<span data-ttu-id="4f4f1-148">Esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="4f4f1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f4f1-149">NOTES</span></span>
* <span data-ttu-id="4f4f1-150">**Add-AzureAccount** (e o método de autenticação do Azure AD) tem precedência sobre **Import-AzurePublishSettings** (e o método de certificado de gerenciamento).</span><span class="sxs-lookup"><span data-stu-id="4f4f1-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="4f4f1-151">Se você usar **Add-AzureAccount** mesmo uma vez na sua conta, o método de autenticação do Azure ad será usado e o certificado de gerenciamento será ignorado.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="4f4f1-152">Para remover o token do Azure AD e restaurar o método de certificado de gerenciamento, use o cmdlet **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="4f4f1-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="4f4f1-153">Para obter mais informações, digite: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="4f4f1-154">O erro, "suas credenciais venceram.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="4f4f1-155">Use Add-AzureAccount para entrar novamente. "</span><span class="sxs-lookup"><span data-stu-id="4f4f1-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="4f4f1-156">indica que o token de acesso expirou e o Windows PowerShell não pode acessar sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="4f4f1-157">Para restaurar o acesso à sua conta, execute **Add-AzureAccount** novamente.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="4f4f1-158">Os cmdlets da assinatura e da conta do PowerShell do Azure recebem seus dados do arquivo de dados de assinatura, e não da conta do Azure ao vivo.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="4f4f1-159">Se você alterar sua conta ou assinaturas fora do Windows PowerShell, por exemplo, usando o portal de gerenciamento do Azure, execute **Add-AzureAccount** novamente para atualizar o arquivo de dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4f4f1-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="4f4f1-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f4f1-160">RELATED LINKS</span></span>

[<span data-ttu-id="4f4f1-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f4f1-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="4f4f1-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f4f1-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="4f4f1-163">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4f4f1-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="4f4f1-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="4f4f1-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="4f4f1-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="4f4f1-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


