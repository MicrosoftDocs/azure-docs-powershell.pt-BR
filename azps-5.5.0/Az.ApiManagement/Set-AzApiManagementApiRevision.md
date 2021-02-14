---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127160"
---
# <span data-ttu-id="79fd3-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="79fd3-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="79fd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="79fd3-103">Modifica uma Revisão da API</span><span class="sxs-lookup"><span data-stu-id="79fd3-103">Modifies an API Revision</span></span>

## <span data-ttu-id="79fd3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79fd3-104">SYNTAX</span></span>

### <span data-ttu-id="79fd3-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79fd3-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79fd3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79fd3-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79fd3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="79fd3-107">DESCRIPTION</span></span>
<span data-ttu-id="79fd3-108">O cmdlet **Set-AzApiManagementApiRevision** modifica uma Revisão da API de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="79fd3-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="79fd3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79fd3-109">EXAMPLES</span></span>

### <span data-ttu-id="79fd3-110">Exemplo 1: modificar uma revisão da API</span><span class="sxs-lookup"><span data-stu-id="79fd3-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="79fd3-111">O cmdlet atualiza a `2` revisão da API com uma nova `echo-api` descrição, protocolo e caminho.</span><span class="sxs-lookup"><span data-stu-id="79fd3-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="79fd3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79fd3-112">PARAMETERS</span></span>

### <span data-ttu-id="79fd3-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79fd3-113">-ApiId</span></span>
<span data-ttu-id="79fd3-114">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="79fd3-114">Identifier of existing API.</span></span>
<span data-ttu-id="79fd3-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="79fd3-116">-ApiRevision</span></span>
<span data-ttu-id="79fd3-117">Identificador de Revisão de API existente.</span><span class="sxs-lookup"><span data-stu-id="79fd3-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="79fd3-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="79fd3-119">-AuthorizationScope</span></span>
<span data-ttu-id="79fd3-120">Escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="79fd3-120">OAuth operations scope.</span></span>
<span data-ttu-id="79fd3-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-121">This parameter is optional.</span></span>
<span data-ttu-id="79fd3-122">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-122">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="79fd3-123">-AuthorizationServerId</span></span>
<span data-ttu-id="79fd3-124">Identificador de servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="79fd3-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="79fd3-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-125">This parameter is optional.</span></span>
<span data-ttu-id="79fd3-126">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-126">Default value is $null.</span></span>
<span data-ttu-id="79fd3-127">Deve ser especificado se AuthorizationScope especificado.</span><span class="sxs-lookup"><span data-stu-id="79fd3-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="79fd3-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="79fd3-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="79fd3-129">Mecanismo do servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="79fd3-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="79fd3-130">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="79fd3-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="79fd3-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-131">This parameter is optional.</span></span> <span data-ttu-id="79fd3-132">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-132">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-133">-Contexto</span><span class="sxs-lookup"><span data-stu-id="79fd3-133">-Context</span></span>
<span data-ttu-id="79fd3-134">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="79fd3-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="79fd3-135">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-135">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fd3-136">-DefaultProfile</span></span>
<span data-ttu-id="79fd3-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79fd3-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79fd3-138">-Descrição</span><span class="sxs-lookup"><span data-stu-id="79fd3-138">-Description</span></span>
<span data-ttu-id="79fd3-139">Descrição da API da Web.</span><span class="sxs-lookup"><span data-stu-id="79fd3-139">Web API description.</span></span>
<span data-ttu-id="79fd3-140">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="79fd3-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79fd3-141">-InputObject</span></span>
<span data-ttu-id="79fd3-142">Instância de PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="79fd3-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="79fd3-143">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-143">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="79fd3-144">-Name</span></span>
<span data-ttu-id="79fd3-145">Nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="79fd3-145">Web API name.</span></span>
<span data-ttu-id="79fd3-146">Nome público da API, como seria exibido nos portais de desenvolvedor e administrador.</span><span class="sxs-lookup"><span data-stu-id="79fd3-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="79fd3-147">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-147">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="79fd3-148">-OpenIdProviderId</span></span>
<span data-ttu-id="79fd3-149">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="79fd3-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="79fd3-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-150">This parameter is optional.</span></span> <span data-ttu-id="79fd3-151">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-151">Default value is $null.</span></span> <span data-ttu-id="79fd3-152">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="79fd3-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="79fd3-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79fd3-153">-PassThru</span></span>
<span data-ttu-id="79fd3-154">Se especificado, instância do tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi que representa a API definida.</span><span class="sxs-lookup"><span data-stu-id="79fd3-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="79fd3-155">-Caminho</span><span class="sxs-lookup"><span data-stu-id="79fd3-155">-Path</span></span>
<span data-ttu-id="79fd3-156">Caminho da API da Web.</span><span class="sxs-lookup"><span data-stu-id="79fd3-156">Web API Path.</span></span>
<span data-ttu-id="79fd3-157">Última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="79fd3-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="79fd3-158">Essa URL será usada pelos consumidores da API para o envio de solicitações para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="79fd3-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="79fd3-159">Deve ter de 1 a 400 caracteres.</span><span class="sxs-lookup"><span data-stu-id="79fd3-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="79fd3-160">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-160">This parameter is optional.</span></span>
<span data-ttu-id="79fd3-161">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-161">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-162">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="79fd3-162">-Protocols</span></span>
<span data-ttu-id="79fd3-163">Protocolos de API da Web (https).</span><span class="sxs-lookup"><span data-stu-id="79fd3-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="79fd3-164">Protocolos sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="79fd3-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="79fd3-165">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-165">This parameter is required.</span></span>
<span data-ttu-id="79fd3-166">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-166">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="79fd3-167">-ServiceUrl</span></span>
<span data-ttu-id="79fd3-168">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="79fd3-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="79fd3-169">Essa URL será usada apenas pelo Gerenciamento de API do Azure e não será pública.</span><span class="sxs-lookup"><span data-stu-id="79fd3-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="79fd3-170">Deve ter de 1 a 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="79fd3-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="79fd3-171">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="79fd3-171">This parameter is required.</span></span>

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

