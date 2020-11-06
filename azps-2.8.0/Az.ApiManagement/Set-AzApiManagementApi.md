---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597953"
---
# <span data-ttu-id="dc314-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="dc314-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc314-102">SYNOPSIS</span></span>
<span data-ttu-id="dc314-103">Modifica uma API.</span><span class="sxs-lookup"><span data-stu-id="dc314-103">Modifies an API.</span></span>

## <span data-ttu-id="dc314-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc314-104">SYNTAX</span></span>

### <span data-ttu-id="dc314-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc314-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc314-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc314-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc314-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc314-107">DESCRIPTION</span></span>
<span data-ttu-id="dc314-108">O cmdlet **set-AzApiManagementApi** modifica uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc314-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="dc314-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc314-109">EXAMPLES</span></span>

### <span data-ttu-id="dc314-110">Exemplo 1 modificar uma API</span><span class="sxs-lookup"><span data-stu-id="dc314-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="dc314-111">Exemplo 2 adicionar uma API a um ApiVersionSet existente</span><span class="sxs-lookup"><span data-stu-id="dc314-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="dc314-112">Este exemplo adiciona uma API a um conjunto de versões de API existente</span><span class="sxs-lookup"><span data-stu-id="dc314-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="dc314-113">OS</span><span class="sxs-lookup"><span data-stu-id="dc314-113">PARAMETERS</span></span>

### <span data-ttu-id="dc314-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dc314-114">-ApiId</span></span>
<span data-ttu-id="dc314-115">Especifica a ID da API a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="dc314-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="dc314-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="dc314-116">-AuthorizationScope</span></span>
<span data-ttu-id="dc314-117">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="dc314-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="dc314-118">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc314-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="dc314-119">-AuthorizationServerId</span></span>
<span data-ttu-id="dc314-120">Especifica o identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="dc314-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="dc314-121">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-121">The default value is $Null.</span></span>
<span data-ttu-id="dc314-122">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="dc314-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="dc314-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="dc314-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="dc314-124">Mecanismo de servidor de autorização OpenId pelo qual o token de acesso é passado para a API.</span><span class="sxs-lookup"><span data-stu-id="dc314-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="dc314-125">Consulte http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="dc314-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="dc314-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc314-126">This parameter is optional.</span></span> <span data-ttu-id="dc314-127">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="dc314-127">Default value is $null.</span></span>

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

### <span data-ttu-id="dc314-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="dc314-128">-Context</span></span>
<span data-ttu-id="dc314-129">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dc314-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dc314-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc314-130">-DefaultProfile</span></span>
<span data-ttu-id="dc314-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc314-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc314-132">-Descrição</span><span class="sxs-lookup"><span data-stu-id="dc314-132">-Description</span></span>
<span data-ttu-id="dc314-133">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="dc314-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="dc314-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc314-134">-InputObject</span></span>
<span data-ttu-id="dc314-135">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="dc314-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="dc314-136">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="dc314-136">This parameter is required.</span></span>

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

### <span data-ttu-id="dc314-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc314-137">-Name</span></span>
<span data-ttu-id="dc314-138">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="dc314-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="dc314-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="dc314-139">-OpenIdProviderId</span></span>
<span data-ttu-id="dc314-140">Identificador do servidor de autorização OpenId.</span><span class="sxs-lookup"><span data-stu-id="dc314-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="dc314-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc314-141">This parameter is optional.</span></span> <span data-ttu-id="dc314-142">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="dc314-142">Default value is $null.</span></span> <span data-ttu-id="dc314-143">Deve ser especificado se BearerTokenSendingMethods for especificado.</span><span class="sxs-lookup"><span data-stu-id="dc314-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="dc314-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc314-144">-PassThru</span></span>
<span data-ttu-id="dc314-145">PassThru</span><span class="sxs-lookup"><span data-stu-id="dc314-145">passthru</span></span>

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

### <span data-ttu-id="dc314-146">-Caminho</span><span class="sxs-lookup"><span data-stu-id="dc314-146">-Path</span></span>
<span data-ttu-id="dc314-147">Especifica o caminho da API Web, que é a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="dc314-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="dc314-148">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="dc314-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="dc314-149">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc314-150">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="dc314-150">-Protocols</span></span>
<span data-ttu-id="dc314-151">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="dc314-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="dc314-152">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dc314-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="dc314-153">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="dc314-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="dc314-154">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc314-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="dc314-155">-ServiceUrl</span></span>
<span data-ttu-id="dc314-156">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="dc314-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="dc314-157">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="dc314-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="dc314-158">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="dc314-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="dc314-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="dc314-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="dc314-160">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="dc314-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="dc314-161">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc314-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="dc314-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="dc314-163">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="dc314-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="dc314-164">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="dc314-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="dc314-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="dc314-165">-SubscriptionRequired</span></span>
<span data-ttu-id="dc314-166">Sinalizador para impor SubscriptionRequired para as solicitações à API.</span><span class="sxs-lookup"><span data-stu-id="dc314-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="dc314-167">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="dc314-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="dc314-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc314-168">CommonParameters</span></span>
<span data-ttu-id="dc314-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc314-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc314-170">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc314-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc314-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc314-171">INPUTS</span></span>

### <span data-ttu-id="dc314-172">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc314-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc314-173">System. String</span><span class="sxs-lookup"><span data-stu-id="dc314-173">System.String</span></span>

### <span data-ttu-id="dc314-174">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="dc314-175">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="dc314-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="dc314-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc314-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc314-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc314-177">OUTPUTS</span></span>

### <span data-ttu-id="dc314-178">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="dc314-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc314-179">NOTES</span></span>

## <span data-ttu-id="dc314-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc314-180">RELATED LINKS</span></span>

[<span data-ttu-id="dc314-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="dc314-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="dc314-183">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dc314-184">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="dc314-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc314-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


