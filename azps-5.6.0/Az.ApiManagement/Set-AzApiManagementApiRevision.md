---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: b8eac81d90f20617399048464ecca40e0df8d93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887075"
---
# <span data-ttu-id="c2c6c-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c2c6c-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="c2c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c6c-103">Modifica uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="c2c6c-103">Modifies an API Revision</span></span>

## <span data-ttu-id="c2c6c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c2c6c-104">SYNTAX</span></span>

### <span data-ttu-id="c2c6c-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c2c6c-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c6c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2c6c-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c6c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c2c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c6c-108">O cmdlet **Set-AzApiManagementApiRevision** modifica uma Revisão da API de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="c2c6c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-109">EXAMPLES</span></span>

### <span data-ttu-id="c2c6c-110">Exemplo 1: Modificar uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="c2c6c-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="c2c6c-111">O cmdlet atualiza `2` a revisão da API com uma nova `echo-api` descrição, protocolo e caminho.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="c2c6c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-112">PARAMETERS</span></span>

### <span data-ttu-id="c2c6c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c2c6c-113">-ApiId</span></span>
<span data-ttu-id="c2c6c-114">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-114">Identifier of existing API.</span></span>
<span data-ttu-id="c2c6c-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6c-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c2c6c-116">-ApiRevision</span></span>
<span data-ttu-id="c2c6c-117">Identificador da Revisão de API existente.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="c2c6c-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6c-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="c2c6c-119">-AuthorizationScope</span></span>
<span data-ttu-id="c2c6c-120">Escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-120">OAuth operations scope.</span></span>
<span data-ttu-id="c2c6c-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-121">This parameter is optional.</span></span>
<span data-ttu-id="c2c6c-122">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-122">Default value is $null.</span></span>

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

### <span data-ttu-id="c2c6c-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="c2c6c-123">-AuthorizationServerId</span></span>
<span data-ttu-id="c2c6c-124">Identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="c2c6c-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-125">This parameter is optional.</span></span>
<span data-ttu-id="c2c6c-126">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-126">Default value is $null.</span></span>
<span data-ttu-id="c2c6c-127">Deve ser especificado se AuthorizationScope especificado.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="c2c6c-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="c2c6c-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="c2c6c-129">Mecanismo do servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="c2c6c-130">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="c2c6c-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="c2c6c-131">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-131">This parameter is optional.</span></span> <span data-ttu-id="c2c6c-132">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-132">Default value is $null.</span></span>

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

### <span data-ttu-id="c2c6c-133">-Context</span><span class="sxs-lookup"><span data-stu-id="c2c6c-133">-Context</span></span>
<span data-ttu-id="c2c6c-134">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c2c6c-135">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-135">This parameter is required.</span></span>

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

### <span data-ttu-id="c2c6c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c6c-136">-DefaultProfile</span></span>
<span data-ttu-id="c2c6c-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2c6c-138">-Description</span><span class="sxs-lookup"><span data-stu-id="c2c6c-138">-Description</span></span>
<span data-ttu-id="c2c6c-139">Descrição da API Web.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-139">Web API description.</span></span>
<span data-ttu-id="c2c6c-140">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="c2c6c-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2c6c-141">-InputObject</span></span>
<span data-ttu-id="c2c6c-142">Instância de PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="c2c6c-143">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6c-144">-Name</span><span class="sxs-lookup"><span data-stu-id="c2c6c-144">-Name</span></span>
<span data-ttu-id="c2c6c-145">Nome da API Da Web.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-145">Web API name.</span></span>
<span data-ttu-id="c2c6c-146">Nome público da API, como seria exibido nos portais de desenvolvedor e administrador.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="c2c6c-147">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-147">This parameter is required.</span></span>

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

