---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771353"
---
# <span data-ttu-id="33729-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="33729-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33729-102">SYNOPSIS</span></span>
<span data-ttu-id="33729-103">Modifica uma API.</span><span class="sxs-lookup"><span data-stu-id="33729-103">Modifies an API.</span></span>

## <span data-ttu-id="33729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33729-104">SYNTAX</span></span>

### <span data-ttu-id="33729-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="33729-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33729-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33729-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33729-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33729-107">DESCRIPTION</span></span>
<span data-ttu-id="33729-108">O cmdlet **set-AzApiManagementApi** modifica uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="33729-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="33729-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33729-109">EXAMPLES</span></span>

### <span data-ttu-id="33729-110">Exemplo 1 modificar uma API</span><span class="sxs-lookup"><span data-stu-id="33729-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="33729-111">OS</span><span class="sxs-lookup"><span data-stu-id="33729-111">PARAMETERS</span></span>

### <span data-ttu-id="33729-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33729-112">-ApiId</span></span>
<span data-ttu-id="33729-113">Especifica a ID da API a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="33729-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="33729-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="33729-114">-AuthorizationScope</span></span>
<span data-ttu-id="33729-115">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="33729-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="33729-116">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="33729-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="33729-117">-AuthorizationServerId</span></span>
<span data-ttu-id="33729-118">Especifica o identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="33729-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="33729-119">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-119">The default value is $Null.</span></span>
<span data-ttu-id="33729-120">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="33729-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="33729-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="33729-121">-Context</span></span>
<span data-ttu-id="33729-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="33729-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33729-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33729-123">-DefaultProfile</span></span>
<span data-ttu-id="33729-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33729-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33729-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="33729-125">-Description</span></span>
<span data-ttu-id="33729-126">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="33729-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="33729-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33729-127">-InputObject</span></span>
<span data-ttu-id="33729-128">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="33729-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="33729-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="33729-129">This parameter is required.</span></span>

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

### <span data-ttu-id="33729-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="33729-130">-Name</span></span>
<span data-ttu-id="33729-131">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="33729-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="33729-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33729-132">-PassThru</span></span>
<span data-ttu-id="33729-133">PassThru</span><span class="sxs-lookup"><span data-stu-id="33729-133">passthru</span></span>

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

### <span data-ttu-id="33729-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="33729-134">-Path</span></span>
<span data-ttu-id="33729-135">Especifica o caminho da API Web, que é a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="33729-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="33729-136">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="33729-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="33729-137">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="33729-138">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="33729-138">-Protocols</span></span>
<span data-ttu-id="33729-139">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="33729-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="33729-140">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="33729-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="33729-141">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="33729-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="33729-142">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="33729-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="33729-143">-ServiceUrl</span></span>
<span data-ttu-id="33729-144">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="33729-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="33729-145">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="33729-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="33729-146">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="33729-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="33729-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="33729-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="33729-148">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="33729-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="33729-149">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="33729-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="33729-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="33729-151">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="33729-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="33729-152">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="33729-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="33729-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33729-153">CommonParameters</span></span>
<span data-ttu-id="33729-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33729-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33729-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33729-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33729-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33729-156">INPUTS</span></span>

### <span data-ttu-id="33729-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33729-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33729-158">System. String</span><span class="sxs-lookup"><span data-stu-id="33729-158">System.String</span></span>

### <span data-ttu-id="33729-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="33729-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="33729-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="33729-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33729-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33729-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33729-162">OUTPUTS</span></span>

### <span data-ttu-id="33729-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="33729-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33729-164">NOTES</span></span>

## <span data-ttu-id="33729-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33729-165">RELATED LINKS</span></span>

[<span data-ttu-id="33729-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="33729-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="33729-168">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="33729-169">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="33729-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="33729-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


