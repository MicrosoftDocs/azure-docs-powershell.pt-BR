---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93945000"
---
# <span data-ttu-id="edfe1-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="edfe1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="edfe1-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-103">Creates an API.</span></span>

## <span data-ttu-id="edfe1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edfe1-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edfe1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edfe1-105">DESCRIPTION</span></span>
<span data-ttu-id="edfe1-106">O cmdlet **New-AzApiManagementApi** cria uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="edfe1-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="edfe1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edfe1-107">EXAMPLES</span></span>

### <span data-ttu-id="edfe1-108">Exemplo 1: criar uma API</span><span class="sxs-lookup"><span data-stu-id="edfe1-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="edfe1-109">Esse comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="edfe1-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="edfe1-110">Exemplo 1: criar uma API copiando todas as operações, marcas, produtos e políticas de eco-API e em um ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="edfe1-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="edfe1-111">Esse comando cria uma API `echoapiv3` no ApiVersionSet `xmsVersionSet` e copia Todas as operações, marcas e políticas da API de origem `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="edfe1-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="edfe1-112">Ele substitui o SubscriptionRequired, o ServiceUrl, o caminho, os protocolos</span><span class="sxs-lookup"><span data-stu-id="edfe1-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="edfe1-113">OS</span><span class="sxs-lookup"><span data-stu-id="edfe1-113">PARAMETERS</span></span>

### <span data-ttu-id="edfe1-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="edfe1-114">-ApiId</span></span>
<span data-ttu-id="edfe1-115">Especifica a ID da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="edfe1-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="edfe1-116">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="edfe1-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="edfe1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="edfe1-117">-ApiVersion</span></span>
<span data-ttu-id="edfe1-118">Versão de API da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="edfe1-118">Api Version of the Api to create.</span></span> <span data-ttu-id="edfe1-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="edfe1-120">-ApiVersionDescription</span></span>
<span data-ttu-id="edfe1-121">Descrição da versão da API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-121">Api Version Description.</span></span> <span data-ttu-id="edfe1-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="edfe1-123">-ApiVersionSetId</span></span>
<span data-ttu-id="edfe1-124">Um identificador de recurso para o conjunto de versões de API relacionado.</span><span class="sxs-lookup"><span data-stu-id="edfe1-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="edfe1-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="edfe1-126">-AuthorizationScope</span></span>
<span data-ttu-id="edfe1-127">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="edfe1-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="edfe1-128">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="edfe1-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="edfe1-129">-AuthorizationServerId</span></span>
<span data-ttu-id="edfe1-130">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="edfe1-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="edfe1-131">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-131">The default value is $Null.</span></span>
<span data-ttu-id="edfe1-132">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="edfe1-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="edfe1-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="edfe1-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="edfe1-134">Mecanismo de servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="edfe1-135">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="edfe1-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="edfe1-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-136">This parameter is optional.</span></span> <span data-ttu-id="edfe1-137">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-137">Default value is $null.</span></span>

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

### <span data-ttu-id="edfe1-138">-Contexto</span><span class="sxs-lookup"><span data-stu-id="edfe1-138">-Context</span></span>
<span data-ttu-id="edfe1-139">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="edfe1-139">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="edfe1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfe1-140">-DefaultProfile</span></span>
<span data-ttu-id="edfe1-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edfe1-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edfe1-142">-Descrição</span><span class="sxs-lookup"><span data-stu-id="edfe1-142">-Description</span></span>
<span data-ttu-id="edfe1-143">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="edfe1-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="edfe1-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="edfe1-144">-Name</span></span>
<span data-ttu-id="edfe1-145">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="edfe1-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="edfe1-146">Esse é o nome público da API como aparece nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="edfe1-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="edfe1-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="edfe1-147">-OpenIdProviderId</span></span>
<span data-ttu-id="edfe1-148">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="edfe1-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="edfe1-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-149">This parameter is optional.</span></span> <span data-ttu-id="edfe1-150">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-150">Default value is $null.</span></span> <span data-ttu-id="edfe1-151">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="edfe1-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="edfe1-152">-Caminho</span><span class="sxs-lookup"><span data-stu-id="edfe1-152">-Path</span></span>
<span data-ttu-id="edfe1-153">Especifica o caminho da API Web, que é a última parte da URL pública da API e corresponde ao campo de sufixo de URL da Web API no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="edfe1-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="edfe1-154">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="edfe1-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="edfe1-155">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="edfe1-156">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="edfe1-156">-ProductIds</span></span>
<span data-ttu-id="edfe1-157">Especifica uma matriz de IDs de produto à qual será adicionada a nova API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="edfe1-158">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="edfe1-158">-Protocols</span></span>
<span data-ttu-id="edfe1-159">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="edfe1-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="edfe1-160">Os valores válidos são http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="edfe1-160">Valid values are http, https.</span></span>
<span data-ttu-id="edfe1-161">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="edfe1-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="edfe1-162">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-162">The default value is $Null.</span></span>

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

### <span data-ttu-id="edfe1-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="edfe1-163">-ServiceUrl</span></span>
<span data-ttu-id="edfe1-164">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="edfe1-165">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="edfe1-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="edfe1-166">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="edfe1-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="edfe1-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="edfe1-167">-SourceApiId</span></span>
<span data-ttu-id="edfe1-168">Identificador de API da API de origem.</span><span class="sxs-lookup"><span data-stu-id="edfe1-168">Api identifier of the source API.</span></span> <span data-ttu-id="edfe1-169">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="edfe1-170">-SourceApiRevision</span></span>
<span data-ttu-id="edfe1-171">A versão da API de origem.</span><span class="sxs-lookup"><span data-stu-id="edfe1-171">Api Revision of the source API.</span></span> <span data-ttu-id="edfe1-172">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="edfe1-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="edfe1-174">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="edfe1-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="edfe1-175">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="edfe1-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="edfe1-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="edfe1-177">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="edfe1-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="edfe1-178">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="edfe1-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="edfe1-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="edfe1-179">-SubscriptionRequired</span></span>
<span data-ttu-id="edfe1-180">Sinalizador para impor SubscriptionRequired para as solicitações à API.</span><span class="sxs-lookup"><span data-stu-id="edfe1-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="edfe1-181">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="edfe1-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="edfe1-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfe1-182">CommonParameters</span></span>
<span data-ttu-id="edfe1-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfe1-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfe1-184">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edfe1-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfe1-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edfe1-185">INPUTS</span></span>

### <span data-ttu-id="edfe1-186">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="edfe1-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="edfe1-187">System. String</span><span class="sxs-lookup"><span data-stu-id="edfe1-187">System.String</span></span>

### <span data-ttu-id="edfe1-188">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="edfe1-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="edfe1-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="edfe1-189">System.String[]</span></span>

## <span data-ttu-id="edfe1-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edfe1-190">OUTPUTS</span></span>

### <span data-ttu-id="edfe1-191">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="edfe1-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edfe1-192">NOTES</span></span>

## <span data-ttu-id="edfe1-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edfe1-193">RELATED LINKS</span></span>

[<span data-ttu-id="edfe1-194">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="edfe1-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="edfe1-196">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="edfe1-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="edfe1-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edfe1-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