### <span data-ttu-id="c2c6c-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="c2c6c-148">-OpenIdProviderId</span></span>
<span data-ttu-id="c2c6c-149">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="c2c6c-150">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-150">This parameter is optional.</span></span> <span data-ttu-id="c2c6c-151">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-151">Default value is $null.</span></span> <span data-ttu-id="c2c6c-152">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="c2c6c-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2c6c-153">-PassThru</span></span>
<span data-ttu-id="c2c6c-154">Se especificado, em seguida, instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi que representa a API definida.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="c2c6c-155">-Path</span><span class="sxs-lookup"><span data-stu-id="c2c6c-155">-Path</span></span>
<span data-ttu-id="c2c6c-156">Caminho da API da Web.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-156">Web API Path.</span></span>
<span data-ttu-id="c2c6c-157">Última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="c2c6c-158">Essa URL será usada pelos consumidores de API para o envio de solicitações para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="c2c6c-159">Deve ter de 1 a 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="c2c6c-160">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-160">This parameter is optional.</span></span>
<span data-ttu-id="c2c6c-161">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-161">Default value is $null.</span></span>

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

### <span data-ttu-id="c2c6c-162">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="c2c6c-162">-Protocols</span></span>
<span data-ttu-id="c2c6c-163">Protocolos de API Da Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="c2c6c-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="c2c6c-164">Protocolos sobre qual API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="c2c6c-165">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-165">This parameter is required.</span></span>
<span data-ttu-id="c2c6c-166">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-166">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c6c-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="c2c6c-167">-ServiceUrl</span></span>
<span data-ttu-id="c2c6c-168">Uma URL do serviço Web expondo a API.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="c2c6c-169">Essa URL será usada apenas pelo Gerenciamento de API do Azure e não será pública.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="c2c6c-170">Deve ter de 1 a 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="c2c6c-171">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-171">This parameter is required.</span></span>

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

### <span data-ttu-id="c2c6c-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="c2c6c-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="c2c6c-173">Nome do header da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-173">Subscription key header name.</span></span>
<span data-ttu-id="c2c6c-174">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-174">This parameter is optional.</span></span>
<span data-ttu-id="c2c6c-175">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-175">Default value is $null.</span></span>

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

### <span data-ttu-id="c2c6c-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="c2c6c-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="c2c6c-177">Nome do parâmetro de cadeia de caracteres de consulta de chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="c2c6c-178">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-178">This parameter is optional.</span></span>
<span data-ttu-id="c2c6c-179">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-179">Default value is $null.</span></span>

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

### <span data-ttu-id="c2c6c-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c2c6c-180">-SubscriptionRequired</span></span>
<span data-ttu-id="c2c6c-181">Sinalizador para impor SubscriptionRequired para solicitações à Api.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="c2c6c-182">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="c2c6c-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2c6c-183">-Confirm</span></span>
<span data-ttu-id="c2c6c-184">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c6c-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c6c-185">-WhatIf</span></span>
<span data-ttu-id="c2c6c-186">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c6c-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c6c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c6c-188">CommonParameters</span></span>
<span data-ttu-id="c2c6c-189">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c6c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c6c-190">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2c6c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c6c-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-191">INPUTS</span></span>

### <span data-ttu-id="c2c6c-192">System.String</span><span class="sxs-lookup"><span data-stu-id="c2c6c-192">System.String</span></span>

### <span data-ttu-id="c2c6c-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c2c6c-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c2c6c-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2c6c-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="c2c6c-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="c2c6c-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="c2c6c-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2c6c-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2c6c-197">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-197">OUTPUTS</span></span>

### <span data-ttu-id="c2c6c-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2c6c-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c2c6c-199">NOTES</span><span class="sxs-lookup"><span data-stu-id="c2c6c-199">NOTES</span></span>

## <span data-ttu-id="c2c6c-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2c6c-200">RELATED LINKS</span></span>

[<span data-ttu-id="c2c6c-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c2c6c-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="c2c6c-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c2c6c-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="c2c6c-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c2c6c-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)