---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595650"
---
# <span data-ttu-id="3e0e2-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="3e0e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0e2-103">Cria uma API.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-103">Creates an API.</span></span>

## <span data-ttu-id="3e0e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e0e2-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e0e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e0e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3e0e2-106">O cmdlet **New-AzApiManagementApi** cria uma API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="3e0e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e0e2-107">EXAMPLES</span></span>

### <span data-ttu-id="3e0e2-108">Exemplo 1: criar uma API</span><span class="sxs-lookup"><span data-stu-id="3e0e2-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="3e0e2-109">Esse comando cria uma API chamada EchoApi com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="3e0e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="3e0e2-110">PARAMETERS</span></span>

### <span data-ttu-id="3e0e2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3e0e2-111">-ApiId</span></span>
<span data-ttu-id="3e0e2-112">Especifica a ID da API a ser criada.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="3e0e2-113">Se você não especificar esse parâmetro, esse cmdlet gerará uma ID para você.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="3e0e2-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="3e0e2-114">-AuthorizationScope</span></span>
<span data-ttu-id="3e0e2-115">Especifica o escopo de operações do OAuth.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="3e0e2-116">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="3e0e2-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="3e0e2-117">-AuthorizationServerId</span></span>
<span data-ttu-id="3e0e2-118">Especifica a ID do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="3e0e2-119">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-119">The default value is $Null.</span></span>
<span data-ttu-id="3e0e2-120">Você deve especificar esse parâmetro se *AuthorizationScope* for especificado.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="3e0e2-121">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3e0e2-121">-Context</span></span>
<span data-ttu-id="3e0e2-122">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3e0e2-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3e0e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0e2-123">-DefaultProfile</span></span>
<span data-ttu-id="3e0e2-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e0e2-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3e0e2-125">-Description</span></span>
<span data-ttu-id="3e0e2-126">Especifica uma descrição para a API da Web.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="3e0e2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e0e2-127">-Name</span></span>
<span data-ttu-id="3e0e2-128">Especifica o nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="3e0e2-129">Esse é o nome público da API como aparece nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="3e0e2-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3e0e2-130">-Path</span></span>
<span data-ttu-id="3e0e2-131">Especifica o caminho da API Web, que é a última parte da URL pública da API e corresponde ao campo de sufixo de URL da Web API no portal de administração.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="3e0e2-132">Essa URL é usada por consumidores de API para enviar solicitações ao serviço Web e deve ter um a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="3e0e2-133">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="3e0e2-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="3e0e2-134">-ProductIds</span></span>
<span data-ttu-id="3e0e2-135">Especifica uma matriz de IDs de produto à qual será adicionada a nova API.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="3e0e2-136">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="3e0e2-136">-Protocols</span></span>
<span data-ttu-id="3e0e2-137">Especifica uma matriz de protocolos de API Web.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="3e0e2-138">Os valores válidos são http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-138">Valid values are http, https.</span></span>
<span data-ttu-id="3e0e2-139">Estes são os protocolos da Web sobre os quais a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="3e0e2-140">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="3e0e2-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="3e0e2-141">-ServiceUrl</span></span>
<span data-ttu-id="3e0e2-142">Especifica a URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="3e0e2-143">Essa URL é usada somente pelo gerenciamento de APIs do Azure, e não é publicada.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="3e0e2-144">A URL deve ter de um a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="3e0e2-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="3e0e2-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="3e0e2-146">Especifica o nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="3e0e2-147">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="3e0e2-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="3e0e2-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="3e0e2-149">Especifica o nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="3e0e2-150">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="3e0e2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0e2-151">CommonParameters</span></span>
<span data-ttu-id="3e0e2-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0e2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0e2-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e0e2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0e2-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e0e2-154">INPUTS</span></span>

### <span data-ttu-id="3e0e2-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e0e2-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e0e2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3e0e2-156">System.String</span></span>

### <span data-ttu-id="3e0e2-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="3e0e2-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="3e0e2-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="3e0e2-158">System.String[]</span></span>

## <span data-ttu-id="3e0e2-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e0e2-159">OUTPUTS</span></span>

### <span data-ttu-id="3e0e2-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3e0e2-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e0e2-161">NOTES</span></span>

## <span data-ttu-id="3e0e2-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e0e2-162">RELATED LINKS</span></span>

[<span data-ttu-id="3e0e2-163">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="3e0e2-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="3e0e2-165">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="3e0e2-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="3e0e2-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3e0e2-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


