---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272226"
---
# <span data-ttu-id="037ce-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="037ce-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="037ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="037ce-102">SYNOPSIS</span></span>
<span data-ttu-id="037ce-103">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="037ce-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="037ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="037ce-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="037ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="037ce-105">DESCRIPTION</span></span>
<span data-ttu-id="037ce-106">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="037ce-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="037ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="037ce-107">EXAMPLES</span></span>

### <span data-ttu-id="037ce-108">Exemplo 1: configura o Facebook como um provedor de identidade para logons do portal do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="037ce-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="037ce-109">Esse comando configura a identidade do Facebook como um provedor de identidade aceito no portal do desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="037ce-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="037ce-110">Isso aceita como entrada de ClientId e ClientSecret do aplicativo Facebook.</span><span class="sxs-lookup"><span data-stu-id="037ce-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="037ce-111">Exemplo 2: configura o adB2C como um provedor de identidade para logons do portal do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="037ce-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="037ce-112">Esse comando configura a identidade do Facebook como um provedor de identidade aceito no portal do desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="037ce-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="037ce-113">Isso aceita como entrada de ClientId e ClientSecret do aplicativo Facebook.</span><span class="sxs-lookup"><span data-stu-id="037ce-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="037ce-114">OS</span><span class="sxs-lookup"><span data-stu-id="037ce-114">PARAMETERS</span></span>

### <span data-ttu-id="037ce-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="037ce-115">-AllowedTenants</span></span>
<span data-ttu-id="037ce-116">Lista de locatários do Azure Active Directory permitidos</span><span class="sxs-lookup"><span data-stu-id="037ce-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-117">-Autoridade</span><span class="sxs-lookup"><span data-stu-id="037ce-117">-Authority</span></span>
<span data-ttu-id="037ce-118">Nome do ponto de extremidade de descoberta do OpenID Connect para AAD ou AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="037ce-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="037ce-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="037ce-120">-ClientId</span></span>
<span data-ttu-id="037ce-121">ID do cliente do aplicativo no provedor de identidade externa.</span><span class="sxs-lookup"><span data-stu-id="037ce-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="037ce-122">Ele é uma ID do aplicativo para o logon do Facebook, ID de cliente para o Google login, ID do aplicativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="037ce-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="037ce-123">-ClientSecret</span></span>
<span data-ttu-id="037ce-124">Segredo do cliente do aplicativo no provedor de identidade externa, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="037ce-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="037ce-125">Por exemplo, é o segredo do aplicativo para o logon do Facebook, a chave de API do Google login, a chave pública para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="037ce-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-126">-Contexto</span><span class="sxs-lookup"><span data-stu-id="037ce-126">-Context</span></span>
<span data-ttu-id="037ce-127">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="037ce-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="037ce-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="037ce-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037ce-129">-DefaultProfile</span></span>
<span data-ttu-id="037ce-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="037ce-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="037ce-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="037ce-132">Nome da política de redefinição de senha.</span><span class="sxs-lookup"><span data-stu-id="037ce-132">Password Reset Policy Name.</span></span> <span data-ttu-id="037ce-133">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="037ce-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="037ce-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="037ce-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="037ce-136">Nome da política de edição do perfil.</span><span class="sxs-lookup"><span data-stu-id="037ce-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="037ce-137">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="037ce-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="037ce-138">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="037ce-139">-SigninPolicyName</span></span>
<span data-ttu-id="037ce-140">Nome da política de entrada.</span><span class="sxs-lookup"><span data-stu-id="037ce-140">Signin Policy Name.</span></span> <span data-ttu-id="037ce-141">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="037ce-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="037ce-142">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="037ce-143">-SigninTenant</span></span>
<span data-ttu-id="037ce-144">Locatário de entrada para substituir no AAD B2C em vez do `common` locatário</span><span class="sxs-lookup"><span data-stu-id="037ce-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="037ce-145">-SignupPolicyName</span></span>
<span data-ttu-id="037ce-146">Nome da política de inscrição.</span><span class="sxs-lookup"><span data-stu-id="037ce-146">Signup Policy Name.</span></span> <span data-ttu-id="037ce-147">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="037ce-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="037ce-148">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-149">-Digite</span><span class="sxs-lookup"><span data-stu-id="037ce-149">-Type</span></span>
<span data-ttu-id="037ce-150">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="037ce-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="037ce-151">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="037ce-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="037ce-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="037ce-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="037ce-153">-Confirm</span></span>
<span data-ttu-id="037ce-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="037ce-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037ce-155">-WhatIf</span></span>
<span data-ttu-id="037ce-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="037ce-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="037ce-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="037ce-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037ce-158">CommonParameters</span></span>
<span data-ttu-id="037ce-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037ce-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037ce-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="037ce-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037ce-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="037ce-161">INPUTS</span></span>

### <span data-ttu-id="037ce-162">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="037ce-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="037ce-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="037ce-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="037ce-164">System. String</span><span class="sxs-lookup"><span data-stu-id="037ce-164">System.String</span></span>

### <span data-ttu-id="037ce-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="037ce-165">System.String[]</span></span>

## <span data-ttu-id="037ce-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="037ce-166">OUTPUTS</span></span>

### <span data-ttu-id="037ce-167">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="037ce-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="037ce-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="037ce-168">NOTES</span></span>

## <span data-ttu-id="037ce-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="037ce-169">RELATED LINKS</span></span>

[<span data-ttu-id="037ce-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="037ce-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="037ce-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="037ce-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="037ce-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="037ce-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
