---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 61c02917d5381753ec8fd9e4b7560f68722d5f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886702"
---
# <span data-ttu-id="9d947-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="9d947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d947-102">SYNOPSIS</span></span>
<span data-ttu-id="9d947-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="9d947-103">Creates an API.</span></span>

## <span data-ttu-id="9d947-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9d947-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d947-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9d947-105">DESCRIPTION</span></span>
<span data-ttu-id="9d947-106">O cmdlet **New-AzApiManagementApi** cria uma API de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d947-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="9d947-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d947-107">EXAMPLES</span></span>

### <span data-ttu-id="9d947-108">Exemplo 1: Criar uma API</span><span class="sxs-lookup"><span data-stu-id="9d947-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="9d947-109">Este comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="9d947-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="9d947-110">Exemplo 2: Criar uma API copiando todas as operações, marcas, produtos e políticas de eco api e em um ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9d947-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="9d947-111">Este comando cria uma API em ApiVersionSet e copia todas `echoapiv3` `xmsVersionSet` as operações, marcas e políticas da Api de `echo-api` origem.</span><span class="sxs-lookup"><span data-stu-id="9d947-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="9d947-112">Ele substitui SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="9d947-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="9d947-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9d947-113">Example 3</span></span>

<span data-ttu-id="9d947-114">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="9d947-114">Creates an API.</span></span> <span data-ttu-id="9d947-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="9d947-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="9d947-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9d947-116">PARAMETERS</span></span>

### <span data-ttu-id="9d947-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9d947-117">-ApiId</span></span>
<span data-ttu-id="9d947-118">Especifica a ID da API a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9d947-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="9d947-119">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="9d947-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="9d947-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d947-120">-ApiVersion</span></span>
<span data-ttu-id="9d947-121">Api Version da Api a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9d947-121">Api Version of the Api to create.</span></span> <span data-ttu-id="9d947-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="9d947-123">-ApiVersionDescription</span></span>
<span data-ttu-id="9d947-124">Api Version Description.</span><span class="sxs-lookup"><span data-stu-id="9d947-124">Api Version Description.</span></span> <span data-ttu-id="9d947-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9d947-126">-ApiVersionSetId</span></span>
<span data-ttu-id="9d947-127">Um identificador de recurso para o Conjunto de Versão da Api relacionado.</span><span class="sxs-lookup"><span data-stu-id="9d947-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="9d947-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9d947-129">-AuthorizationScope</span></span>
<span data-ttu-id="9d947-130">Especifica o escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="9d947-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9d947-131">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="9d947-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9d947-132">-AuthorizationServerId</span></span>
<span data-ttu-id="9d947-133">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="9d947-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="9d947-134">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-134">The default value is $Null.</span></span>
<span data-ttu-id="9d947-135">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="9d947-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="9d947-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="9d947-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="9d947-137">Mecanismo do servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="9d947-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="9d947-138">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="9d947-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="9d947-139">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-139">This parameter is optional.</span></span> <span data-ttu-id="9d947-140">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="9d947-140">Default value is $null.</span></span>

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

