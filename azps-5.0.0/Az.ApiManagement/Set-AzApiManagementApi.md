---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281502"
---
# <span data-ttu-id="4e015-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="4e015-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e015-102">SYNOPSIS</span></span>
<span data-ttu-id="4e015-103">Modifica uma API.</span><span class="sxs-lookup"><span data-stu-id="4e015-103">Modifies an API.</span></span>

## <span data-ttu-id="4e015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e015-104">SYNTAX</span></span>

### <span data-ttu-id="4e015-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4e015-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e015-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e015-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e015-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e015-107">DESCRIPTION</span></span>
<span data-ttu-id="4e015-108">O cmdlet **set-AzApiManagementApi** modifica uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e015-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="4e015-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e015-109">EXAMPLES</span></span>

### <span data-ttu-id="4e015-110">Exemplo 1: modificar uma API</span><span class="sxs-lookup"><span data-stu-id="4e015-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="4e015-111">Exemplo 2: adicionar uma API a um ApiVersionSet existente</span><span class="sxs-lookup"><span data-stu-id="4e015-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="4e015-112">Este exemplo adiciona uma API a um conjunto de versões de API existente</span><span class="sxs-lookup"><span data-stu-id="4e015-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="4e015-113">Exemplo 3: alterar o ServiceUrl de back-end no qual a API está apontando</span><span class="sxs-lookup"><span data-stu-id="4e015-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="4e015-114">Este exemplo atualiza o ServiceUrl ao `echo-api` qual está apontando.</span><span class="sxs-lookup"><span data-stu-id="4e015-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="4e015-115">OS</span><span class="sxs-lookup"><span data-stu-id="4e015-115">PARAMETERS</span></span>

### <span data-ttu-id="4e015-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4e015-116">-ApiId</span></span>
<span data-ttu-id="4e015-117">Especifica a ID da API a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="4e015-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="4e015-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="4e015-118">-AuthorizationScope</span></span>
<span data-ttu-id="4e015-119">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="4e015-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="4e015-120">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="4e015-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="4e015-121">-AuthorizationServerId</span></span>
<span data-ttu-id="4e015-122">Especifica o identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="4e015-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="4e015-123">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-123">The default value is $Null.</span></span>
<span data-ttu-id="4e015-124">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="4e015-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="4e015-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="4e015-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="4e015-126">Mecanismo de servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="4e015-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="4e015-127">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="4e015-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="4e015-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e015-128">This parameter is optional.</span></span> <span data-ttu-id="4e015-129">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4e015-129">Default value is $null.</span></span>

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

### <span data-ttu-id="4e015-130">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4e015-130">-Context</span></span>
<span data-ttu-id="4e015-131">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4e015-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4e015-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e015-132">-DefaultProfile</span></span>
<span data-ttu-id="4e015-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e015-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e015-134">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4e015-134">-Description</span></span>
<span data-ttu-id="4e015-135">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="4e015-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="4e015-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e015-136">-InputObject</span></span>
<span data-ttu-id="4e015-137">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4e015-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="4e015-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4e015-138">This parameter is required.</span></span>

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

### <span data-ttu-id="4e015-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e015-139">-Name</span></span>
<span data-ttu-id="4e015-140">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="4e015-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="4e015-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="4e015-141">-OpenIdProviderId</span></span>
<span data-ttu-id="4e015-142">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="4e015-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="4e015-143">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e015-143">This parameter is optional.</span></span> <span data-ttu-id="4e015-144">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4e015-144">Default value is $null.</span></span> <span data-ttu-id="4e015-145">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="4e015-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="4e015-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e015-146">-PassThru</span></span>
<span data-ttu-id="4e015-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="4e015-147">passthru</span></span>

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

### <span data-ttu-id="4e015-148">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4e015-148">-Path</span></span>
<span data-ttu-id="4e015-149">Especifica o caminho da API Web, que é a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="4e015-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="4e015-150">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="4e015-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="4e015-151">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="4e015-152">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="4e015-152">-Protocols</span></span>
<span data-ttu-id="4e015-153">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="4e015-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="4e015-154">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4e015-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="4e015-155">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="4e015-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="4e015-156">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="4e015-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4e015-157">-ServiceUrl</span></span>
<span data-ttu-id="4e015-158">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="4e015-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="4e015-159">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="4e015-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="4e015-160">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="4e015-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="4e015-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="4e015-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="4e015-162">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e015-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="4e015-163">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="4e015-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="4e015-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="4e015-165">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e015-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="4e015-166">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="4e015-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="4e015-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4e015-167">-SubscriptionRequired</span></span>
<span data-ttu-id="4e015-168">Sinalizador para impor SubscriptionRequired para as solicitações à API.</span><span class="sxs-lookup"><span data-stu-id="4e015-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="4e015-169">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e015-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="4e015-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e015-170">CommonParameters</span></span>
<span data-ttu-id="4e015-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e015-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e015-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e015-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e015-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e015-173">INPUTS</span></span>

### <span data-ttu-id="4e015-174">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4e015-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4e015-175">System. String</span><span class="sxs-lookup"><span data-stu-id="4e015-175">System.String</span></span>

### <span data-ttu-id="4e015-176">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="4e015-177">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="4e015-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="4e015-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4e015-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e015-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e015-179">OUTPUTS</span></span>

### <span data-ttu-id="4e015-180">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4e015-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e015-181">NOTES</span></span>

## <span data-ttu-id="4e015-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e015-182">RELATED LINKS</span></span>

[<span data-ttu-id="4e015-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="4e015-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4e015-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="4e015-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="4e015-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4e015-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