### <span data-ttu-id="79fd3-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="79fd3-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="79fd3-173">Nome do header da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="79fd3-173">Subscription key header name.</span></span>
<span data-ttu-id="79fd3-174">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-174">This parameter is optional.</span></span>
<span data-ttu-id="79fd3-175">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-175">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="79fd3-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="79fd3-177">Nome do parâmetro da cadeia de caracteres de consulta de chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="79fd3-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="79fd3-178">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-178">This parameter is optional.</span></span>
<span data-ttu-id="79fd3-179">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="79fd3-179">Default value is $null.</span></span>

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

### <span data-ttu-id="79fd3-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="79fd3-180">-SubscriptionRequired</span></span>
<span data-ttu-id="79fd3-181">Sinalizar para impor SubscriptionRequired para solicitações à Api.</span><span class="sxs-lookup"><span data-stu-id="79fd3-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="79fd3-182">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd3-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="79fd3-183">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="79fd3-183">-Confirm</span></span>
<span data-ttu-id="79fd3-184">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79fd3-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79fd3-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fd3-185">-WhatIf</span></span>
<span data-ttu-id="79fd3-186">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="79fd3-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fd3-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79fd3-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79fd3-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fd3-188">CommonParameters</span></span>
<span data-ttu-id="79fd3-189">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fd3-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fd3-190">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79fd3-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fd3-191">Entradas</span><span class="sxs-lookup"><span data-stu-id="79fd3-191">INPUTS</span></span>

### <span data-ttu-id="79fd3-192">System.String</span><span class="sxs-lookup"><span data-stu-id="79fd3-192">System.String</span></span>

### <span data-ttu-id="79fd3-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79fd3-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79fd3-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79fd3-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="79fd3-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="79fd3-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="79fd3-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79fd3-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79fd3-197">Saídas</span><span class="sxs-lookup"><span data-stu-id="79fd3-197">OUTPUTS</span></span>

### <span data-ttu-id="79fd3-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79fd3-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="79fd3-199">Notas</span><span class="sxs-lookup"><span data-stu-id="79fd3-199">NOTES</span></span>

## <span data-ttu-id="79fd3-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79fd3-200">RELATED LINKS</span></span>

[<span data-ttu-id="79fd3-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="79fd3-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="79fd3-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="79fd3-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="79fd3-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="79fd3-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)