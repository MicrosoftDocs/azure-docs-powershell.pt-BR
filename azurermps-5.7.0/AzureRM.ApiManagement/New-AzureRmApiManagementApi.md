---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610436"
---
# <span data-ttu-id="3ff21-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="3ff21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff21-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff21-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="3ff21-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff21-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ff21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ff21-105">DESCRIPTION</span></span>
<span data-ttu-id="3ff21-106">O cmdlet **New-AzureRmApiManagementApi** cria uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff21-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="3ff21-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ff21-107">EXAMPLES</span></span>

### <span data-ttu-id="3ff21-108">Exemplo 1: criar uma API</span><span class="sxs-lookup"><span data-stu-id="3ff21-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="3ff21-109">Esse comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="3ff21-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="3ff21-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ff21-110">PARAMETERS</span></span>

### <span data-ttu-id="3ff21-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3ff21-111">-ApiId</span></span>
<span data-ttu-id="3ff21-112">Especifica a ID da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="3ff21-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="3ff21-113">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="3ff21-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="3ff21-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="3ff21-114">-AuthorizationScope</span></span>
<span data-ttu-id="3ff21-115">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="3ff21-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="3ff21-116">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="3ff21-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="3ff21-117">-AuthorizationServerId</span></span>
<span data-ttu-id="3ff21-118">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="3ff21-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="3ff21-119">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-119">The default value is $Null.</span></span>
<span data-ttu-id="3ff21-120">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="3ff21-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="3ff21-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3ff21-121">-Context</span></span>
<span data-ttu-id="3ff21-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3ff21-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3ff21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff21-123">-DefaultProfile</span></span>
<span data-ttu-id="3ff21-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff21-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3ff21-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff21-125">-Description</span></span>
<span data-ttu-id="3ff21-126">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="3ff21-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="3ff21-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff21-127">-Name</span></span>
<span data-ttu-id="3ff21-128">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="3ff21-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="3ff21-129">Esse é o nome público da API como aparece nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="3ff21-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="3ff21-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3ff21-130">-Path</span></span>
<span data-ttu-id="3ff21-131">Especifica o caminho da API Web, que é a última parte da URL pública da API e corresponde ao campo de sufixo de URL da Web API no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="3ff21-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="3ff21-132">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3ff21-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="3ff21-133">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="3ff21-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="3ff21-134">-ProductIds</span></span>
<span data-ttu-id="3ff21-135">Especifica uma matriz de IDs de produto à qual será adicionada a nova API.</span><span class="sxs-lookup"><span data-stu-id="3ff21-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff21-136">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="3ff21-136">-Protocols</span></span>
<span data-ttu-id="3ff21-137">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="3ff21-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="3ff21-138">Os valores válidos são http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3ff21-138">Valid values are http, https.</span></span>
<span data-ttu-id="3ff21-139">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="3ff21-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="3ff21-140">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="3ff21-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="3ff21-141">-ServiceUrl</span></span>
<span data-ttu-id="3ff21-142">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="3ff21-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="3ff21-143">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="3ff21-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="3ff21-144">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3ff21-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="3ff21-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="3ff21-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="3ff21-146">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3ff21-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="3ff21-147">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="3ff21-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="3ff21-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="3ff21-149">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3ff21-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="3ff21-150">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3ff21-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="3ff21-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff21-151">CommonParameters</span></span>
<span data-ttu-id="3ff21-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff21-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff21-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff21-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff21-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ff21-154">INPUTS</span></span>

### <span data-ttu-id="3ff21-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ff21-155">None</span></span>
<span data-ttu-id="3ff21-156">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3ff21-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ff21-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ff21-157">OUTPUTS</span></span>

### <span data-ttu-id="3ff21-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3ff21-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ff21-159">NOTES</span></span>

## <span data-ttu-id="3ff21-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff21-160">RELATED LINKS</span></span>

[<span data-ttu-id="3ff21-161">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="3ff21-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="3ff21-163">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="3ff21-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="3ff21-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ff21-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


