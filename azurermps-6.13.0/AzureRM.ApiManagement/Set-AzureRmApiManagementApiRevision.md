---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432814"
---
# <span data-ttu-id="0d5b4-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d5b4-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="0d5b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5b4-103">Modifica uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="0d5b4-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d5b4-104">SYNTAX</span></span>

### <span data-ttu-id="0d5b4-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d5b4-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5b4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d5b4-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d5b4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d5b4-107">DESCRIPTION</span></span>
<span data-ttu-id="0d5b4-108">O cmdlet **set-AzureRmApiManagementApiRevision** modifica uma revisão da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="0d5b4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d5b4-109">EXAMPLES</span></span>

### <span data-ttu-id="0d5b4-110">Exemplo 1 modificar uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="0d5b4-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="0d5b4-111">O cmdlet atualiza a `2` revisão da API `echo-api` com uma nova descrição, protocolo e caminho.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="0d5b4-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d5b4-112">PARAMETERS</span></span>

### <span data-ttu-id="0d5b4-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0d5b4-113">-ApiId</span></span>
<span data-ttu-id="0d5b4-114">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-114">Identifier of existing API.</span></span>
<span data-ttu-id="0d5b4-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d5b4-116">-ApiRevision</span></span>
<span data-ttu-id="0d5b4-117">Identificador da revisão de API existente.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="0d5b4-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="0d5b4-119">-AuthorizationScope</span></span>
<span data-ttu-id="0d5b4-120">Escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-120">OAuth operations scope.</span></span>
<span data-ttu-id="0d5b4-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-121">This parameter is optional.</span></span>
<span data-ttu-id="0d5b4-122">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-122">Default value is $null.</span></span>

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

### <span data-ttu-id="0d5b4-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="0d5b4-123">-AuthorizationServerId</span></span>
<span data-ttu-id="0d5b4-124">Identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="0d5b4-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-125">This parameter is optional.</span></span>
<span data-ttu-id="0d5b4-126">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-126">Default value is $null.</span></span>
<span data-ttu-id="0d5b4-127">Deve ser especificado se AuthorizationScope for especificado.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="0d5b4-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0d5b4-128">-Context</span></span>
<span data-ttu-id="0d5b4-129">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0d5b4-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-130">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5b4-131">-DefaultProfile</span></span>
<span data-ttu-id="0d5b4-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d5b4-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0d5b4-133">-Description</span></span>
<span data-ttu-id="0d5b4-134">Descrição da API Web.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-134">Web API description.</span></span>
<span data-ttu-id="0d5b4-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="0d5b4-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d5b4-136">-InputObject</span></span>
<span data-ttu-id="0d5b4-137">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="0d5b4-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-138">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d5b4-139">-Name</span></span>
<span data-ttu-id="0d5b4-140">Nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-140">Web API name.</span></span>
<span data-ttu-id="0d5b4-141">Nome público da API como seria exibido nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="0d5b4-142">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-142">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d5b4-143">-PassThru</span></span>
<span data-ttu-id="0d5b4-144">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement... Model. PsApiManagementApi que representa a API Set.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="0d5b4-145">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0d5b4-145">-Path</span></span>
<span data-ttu-id="0d5b4-146">Caminho de API Web.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-146">Web API Path.</span></span>
<span data-ttu-id="0d5b4-147">Última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="0d5b4-148">Esta URL será usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="0d5b4-149">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="0d5b4-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-150">This parameter is optional.</span></span>
<span data-ttu-id="0d5b4-151">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-151">Default value is $null.</span></span>

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

### <span data-ttu-id="0d5b4-152">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="0d5b4-152">-Protocols</span></span>
<span data-ttu-id="0d5b4-153">Protocolos de API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="0d5b4-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="0d5b4-154">Protocolos em que a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="0d5b4-155">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-155">This parameter is required.</span></span>
<span data-ttu-id="0d5b4-156">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-156">Default value is $null.</span></span>

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

### <span data-ttu-id="0d5b4-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0d5b4-157">-ServiceUrl</span></span>
<span data-ttu-id="0d5b4-158">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="0d5b4-159">Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="0d5b4-160">Deve ter de 1 a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="0d5b4-161">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-161">This parameter is required.</span></span>

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

### <span data-ttu-id="0d5b4-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="0d5b4-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="0d5b4-163">Nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-163">Subscription key header name.</span></span>
<span data-ttu-id="0d5b4-164">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-164">This parameter is optional.</span></span>
<span data-ttu-id="0d5b4-165">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-165">Default value is $null.</span></span>

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

### <span data-ttu-id="0d5b4-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="0d5b4-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="0d5b4-167">Nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="0d5b4-168">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-168">This parameter is optional.</span></span>
<span data-ttu-id="0d5b4-169">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-169">Default value is $null.</span></span>

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

### <span data-ttu-id="0d5b4-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d5b4-170">-Confirm</span></span>
<span data-ttu-id="0d5b4-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b4-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5b4-172">-WhatIf</span></span>
<span data-ttu-id="0d5b4-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d5b4-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-174">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b4-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5b4-175">CommonParameters</span></span>
<span data-ttu-id="0d5b4-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5b4-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5b4-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5b4-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5b4-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d5b4-178">INPUTS</span></span>

### <span data-ttu-id="0d5b4-179">System. String</span><span class="sxs-lookup"><span data-stu-id="0d5b4-179">System.String</span></span>

### <span data-ttu-id="0d5b4-180">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d5b4-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d5b4-181">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0d5b4-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="0d5b4-182">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d5b4-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0d5b4-183">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="0d5b4-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="0d5b4-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0d5b4-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d5b4-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d5b4-185">OUTPUTS</span></span>

### <span data-ttu-id="0d5b4-186">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0d5b4-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0d5b4-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d5b4-187">NOTES</span></span>

## <span data-ttu-id="0d5b4-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d5b4-188">RELATED LINKS</span></span>

[<span data-ttu-id="0d5b4-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d5b4-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="0d5b4-190">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d5b4-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="0d5b4-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d5b4-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
