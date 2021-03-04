---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 31a635c5965d40cf12e77d556e987c08dfb7175a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890677"
---
# <span data-ttu-id="b737d-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b737d-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b737d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b737d-102">SYNOPSIS</span></span>
<span data-ttu-id="b737d-103">Cria uma nova configuração do Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="b737d-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b737d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b737d-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b737d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b737d-105">DESCRIPTION</span></span>
<span data-ttu-id="b737d-106">Cria uma nova configuração do Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="b737d-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b737d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b737d-107">EXAMPLES</span></span>

### <span data-ttu-id="b737d-108">Exemplo 1: configura o Facebook como um provedor de identidade para logons do Portal do Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="b737d-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="b737d-109">Este comando configura a Identidade do Facebook como um Provedor de Identidade aceito no Portal do Desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b737d-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b737d-110">Isso leva como entrada ClientId e ClientSecret do aplicativo do Facebook.</span><span class="sxs-lookup"><span data-stu-id="b737d-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="b737d-111">Exemplo 2: configura o adB2C como um provedor de identidade para logons do Portal do Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="b737d-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="b737d-112">Este comando configura a Identidade do Facebook como um Provedor de Identidade aceito no Portal do Desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b737d-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b737d-113">Isso leva como entrada ClientId e ClientSecret do aplicativo do Facebook.</span><span class="sxs-lookup"><span data-stu-id="b737d-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="b737d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b737d-114">PARAMETERS</span></span>

### <span data-ttu-id="b737d-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="b737d-115">-AllowedTenants</span></span>
<span data-ttu-id="b737d-116">Lista de locatários permitidos do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b737d-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="b737d-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="b737d-117">-Authority</span></span>
<span data-ttu-id="b737d-118">Nome do host do ponto de extremidade de descoberta do OpenID Connect para AAD ou AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="b737d-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="b737d-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="b737d-120">-ClientId</span></span>
<span data-ttu-id="b737d-121">ID do cliente do Aplicativo no Provedor de Identidade externo.</span><span class="sxs-lookup"><span data-stu-id="b737d-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="b737d-122">É iD do aplicativo para logon do Facebook, ID do cliente para logon do Google, ID do aplicativo para Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b737d-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="b737d-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b737d-123">-ClientSecret</span></span>
<span data-ttu-id="b737d-124">Segredo do cliente do Aplicativo no Provedor de Identidade externo, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="b737d-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="b737d-125">Por exemplo, é o App Secret para logon do Facebook, CHAVE da API para logon do Google, Chave Pública para Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b737d-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="b737d-126">-Context</span><span class="sxs-lookup"><span data-stu-id="b737d-126">-Context</span></span>
<span data-ttu-id="b737d-127">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b737d-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b737d-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b737d-128">This parameter is required.</span></span>

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

### <span data-ttu-id="b737d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b737d-129">-DefaultProfile</span></span>
<span data-ttu-id="b737d-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b737d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b737d-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="b737d-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="b737d-132">Nome da Política de Redefinição de Senha.</span><span class="sxs-lookup"><span data-stu-id="b737d-132">Password Reset Policy Name.</span></span> <span data-ttu-id="b737d-133">Aplica-se apenas ao Provedor de Identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="b737d-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b737d-134">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="b737d-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="b737d-136">Nome da Política de Edição de Perfil.</span><span class="sxs-lookup"><span data-stu-id="b737d-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="b737d-137">Aplica-se apenas ao Provedor de Identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="b737d-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b737d-138">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="b737d-139">-SigninPolicyName</span></span>
<span data-ttu-id="b737d-140">Nome da política de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b737d-140">Signin Policy Name.</span></span> <span data-ttu-id="b737d-141">Aplica-se apenas ao Provedor de Identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="b737d-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b737d-142">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="b737d-143">-SigninTenant</span></span>
<span data-ttu-id="b737d-144">Locatário de signin para substituir no AAD B2C em vez do `common` Locatário</span><span class="sxs-lookup"><span data-stu-id="b737d-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="b737d-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="b737d-145">-SignupPolicyName</span></span>
<span data-ttu-id="b737d-146">Nome da Política de Assinatura.</span><span class="sxs-lookup"><span data-stu-id="b737d-146">Signup Policy Name.</span></span> <span data-ttu-id="b737d-147">Aplica-se apenas ao Provedor de Identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="b737d-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b737d-148">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-149">-Type</span><span class="sxs-lookup"><span data-stu-id="b737d-149">-Type</span></span>
<span data-ttu-id="b737d-150">Identificador de um Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="b737d-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b737d-151">Se especificado, tentará encontrar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="b737d-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b737d-152">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b737d-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="b737d-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b737d-153">-Confirm</span></span>
<span data-ttu-id="b737d-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b737d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b737d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b737d-155">-WhatIf</span></span>
<span data-ttu-id="b737d-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b737d-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b737d-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b737d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b737d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b737d-158">CommonParameters</span></span>
<span data-ttu-id="b737d-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b737d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b737d-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b737d-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b737d-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b737d-161">INPUTS</span></span>

### <span data-ttu-id="b737d-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b737d-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b737d-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b737d-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="b737d-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b737d-164">System.String</span></span>

### <span data-ttu-id="b737d-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b737d-165">System.String[]</span></span>

## <span data-ttu-id="b737d-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b737d-166">OUTPUTS</span></span>

### <span data-ttu-id="b737d-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b737d-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b737d-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="b737d-168">NOTES</span></span>

## <span data-ttu-id="b737d-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b737d-169">RELATED LINKS</span></span>

[<span data-ttu-id="b737d-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b737d-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b737d-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b737d-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b737d-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b737d-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
