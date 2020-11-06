---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431242"
---
# <span data-ttu-id="89255-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="89255-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89255-102">SYNOPSIS</span></span>
<span data-ttu-id="89255-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="89255-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89255-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89255-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89255-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89255-105">DESCRIPTION</span></span>
<span data-ttu-id="89255-106">O cmdlet **New-AzureRmApiManagementApi** cria uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="89255-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="89255-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89255-107">EXAMPLES</span></span>

### <span data-ttu-id="89255-108">Exemplo 1: criar uma API</span><span class="sxs-lookup"><span data-stu-id="89255-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="89255-109">Esse comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="89255-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="89255-110">OS</span><span class="sxs-lookup"><span data-stu-id="89255-110">PARAMETERS</span></span>

### <span data-ttu-id="89255-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="89255-111">-ApiId</span></span>
<span data-ttu-id="89255-112">Especifica a ID da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="89255-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="89255-113">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="89255-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="89255-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="89255-114">-AuthorizationScope</span></span>
<span data-ttu-id="89255-115">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="89255-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="89255-116">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="89255-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="89255-117">-AuthorizationServerId</span></span>
<span data-ttu-id="89255-118">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="89255-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="89255-119">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-119">The default value is $Null.</span></span>
<span data-ttu-id="89255-120">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="89255-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="89255-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="89255-121">-Context</span></span>
<span data-ttu-id="89255-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="89255-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89255-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="89255-123">-Description</span></span>
<span data-ttu-id="89255-124">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="89255-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="89255-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="89255-125">-Name</span></span>
<span data-ttu-id="89255-126">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="89255-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="89255-127">Esse é o nome público da API como aparece nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="89255-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="89255-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="89255-128">-Path</span></span>
<span data-ttu-id="89255-129">Especifica o caminho da API Web, que é a última parte da URL pública da API e corresponde ao campo de sufixo de URL da Web API no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="89255-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="89255-130">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="89255-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="89255-131">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="89255-132">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="89255-132">-ProductIds</span></span>
<span data-ttu-id="89255-133">Especifica uma matriz de IDs de produto à qual será adicionada a nova API.</span><span class="sxs-lookup"><span data-stu-id="89255-133">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="89255-134">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="89255-134">-Protocols</span></span>
<span data-ttu-id="89255-135">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="89255-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="89255-136">Os valores válidos são http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="89255-136">Valid values are http, https.</span></span>
<span data-ttu-id="89255-137">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="89255-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="89255-138">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="89255-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="89255-139">-ServiceUrl</span></span>
<span data-ttu-id="89255-140">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="89255-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="89255-141">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="89255-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="89255-142">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="89255-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="89255-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="89255-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="89255-144">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="89255-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="89255-145">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="89255-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="89255-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="89255-147">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="89255-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="89255-148">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="89255-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="89255-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89255-149">-DefaultProfile</span></span>
<span data-ttu-id="89255-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89255-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89255-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89255-151">CommonParameters</span></span>
<span data-ttu-id="89255-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89255-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89255-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89255-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89255-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89255-154">INPUTS</span></span>

## <span data-ttu-id="89255-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89255-155">OUTPUTS</span></span>

### <span data-ttu-id="89255-156">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="89255-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89255-157">NOTES</span></span>

## <span data-ttu-id="89255-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89255-158">RELATED LINKS</span></span>

[<span data-ttu-id="89255-159">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="89255-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="89255-161">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="89255-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="89255-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="89255-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


