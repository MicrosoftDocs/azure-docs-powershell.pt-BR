---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432815"
---
# <span data-ttu-id="108c6-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="108c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="108c6-102">SYNOPSIS</span></span>
<span data-ttu-id="108c6-103">Modifica uma API.</span><span class="sxs-lookup"><span data-stu-id="108c6-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="108c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="108c6-104">SYNTAX</span></span>

### <span data-ttu-id="108c6-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="108c6-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="108c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="108c6-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108c6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="108c6-107">DESCRIPTION</span></span>
<span data-ttu-id="108c6-108">O cmdlet **set-AzureRmApiManagementApi** modifica uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="108c6-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="108c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="108c6-109">EXAMPLES</span></span>

### <span data-ttu-id="108c6-110">Exemplo 1 modificar uma API</span><span class="sxs-lookup"><span data-stu-id="108c6-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="108c6-111">OS</span><span class="sxs-lookup"><span data-stu-id="108c6-111">PARAMETERS</span></span>

### <span data-ttu-id="108c6-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="108c6-112">-ApiId</span></span>
<span data-ttu-id="108c6-113">Especifica a ID da API a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="108c6-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="108c6-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="108c6-114">-AuthorizationScope</span></span>
<span data-ttu-id="108c6-115">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="108c6-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="108c6-116">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="108c6-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="108c6-117">-AuthorizationServerId</span></span>
<span data-ttu-id="108c6-118">Especifica o identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="108c6-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="108c6-119">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-119">The default value is $Null.</span></span>
<span data-ttu-id="108c6-120">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="108c6-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="108c6-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="108c6-121">-Context</span></span>
<span data-ttu-id="108c6-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="108c6-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="108c6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108c6-123">-DefaultProfile</span></span>
<span data-ttu-id="108c6-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="108c6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="108c6-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="108c6-125">-Description</span></span>
<span data-ttu-id="108c6-126">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="108c6-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="108c6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="108c6-127">-InputObject</span></span>
<span data-ttu-id="108c6-128">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="108c6-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="108c6-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="108c6-129">This parameter is required.</span></span>

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

### <span data-ttu-id="108c6-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="108c6-130">-Name</span></span>
<span data-ttu-id="108c6-131">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="108c6-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="108c6-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="108c6-132">-PassThru</span></span>
<span data-ttu-id="108c6-133">PassThru</span><span class="sxs-lookup"><span data-stu-id="108c6-133">passthru</span></span>

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

### <span data-ttu-id="108c6-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="108c6-134">-Path</span></span>
<span data-ttu-id="108c6-135">Especifica o caminho da API Web, que é a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="108c6-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="108c6-136">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="108c6-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="108c6-137">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="108c6-138">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="108c6-138">-Protocols</span></span>
<span data-ttu-id="108c6-139">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="108c6-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="108c6-140">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="108c6-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="108c6-141">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="108c6-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="108c6-142">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="108c6-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="108c6-143">-ServiceUrl</span></span>
<span data-ttu-id="108c6-144">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="108c6-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="108c6-145">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="108c6-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="108c6-146">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="108c6-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="108c6-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="108c6-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="108c6-148">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="108c6-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="108c6-149">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="108c6-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="108c6-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="108c6-151">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="108c6-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="108c6-152">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="108c6-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="108c6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108c6-153">CommonParameters</span></span>
<span data-ttu-id="108c6-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108c6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108c6-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="108c6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108c6-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="108c6-156">INPUTS</span></span>

### <span data-ttu-id="108c6-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="108c6-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="108c6-158">System. String</span><span class="sxs-lookup"><span data-stu-id="108c6-158">System.String</span></span>

### <span data-ttu-id="108c6-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="108c6-160">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="108c6-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="108c6-161">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="108c6-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="108c6-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="108c6-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="108c6-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="108c6-163">OUTPUTS</span></span>

### <span data-ttu-id="108c6-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="108c6-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="108c6-165">NOTES</span></span>

## <span data-ttu-id="108c6-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="108c6-166">RELATED LINKS</span></span>

[<span data-ttu-id="108c6-167">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="108c6-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="108c6-169">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="108c6-170">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="108c6-171">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="108c6-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


