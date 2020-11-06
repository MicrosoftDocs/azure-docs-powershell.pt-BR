---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431750"
---
# <span data-ttu-id="749a2-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="749a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="749a2-102">SYNOPSIS</span></span>
<span data-ttu-id="749a2-103">Modifica uma API.</span><span class="sxs-lookup"><span data-stu-id="749a2-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="749a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="749a2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="749a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="749a2-105">DESCRIPTION</span></span>
<span data-ttu-id="749a2-106">O cmdlet **set-AzureRmApiManagementApi** modifica uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="749a2-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="749a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="749a2-107">EXAMPLES</span></span>

### <span data-ttu-id="749a2-108">Exemplo 1 modificar uma API</span><span class="sxs-lookup"><span data-stu-id="749a2-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="749a2-109">OS</span><span class="sxs-lookup"><span data-stu-id="749a2-109">PARAMETERS</span></span>

### <span data-ttu-id="749a2-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="749a2-110">-ApiId</span></span>
<span data-ttu-id="749a2-111">Especifica a ID da API a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="749a2-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="749a2-112">-AuthorizationScope</span></span>
<span data-ttu-id="749a2-113">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="749a2-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="749a2-114">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="749a2-115">-AuthorizationServerId</span></span>
<span data-ttu-id="749a2-116">Especifica o identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="749a2-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="749a2-117">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-117">The default value is $Null.</span></span>
<span data-ttu-id="749a2-118">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="749a2-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="749a2-119">-Context</span></span>
<span data-ttu-id="749a2-120">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="749a2-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749a2-121">-DefaultProfile</span></span>
<span data-ttu-id="749a2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="749a2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="749a2-123">-Description</span></span>
<span data-ttu-id="749a2-124">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="749a2-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="749a2-125">-Name</span></span>
<span data-ttu-id="749a2-126">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="749a2-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="749a2-127">-PassThru</span></span>
<span data-ttu-id="749a2-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="749a2-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="749a2-129">-Path</span></span>
<span data-ttu-id="749a2-130">Especifica o caminho da API Web, que é a última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="749a2-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="749a2-131">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="749a2-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="749a2-132">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-133">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="749a2-133">-Protocols</span></span>
<span data-ttu-id="749a2-134">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="749a2-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="749a2-135">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="749a2-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="749a2-136">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="749a2-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="749a2-137">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="749a2-138">-ServiceUrl</span></span>
<span data-ttu-id="749a2-139">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="749a2-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="749a2-140">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="749a2-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="749a2-141">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="749a2-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="749a2-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="749a2-143">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="749a2-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="749a2-144">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="749a2-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="749a2-146">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="749a2-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="749a2-147">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="749a2-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749a2-148">CommonParameters</span></span>
<span data-ttu-id="749a2-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749a2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749a2-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="749a2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749a2-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="749a2-151">INPUTS</span></span>

### <span data-ttu-id="749a2-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="749a2-152">None</span></span>
<span data-ttu-id="749a2-153">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="749a2-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="749a2-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="749a2-154">OUTPUTS</span></span>

### <span data-ttu-id="749a2-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="749a2-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="749a2-156">NOTES</span></span>

## <span data-ttu-id="749a2-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="749a2-157">RELATED LINKS</span></span>

[<span data-ttu-id="749a2-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="749a2-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="749a2-160">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="749a2-161">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="749a2-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="749a2-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


