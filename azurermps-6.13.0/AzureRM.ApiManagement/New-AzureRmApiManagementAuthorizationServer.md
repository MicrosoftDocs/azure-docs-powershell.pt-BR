---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 636391b427702b1b66dff284f8a16264bf1b1f12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428646"
---
# <span data-ttu-id="946a6-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="946a6-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="946a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="946a6-102">SYNOPSIS</span></span>
<span data-ttu-id="946a6-103">Cria um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="946a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="946a6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="946a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="946a6-105">DESCRIPTION</span></span>
<span data-ttu-id="946a6-106">O cmdlet **New-AzureRmApiManagementAuthorizationServer** cria um servidor de autorização de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="946a6-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="946a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="946a6-107">EXAMPLES</span></span>

### <span data-ttu-id="946a6-108">Exemplo 1: criar um servidor de autorização</span><span class="sxs-lookup"><span data-stu-id="946a6-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="946a6-109">Esse comando cria um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="946a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="946a6-110">PARAMETERS</span></span>

### <span data-ttu-id="946a6-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="946a6-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="946a6-112">Especifica uma matriz de métodos para enviar um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="946a6-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="946a6-113">psdx_paramvalues AuthorizationHeader e consulta.</span><span class="sxs-lookup"><span data-stu-id="946a6-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="946a6-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="946a6-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="946a6-115">Especifica o ponto de extremidade de autorização para autenticar proprietários de recursos e obter autorizações de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="946a6-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="946a6-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="946a6-117">Especifica uma matriz de métodos de solicitação de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="946a6-118">Os valores válidos são: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="946a6-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="946a6-119">O valor padrão é GET.</span><span class="sxs-lookup"><span data-stu-id="946a6-119">The default value is GET.</span></span>

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

### <span data-ttu-id="946a6-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="946a6-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="946a6-121">Especifica uma matriz de métodos de autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="946a6-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="946a6-122">psdx_paramvalues Basic e corpo.</span><span class="sxs-lookup"><span data-stu-id="946a6-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="946a6-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="946a6-123">-ClientId</span></span>
<span data-ttu-id="946a6-124">Especifica a ID do cliente do console de desenvolvedor que é o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="946a6-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="946a6-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="946a6-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="946a6-126">Especifica o ponto de extremidade de registro do cliente para registrar clientes com o servidor de autorização e obter credenciais do cliente.</span><span class="sxs-lookup"><span data-stu-id="946a6-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="946a6-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="946a6-127">-ClientSecret</span></span>
<span data-ttu-id="946a6-128">Especifica o segredo do cliente do console de desenvolvedor que é o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="946a6-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="946a6-129">-Contexto</span><span class="sxs-lookup"><span data-stu-id="946a6-129">-Context</span></span>
<span data-ttu-id="946a6-130">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="946a6-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="946a6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946a6-131">-DefaultProfile</span></span>
<span data-ttu-id="946a6-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="946a6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946a6-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="946a6-133">-DefaultScope</span></span>
<span data-ttu-id="946a6-134">Especifica o escopo padrão do servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="946a6-135">-Descrição</span><span class="sxs-lookup"><span data-stu-id="946a6-135">-Description</span></span>
<span data-ttu-id="946a6-136">Especifica uma descrição para um servidor de autorização.</span><span class="sxs-lookup"><span data-stu-id="946a6-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="946a6-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="946a6-137">-GrantTypes</span></span>
<span data-ttu-id="946a6-138">Especifica uma matriz de tipos de concessão.</span><span class="sxs-lookup"><span data-stu-id="946a6-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="946a6-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="946a6-139">psdx_paramvalues</span></span>
- <span data-ttu-id="946a6-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="946a6-140">AuthorizationCode</span></span>
- <span data-ttu-id="946a6-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="946a6-141">ClientCredentials</span></span> 
- <span data-ttu-id="946a6-142">Implícito</span><span class="sxs-lookup"><span data-stu-id="946a6-142">Implicit</span></span> 
- <span data-ttu-id="946a6-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="946a6-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="946a6-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="946a6-144">-Name</span></span>
<span data-ttu-id="946a6-145">Especifica o nome do servidor de autorização a ser criado.</span><span class="sxs-lookup"><span data-stu-id="946a6-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="946a6-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="946a6-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="946a6-147">Especifica a senha de proprietário do recurso.</span><span class="sxs-lookup"><span data-stu-id="946a6-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="946a6-148">Você deve especificar esse parâmetro é necessário se ResourceOwnerPassword for especificado pelo parâmetro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="946a6-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="946a6-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="946a6-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="946a6-150">Especifica o nome de usuário do proprietário do recurso.</span><span class="sxs-lookup"><span data-stu-id="946a6-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="946a6-151">Você deve especificar esse parâmetro se ResourceOwnerPassword for especificado pelo parâmetro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="946a6-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="946a6-152">-ServerID</span><span class="sxs-lookup"><span data-stu-id="946a6-152">-ServerId</span></span>
<span data-ttu-id="946a6-153">Especifica a ID do servidor de autorização a ser criado.</span><span class="sxs-lookup"><span data-stu-id="946a6-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="946a6-154">-Supportstate</span><span class="sxs-lookup"><span data-stu-id="946a6-154">-SupportState</span></span>
<span data-ttu-id="946a6-155">Indica se o parâmetro de *estado* deve ser compatível.</span><span class="sxs-lookup"><span data-stu-id="946a6-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="946a6-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="946a6-156">-TokenBodyParameters</span></span>
<span data-ttu-id="946a6-157">Especifica parâmetros de corpo adicionais usando o formato **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="946a6-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="946a6-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="946a6-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="946a6-159">Especifica a URL de ponto de extremidade de token usada por clientes para obter tokens de acesso no Exchange para apresentar as autorizações de autorização ou os tokens de atualização.</span><span class="sxs-lookup"><span data-stu-id="946a6-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="946a6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946a6-160">CommonParameters</span></span>
<span data-ttu-id="946a6-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946a6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946a6-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946a6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946a6-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="946a6-163">INPUTS</span></span>

### <span data-ttu-id="946a6-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="946a6-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="946a6-165">System. String</span><span class="sxs-lookup"><span data-stu-id="946a6-165">System.String</span></span>

### <span data-ttu-id="946a6-166">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="946a6-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="946a6-167">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="946a6-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="946a6-168">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="946a6-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="946a6-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="946a6-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="946a6-170">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="946a6-170">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="946a6-171">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="946a6-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="946a6-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="946a6-172">OUTPUTS</span></span>

### <span data-ttu-id="946a6-173">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="946a6-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="946a6-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="946a6-174">NOTES</span></span>

## <span data-ttu-id="946a6-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="946a6-175">RELATED LINKS</span></span>