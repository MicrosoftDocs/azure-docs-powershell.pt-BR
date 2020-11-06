---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597937"
---
# <span data-ttu-id="a9621-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a9621-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a9621-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9621-102">SYNOPSIS</span></span>
<span data-ttu-id="a9621-103">Atualiza a configuração de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a9621-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="a9621-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9621-104">SYNTAX</span></span>

### <span data-ttu-id="a9621-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9621-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9621-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9621-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9621-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9621-107">DESCRIPTION</span></span>
<span data-ttu-id="a9621-108">Atualiza a configuração de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a9621-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="a9621-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9621-109">EXAMPLES</span></span>

### <span data-ttu-id="a9621-110">Exemplo 1: atualizar o provedor de identidade do Facebook</span><span class="sxs-lookup"><span data-stu-id="a9621-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="a9621-111">O cmdlet atualiza o segredo do cliente do provedor de identidade do Facebook;</span><span class="sxs-lookup"><span data-stu-id="a9621-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="a9621-112">OS</span><span class="sxs-lookup"><span data-stu-id="a9621-112">PARAMETERS</span></span>

### <span data-ttu-id="a9621-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="a9621-113">-AllowedTenants</span></span>
<span data-ttu-id="a9621-114">Lista de locatários do Azure Active Directory permitidos.</span><span class="sxs-lookup"><span data-stu-id="a9621-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="a9621-115">-Autoridade</span><span class="sxs-lookup"><span data-stu-id="a9621-115">-Authority</span></span>
<span data-ttu-id="a9621-116">Nome do ponto de extremidade de descoberta do OpenID Connect para AAD ou AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9621-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="a9621-117">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9621-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9621-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a9621-118">-ClientId</span></span>
<span data-ttu-id="a9621-119">ID do cliente do aplicativo no provedor de identidade externa.</span><span class="sxs-lookup"><span data-stu-id="a9621-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="a9621-120">Ele é uma ID do aplicativo para o logon do Facebook, ID de cliente para o Google login, ID do aplicativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9621-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="a9621-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a9621-121">-ClientSecret</span></span>
<span data-ttu-id="a9621-122">Segredo do cliente do aplicativo no provedor de identidade externa, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="a9621-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="a9621-123">Por exemplo, é o segredo do aplicativo para o logon do Facebook, a chave de API do Google login, a chave pública para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9621-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="a9621-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a9621-124">-Context</span></span>
<span data-ttu-id="a9621-125">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a9621-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9621-126">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a9621-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9621-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9621-127">-DefaultProfile</span></span>
<span data-ttu-id="a9621-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9621-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9621-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9621-129">-InputObject</span></span>
<span data-ttu-id="a9621-130">Instância do PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="a9621-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="a9621-131">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a9621-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9621-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9621-132">-PassThru</span></span>
<span data-ttu-id="a9621-133">Indica que esse cmdlet retorna o  **PsApiManagementIdentityProvider** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a9621-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9621-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="a9621-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="a9621-135">Nome da política de redefinição de senha.</span><span class="sxs-lookup"><span data-stu-id="a9621-135">Password Reset Policy Name.</span></span> <span data-ttu-id="a9621-136">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9621-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="a9621-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9621-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9621-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="a9621-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="a9621-139">Nome da política de edição do perfil.</span><span class="sxs-lookup"><span data-stu-id="a9621-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="a9621-140">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9621-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="a9621-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9621-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9621-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="a9621-142">-SigninPolicyName</span></span>
<span data-ttu-id="a9621-143">Nome da política de entrada.</span><span class="sxs-lookup"><span data-stu-id="a9621-143">Signin Policy Name.</span></span> <span data-ttu-id="a9621-144">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9621-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="a9621-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9621-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9621-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="a9621-146">-SignupPolicyName</span></span>
<span data-ttu-id="a9621-147">Nome da política de inscrição.</span><span class="sxs-lookup"><span data-stu-id="a9621-147">Signup Policy Name.</span></span> <span data-ttu-id="a9621-148">Aplica-se somente ao provedor de identidade do AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9621-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="a9621-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9621-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9621-150">-Digite</span><span class="sxs-lookup"><span data-stu-id="a9621-150">-Type</span></span>
<span data-ttu-id="a9621-151">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="a9621-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="a9621-152">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a9621-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9621-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9621-153">-Confirm</span></span>
<span data-ttu-id="a9621-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9621-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9621-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9621-155">-WhatIf</span></span>
<span data-ttu-id="a9621-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9621-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9621-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9621-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9621-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9621-158">CommonParameters</span></span>
<span data-ttu-id="a9621-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9621-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9621-160">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9621-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9621-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9621-161">INPUTS</span></span>

### <span data-ttu-id="a9621-162">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a9621-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9621-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a9621-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="a9621-164">System. String</span><span class="sxs-lookup"><span data-stu-id="a9621-164">System.String</span></span>

### <span data-ttu-id="a9621-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="a9621-165">System.String[]</span></span>

### <span data-ttu-id="a9621-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9621-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9621-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9621-167">OUTPUTS</span></span>

### <span data-ttu-id="a9621-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a9621-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a9621-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9621-169">NOTES</span></span>

## <span data-ttu-id="a9621-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9621-170">RELATED LINKS</span></span>

[<span data-ttu-id="a9621-171">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a9621-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a9621-172">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a9621-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a9621-173">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a9621-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
