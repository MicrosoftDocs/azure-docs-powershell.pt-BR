---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284134"
---
# <span data-ttu-id="814b7-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="814b7-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="814b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="814b7-102">SYNOPSIS</span></span>
<span data-ttu-id="814b7-103">Modifica uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="814b7-103">Modifies an API Revision</span></span>

## <span data-ttu-id="814b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="814b7-104">SYNTAX</span></span>

### <span data-ttu-id="814b7-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="814b7-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="814b7-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="814b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="814b7-107">DESCRIPTION</span></span>
<span data-ttu-id="814b7-108">O cmdlet **set-AzApiManagementApiRevision** modifica uma revisão da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="814b7-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="814b7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="814b7-109">EXAMPLES</span></span>

### <span data-ttu-id="814b7-110">Exemplo 1: modificar uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="814b7-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="814b7-111">O cmdlet atualiza a `2` revisão da API `echo-api` com uma nova descrição, protocolo e caminho.</span><span class="sxs-lookup"><span data-stu-id="814b7-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="814b7-112">OS</span><span class="sxs-lookup"><span data-stu-id="814b7-112">PARAMETERS</span></span>

### <span data-ttu-id="814b7-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="814b7-113">-ApiId</span></span>
<span data-ttu-id="814b7-114">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="814b7-114">Identifier of existing API.</span></span>
<span data-ttu-id="814b7-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-115">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="814b7-116">-ApiRevision</span></span>
<span data-ttu-id="814b7-117">Identificador da revisão de API existente.</span><span class="sxs-lookup"><span data-stu-id="814b7-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="814b7-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-118">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="814b7-119">-AuthorizationScope</span></span>
<span data-ttu-id="814b7-120">Escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="814b7-120">OAuth operations scope.</span></span>
<span data-ttu-id="814b7-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-121">This parameter is optional.</span></span>
<span data-ttu-id="814b7-122">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-122">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="814b7-123">-AuthorizationServerId</span></span>
<span data-ttu-id="814b7-124">Identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="814b7-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="814b7-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-125">This parameter is optional.</span></span>
<span data-ttu-id="814b7-126">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-126">Default value is $null.</span></span>
<span data-ttu-id="814b7-127">Deve ser especificado se AuthorizationScope for especificado.</span><span class="sxs-lookup"><span data-stu-id="814b7-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="814b7-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="814b7-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="814b7-129">Mecanismo de servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="814b7-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="814b7-130">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="814b7-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="814b7-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-131">This parameter is optional.</span></span> <span data-ttu-id="814b7-132">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-132">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-133">-Contexto</span><span class="sxs-lookup"><span data-stu-id="814b7-133">-Context</span></span>
<span data-ttu-id="814b7-134">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="814b7-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="814b7-135">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-135">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814b7-136">-DefaultProfile</span></span>
<span data-ttu-id="814b7-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="814b7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="814b7-138">-Descrição</span><span class="sxs-lookup"><span data-stu-id="814b7-138">-Description</span></span>
<span data-ttu-id="814b7-139">Descrição da API Web.</span><span class="sxs-lookup"><span data-stu-id="814b7-139">Web API description.</span></span>
<span data-ttu-id="814b7-140">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="814b7-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="814b7-141">-InputObject</span></span>
<span data-ttu-id="814b7-142">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="814b7-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="814b7-143">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-143">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="814b7-144">-Name</span></span>
<span data-ttu-id="814b7-145">Nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="814b7-145">Web API name.</span></span>
<span data-ttu-id="814b7-146">Nome público da API como seria exibido nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="814b7-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="814b7-147">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-147">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="814b7-148">-OpenIdProviderId</span></span>
<span data-ttu-id="814b7-149">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="814b7-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="814b7-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-150">This parameter is optional.</span></span> <span data-ttu-id="814b7-151">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-151">Default value is $null.</span></span> <span data-ttu-id="814b7-152">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="814b7-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="814b7-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="814b7-153">-PassThru</span></span>
<span data-ttu-id="814b7-154">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement... Model. PsApiManagementApi que representa a API Set.</span><span class="sxs-lookup"><span data-stu-id="814b7-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="814b7-155">-Caminho</span><span class="sxs-lookup"><span data-stu-id="814b7-155">-Path</span></span>
<span data-ttu-id="814b7-156">Caminho de API Web.</span><span class="sxs-lookup"><span data-stu-id="814b7-156">Web API Path.</span></span>
<span data-ttu-id="814b7-157">Última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="814b7-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="814b7-158">Esta URL será usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="814b7-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="814b7-159">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="814b7-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="814b7-160">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-160">This parameter is optional.</span></span>
<span data-ttu-id="814b7-161">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-161">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-162">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="814b7-162">-Protocols</span></span>
<span data-ttu-id="814b7-163">Protocolos de API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="814b7-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="814b7-164">Protocolos em que a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="814b7-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="814b7-165">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-165">This parameter is required.</span></span>
<span data-ttu-id="814b7-166">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-166">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="814b7-167">-ServiceUrl</span></span>
<span data-ttu-id="814b7-168">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="814b7-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="814b7-169">Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.</span><span class="sxs-lookup"><span data-stu-id="814b7-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="814b7-170">Deve ter de 1 a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="814b7-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="814b7-171">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="814b7-171">This parameter is required.</span></span>

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

### <span data-ttu-id="814b7-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="814b7-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="814b7-173">Nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="814b7-173">Subscription key header name.</span></span>
<span data-ttu-id="814b7-174">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-174">This parameter is optional.</span></span>
<span data-ttu-id="814b7-175">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-175">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="814b7-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="814b7-177">Nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="814b7-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="814b7-178">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-178">This parameter is optional.</span></span>
<span data-ttu-id="814b7-179">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="814b7-179">Default value is $null.</span></span>

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

### <span data-ttu-id="814b7-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="814b7-180">-SubscriptionRequired</span></span>
<span data-ttu-id="814b7-181">Sinalizador para impor SubscriptionRequired para as solicitações à API.</span><span class="sxs-lookup"><span data-stu-id="814b7-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="814b7-182">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="814b7-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="814b7-183">-Confirme</span><span class="sxs-lookup"><span data-stu-id="814b7-183">-Confirm</span></span>
<span data-ttu-id="814b7-184">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="814b7-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814b7-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814b7-185">-WhatIf</span></span>
<span data-ttu-id="814b7-186">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="814b7-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="814b7-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="814b7-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814b7-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814b7-188">CommonParameters</span></span>
<span data-ttu-id="814b7-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="814b7-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814b7-190">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="814b7-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814b7-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="814b7-191">INPUTS</span></span>

### <span data-ttu-id="814b7-192">System. String</span><span class="sxs-lookup"><span data-stu-id="814b7-192">System.String</span></span>

### <span data-ttu-id="814b7-193">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="814b7-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="814b7-194">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="814b7-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="814b7-195">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="814b7-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="814b7-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="814b7-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="814b7-197">EXIBE</span><span class="sxs-lookup"><span data-stu-id="814b7-197">OUTPUTS</span></span>

### <span data-ttu-id="814b7-198">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="814b7-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="814b7-199">INFORMA</span><span class="sxs-lookup"><span data-stu-id="814b7-199">NOTES</span></span>

## <span data-ttu-id="814b7-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="814b7-200">RELATED LINKS</span></span>

[<span data-ttu-id="814b7-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="814b7-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="814b7-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="814b7-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="814b7-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="814b7-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)