### <span data-ttu-id="9d947-141">-Context</span><span class="sxs-lookup"><span data-stu-id="9d947-141">-Context</span></span>
<span data-ttu-id="9d947-142">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9d947-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9d947-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d947-143">-DefaultProfile</span></span>
<span data-ttu-id="9d947-144">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9d947-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d947-145">-Description</span><span class="sxs-lookup"><span data-stu-id="9d947-145">-Description</span></span>
<span data-ttu-id="9d947-146">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="9d947-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="9d947-147">-Name</span><span class="sxs-lookup"><span data-stu-id="9d947-147">-Name</span></span>
<span data-ttu-id="9d947-148">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="9d947-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="9d947-149">Esse é o nome público da API, conforme aparece nos portais de desenvolvedor e administrador.</span><span class="sxs-lookup"><span data-stu-id="9d947-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="9d947-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="9d947-150">-OpenIdProviderId</span></span>
<span data-ttu-id="9d947-151">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="9d947-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="9d947-152">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-152">This parameter is optional.</span></span> <span data-ttu-id="9d947-153">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="9d947-153">Default value is $null.</span></span> <span data-ttu-id="9d947-154">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="9d947-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="9d947-155">-Path</span><span class="sxs-lookup"><span data-stu-id="9d947-155">-Path</span></span>
<span data-ttu-id="9d947-156">Especifica o caminho da API da Web, que é a última parte da URL pública da API e corresponde ao campo sufixo URL da API Web no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="9d947-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="9d947-157">Essa URL é usada pelos consumidores de API para enviar solicitações para o serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="9d947-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9d947-158">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="9d947-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="9d947-159">-ProductIds</span></span>
<span data-ttu-id="9d947-160">Especifica uma matriz de IDs de produto às quais adicionar a nova API.</span><span class="sxs-lookup"><span data-stu-id="9d947-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="9d947-161">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="9d947-161">-Protocols</span></span>
<span data-ttu-id="9d947-162">Especifica uma matriz de protocolos de API da Web.</span><span class="sxs-lookup"><span data-stu-id="9d947-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9d947-163">Os valores válidos são https.</span><span class="sxs-lookup"><span data-stu-id="9d947-163">Valid values are http, https.</span></span>
<span data-ttu-id="9d947-164">Esses são os protocolos web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="9d947-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9d947-165">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="9d947-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9d947-166">-ServiceUrl</span></span>
<span data-ttu-id="9d947-167">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="9d947-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9d947-168">Essa URL é usada apenas pelo Gerenciamento de API do Azure e não é pública.</span><span class="sxs-lookup"><span data-stu-id="9d947-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9d947-169">A URL deve ter de um a 2.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d947-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="9d947-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="9d947-170">-SourceApiId</span></span>
<span data-ttu-id="9d947-171">Identificador de api da API de origem.</span><span class="sxs-lookup"><span data-stu-id="9d947-171">Api identifier of the source API.</span></span> <span data-ttu-id="9d947-172">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="9d947-173">-SourceApiRevision</span></span>
<span data-ttu-id="9d947-174">Revisão da API da API de origem.</span><span class="sxs-lookup"><span data-stu-id="9d947-174">Api Revision of the source API.</span></span> <span data-ttu-id="9d947-175">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9d947-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9d947-177">Especifica o nome do header da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9d947-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="9d947-178">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="9d947-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9d947-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9d947-180">Especifica o nome do parâmetro de cadeia de caracteres de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9d947-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="9d947-181">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="9d947-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="9d947-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9d947-182">-SubscriptionRequired</span></span>
<span data-ttu-id="9d947-183">Sinalizador para impor SubscriptionRequired para solicitações à Api.</span><span class="sxs-lookup"><span data-stu-id="9d947-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="9d947-184">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9d947-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d947-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d947-185">CommonParameters</span></span>
<span data-ttu-id="9d947-186">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d947-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d947-187">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d947-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d947-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d947-188">INPUTS</span></span>

### <span data-ttu-id="9d947-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d947-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d947-190">System.String</span><span class="sxs-lookup"><span data-stu-id="9d947-190">System.String</span></span>

### <span data-ttu-id="9d947-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="9d947-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9d947-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9d947-192">System.String[]</span></span>

## <span data-ttu-id="9d947-193">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9d947-193">OUTPUTS</span></span>

### <span data-ttu-id="9d947-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9d947-195">NOTES</span><span class="sxs-lookup"><span data-stu-id="9d947-195">NOTES</span></span>

## <span data-ttu-id="9d947-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d947-196">RELATED LINKS</span></span>

[<span data-ttu-id="9d947-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9d947-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9d947-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9d947-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="9d947-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9d947-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


