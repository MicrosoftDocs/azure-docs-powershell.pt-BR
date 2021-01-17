---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432677"
---
# <span data-ttu-id="e89c4-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="e89c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e89c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e89c4-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-103">Creates an API.</span></span>

## <span data-ttu-id="e89c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e89c4-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e89c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e89c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e89c4-106">O cmdlet **New-AzApiManagementApi** cria uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="e89c4-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="e89c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e89c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e89c4-108">Exemplo 1: criar uma API</span><span class="sxs-lookup"><span data-stu-id="e89c4-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="e89c4-109">Esse comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="e89c4-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="e89c4-110">Exemplo 2: criar uma API copiando todas as operações, marcas, produtos e políticas de eco-API e em um ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e89c4-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="e89c4-111">Esse comando cria uma API `echoapiv3` no ApiVersionSet `xmsVersionSet` e copia Todas as operações, marcas e políticas da API de origem `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="e89c4-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="e89c4-112">Ele substitui o SubscriptionRequired, o ServiceUrl, o caminho, os protocolos</span><span class="sxs-lookup"><span data-stu-id="e89c4-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="e89c4-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e89c4-113">Example 3</span></span>

<span data-ttu-id="e89c4-114">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-114">Creates an API.</span></span> <span data-ttu-id="e89c4-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e89c4-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="e89c4-116">OS</span><span class="sxs-lookup"><span data-stu-id="e89c4-116">PARAMETERS</span></span>

### <span data-ttu-id="e89c4-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e89c4-117">-ApiId</span></span>
<span data-ttu-id="e89c4-118">Especifica a ID da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e89c4-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="e89c4-119">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="e89c4-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="e89c4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e89c4-120">-ApiVersion</span></span>
<span data-ttu-id="e89c4-121">Versão de API da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e89c4-121">Api Version of the Api to create.</span></span> <span data-ttu-id="e89c4-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="e89c4-123">-ApiVersionDescription</span></span>
<span data-ttu-id="e89c4-124">Descrição da versão da API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-124">Api Version Description.</span></span> <span data-ttu-id="e89c4-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e89c4-126">-ApiVersionSetId</span></span>
<span data-ttu-id="e89c4-127">Um identificador de recurso para o conjunto de versões de API relacionado.</span><span class="sxs-lookup"><span data-stu-id="e89c4-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="e89c4-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="e89c4-129">-AuthorizationScope</span></span>
<span data-ttu-id="e89c4-130">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="e89c4-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="e89c4-131">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="e89c4-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="e89c4-132">-AuthorizationServerId</span></span>
<span data-ttu-id="e89c4-133">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="e89c4-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="e89c4-134">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-134">The default value is $Null.</span></span>
<span data-ttu-id="e89c4-135">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="e89c4-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="e89c4-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="e89c4-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="e89c4-137">Mecanismo de servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="e89c4-138">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="e89c4-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="e89c4-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-139">This parameter is optional.</span></span> <span data-ttu-id="e89c4-140">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-140">Default value is $null.</span></span>

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

### <span data-ttu-id="e89c4-141">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e89c4-141">-Context</span></span>
<span data-ttu-id="e89c4-142">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e89c4-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e89c4-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89c4-143">-DefaultProfile</span></span>
<span data-ttu-id="e89c4-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e89c4-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e89c4-145">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e89c4-145">-Description</span></span>
<span data-ttu-id="e89c4-146">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="e89c4-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="e89c4-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="e89c4-147">-Name</span></span>
<span data-ttu-id="e89c4-148">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="e89c4-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="e89c4-149">Esse é o nome público da API como aparece nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="e89c4-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="e89c4-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="e89c4-150">-OpenIdProviderId</span></span>
<span data-ttu-id="e89c4-151">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="e89c4-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="e89c4-152">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-152">This parameter is optional.</span></span> <span data-ttu-id="e89c4-153">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-153">Default value is $null.</span></span> <span data-ttu-id="e89c4-154">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="e89c4-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="e89c4-155">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e89c4-155">-Path</span></span>
<span data-ttu-id="e89c4-156">Especifica o caminho da API Web, que é a última parte da URL pública da API e corresponde ao campo de sufixo de URL da Web API no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="e89c4-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="e89c4-157">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e89c4-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="e89c4-158">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="e89c4-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="e89c4-159">-ProductIds</span></span>
<span data-ttu-id="e89c4-160">Especifica uma matriz de IDs de produto à qual será adicionada a nova API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="e89c4-161">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="e89c4-161">-Protocols</span></span>
<span data-ttu-id="e89c4-162">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="e89c4-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="e89c4-163">Os valores válidos são http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e89c4-163">Valid values are http, https.</span></span>
<span data-ttu-id="e89c4-164">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="e89c4-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="e89c4-165">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-165">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c4-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e89c4-166">-ServiceUrl</span></span>
<span data-ttu-id="e89c4-167">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="e89c4-168">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="e89c4-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="e89c4-169">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e89c4-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="e89c4-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="e89c4-170">-SourceApiId</span></span>
<span data-ttu-id="e89c4-171">Identificador de API da API de origem.</span><span class="sxs-lookup"><span data-stu-id="e89c4-171">Api identifier of the source API.</span></span> <span data-ttu-id="e89c4-172">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="e89c4-173">-SourceApiRevision</span></span>
<span data-ttu-id="e89c4-174">A versão da API de origem.</span><span class="sxs-lookup"><span data-stu-id="e89c4-174">Api Revision of the source API.</span></span> <span data-ttu-id="e89c4-175">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="e89c4-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="e89c4-177">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e89c4-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="e89c4-178">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="e89c4-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="e89c4-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="e89c4-180">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e89c4-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="e89c4-181">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e89c4-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="e89c4-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="e89c4-182">-SubscriptionRequired</span></span>
<span data-ttu-id="e89c4-183">Sinalizador para impor SubscriptionRequired para as solicitações à API.</span><span class="sxs-lookup"><span data-stu-id="e89c4-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="e89c4-184">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e89c4-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="e89c4-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89c4-185">CommonParameters</span></span>
<span data-ttu-id="e89c4-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e89c4-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89c4-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e89c4-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89c4-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e89c4-188">INPUTS</span></span>

### <span data-ttu-id="e89c4-189">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e89c4-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e89c4-190">System. String</span><span class="sxs-lookup"><span data-stu-id="e89c4-190">System.String</span></span>

### <span data-ttu-id="e89c4-191">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="e89c4-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="e89c4-192">System. String []</span><span class="sxs-lookup"><span data-stu-id="e89c4-192">System.String[]</span></span>

## <span data-ttu-id="e89c4-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e89c4-193">OUTPUTS</span></span>

### <span data-ttu-id="e89c4-194">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e89c4-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e89c4-195">NOTES</span></span>

## <span data-ttu-id="e89c4-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e89c4-196">RELATED LINKS</span></span>

[<span data-ttu-id="e89c4-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="e89c4-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e89c4-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e89c4-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e89c4-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e89c4-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


