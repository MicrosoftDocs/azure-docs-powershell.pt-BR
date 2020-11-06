---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 684c68b1af37ae1ae64d8ce3d9ea5b35ec008a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431458"
---
# <span data-ttu-id="705fe-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="705fe-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="705fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="705fe-102">SYNOPSIS</span></span>
<span data-ttu-id="705fe-103">Modifica um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="705fe-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="705fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="705fe-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="705fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="705fe-105">DESCRIPTION</span></span>
<span data-ttu-id="705fe-106">O cmdlet **set-AzureRmApiManagementAuthorizationServer** modifica os detalhes do servidor de autorização do gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="705fe-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="705fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="705fe-107">EXAMPLES</span></span>

### <span data-ttu-id="705fe-108">Exemplo 1: modificar um servidor de autorização</span><span class="sxs-lookup"><span data-stu-id="705fe-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="705fe-109">Esse comando modifica o servidor de autorização de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="705fe-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="705fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="705fe-110">PARAMETERS</span></span>

### <span data-ttu-id="705fe-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="705fe-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="705fe-112">Especifica uma matriz de métodos para enviar um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="705fe-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="705fe-113">psdx_paramvalues AuthorizationHeader e consulta.</span><span class="sxs-lookup"><span data-stu-id="705fe-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="705fe-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="705fe-115">Especifica o ponto de extremidade de autorização para autenticar proprietários de recursos e obter autorizações de autorização.</span><span class="sxs-lookup"><span data-stu-id="705fe-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="705fe-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="705fe-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="705fe-117">Especifica uma matriz de métodos de solicitação de autorização.</span><span class="sxs-lookup"><span data-stu-id="705fe-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="705fe-118">psdx_paramvalues GET e POST.</span><span class="sxs-lookup"><span data-stu-id="705fe-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="705fe-119">O valor padrão é GET.</span><span class="sxs-lookup"><span data-stu-id="705fe-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="705fe-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="705fe-121">Especifica uma matriz de métodos de autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="705fe-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="705fe-122">psdx_paramvalues Basic e corpo.</span><span class="sxs-lookup"><span data-stu-id="705fe-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="705fe-123">-ClientId</span></span>
<span data-ttu-id="705fe-124">Especifica a ID do cliente do console de desenvolvedor que é o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="705fe-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="705fe-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="705fe-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="705fe-126">Especifica o ponto de extremidade de registro do cliente para registrar clientes com o servidor de autorização e obter credenciais do cliente.</span><span class="sxs-lookup"><span data-stu-id="705fe-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="705fe-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="705fe-127">-ClientSecret</span></span>
<span data-ttu-id="705fe-128">Especifica o segredo do cliente do console de desenvolvedor que é o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="705fe-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="705fe-129">-Contexto</span><span class="sxs-lookup"><span data-stu-id="705fe-129">-Context</span></span>
<span data-ttu-id="705fe-130">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="705fe-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705fe-131">-DefaultProfile</span></span>
<span data-ttu-id="705fe-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="705fe-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="705fe-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="705fe-133">-DefaultScope</span></span>
<span data-ttu-id="705fe-134">Especifica o escopo padrão do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="705fe-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="705fe-135">-Descrição</span><span class="sxs-lookup"><span data-stu-id="705fe-135">-Description</span></span>
<span data-ttu-id="705fe-136">Especifica uma descrição para um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="705fe-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="705fe-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="705fe-137">-GrantTypes</span></span>
<span data-ttu-id="705fe-138">Especifica uma matriz de tipos de concessão.</span><span class="sxs-lookup"><span data-stu-id="705fe-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="705fe-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="705fe-139">psdx_paramvalues</span></span>
- <span data-ttu-id="705fe-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="705fe-140">AuthorizationCode</span></span>
- <span data-ttu-id="705fe-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="705fe-141">ClientCredentials</span></span> 
- <span data-ttu-id="705fe-142">Implícito</span><span class="sxs-lookup"><span data-stu-id="705fe-142">Implicit</span></span> 
- <span data-ttu-id="705fe-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="705fe-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="705fe-144">-Name</span></span>
<span data-ttu-id="705fe-145">Especifica o nome do servidor de autorização a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="705fe-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="705fe-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="705fe-146">-PassThru</span></span>
<span data-ttu-id="705fe-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="705fe-147">passthru</span></span>

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

### <span data-ttu-id="705fe-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="705fe-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="705fe-149">Especifica a senha de proprietário do recurso.</span><span class="sxs-lookup"><span data-stu-id="705fe-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="705fe-150">Você deve especificar esse parâmetro se ResourceOwnerPassword for especificado pelo parâmetro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="705fe-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="705fe-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="705fe-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="705fe-152">Especifica o nome de usuário do proprietário do recurso.</span><span class="sxs-lookup"><span data-stu-id="705fe-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="705fe-153">Você deve especificar esse parâmetro se ResourceOwnerPassword for especificado pelo parâmetro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="705fe-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="705fe-154">-ServerID</span><span class="sxs-lookup"><span data-stu-id="705fe-154">-ServerId</span></span>
<span data-ttu-id="705fe-155">Especifica a ID do servidor de autorização a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="705fe-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="705fe-156">-Supportstate</span><span class="sxs-lookup"><span data-stu-id="705fe-156">-SupportState</span></span>
<span data-ttu-id="705fe-157">Indica se o parâmetro de *estado* deve ser compatível.</span><span class="sxs-lookup"><span data-stu-id="705fe-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="705fe-158">-TokenBodyParameters</span></span>
<span data-ttu-id="705fe-159">Especifica parâmetros de corpo adicionais usando o formato application/x-www-form-urlencoded.</span><span class="sxs-lookup"><span data-stu-id="705fe-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705fe-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="705fe-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="705fe-161">Especifica o ponto de extremidade do token para os clientes obterem tokens de acesso no Exchange para apresentar as autorizações de autorização ou atualizar tokens.</span><span class="sxs-lookup"><span data-stu-id="705fe-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="705fe-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705fe-162">CommonParameters</span></span>
<span data-ttu-id="705fe-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705fe-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705fe-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705fe-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705fe-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="705fe-165">INPUTS</span></span>

### <span data-ttu-id="705fe-166">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="705fe-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="705fe-167">System. String</span><span class="sxs-lookup"><span data-stu-id="705fe-167">System.String</span></span>

### <span data-ttu-id="705fe-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="705fe-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="705fe-169">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="705fe-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="705fe-170">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="705fe-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="705fe-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="705fe-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="705fe-172">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="705fe-172">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="705fe-173">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="705fe-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="705fe-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="705fe-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="705fe-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="705fe-175">OUTPUTS</span></span>

### <span data-ttu-id="705fe-176">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="705fe-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="705fe-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="705fe-177">NOTES</span></span>

## <span data-ttu-id="705fe-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="705fe-178">RELATED LINKS</span></span>

[<span data-ttu-id="705fe-179">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="705fe-179">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="705fe-180">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="705fe-180">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="705fe-181">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="705fe-181">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


