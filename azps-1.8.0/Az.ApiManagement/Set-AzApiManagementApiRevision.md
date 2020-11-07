---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771348"
---
# <span data-ttu-id="4cd76-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cd76-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="4cd76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cd76-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd76-103">Modifica uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="4cd76-103">Modifies an API Revision</span></span>

## <span data-ttu-id="4cd76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cd76-104">SYNTAX</span></span>

### <span data-ttu-id="4cd76-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cd76-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cd76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cd76-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd76-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cd76-107">DESCRIPTION</span></span>
<span data-ttu-id="4cd76-108">O cmdlet **set-AzApiManagementApiRevision** modifica uma revisão da API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd76-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="4cd76-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cd76-109">EXAMPLES</span></span>

### <span data-ttu-id="4cd76-110">Exemplo 1 modificar uma revisão de API</span><span class="sxs-lookup"><span data-stu-id="4cd76-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="4cd76-111">O cmdlet atualiza a `2` revisão da API `echo-api` com uma nova descrição, protocolo e caminho.</span><span class="sxs-lookup"><span data-stu-id="4cd76-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="4cd76-112">OS</span><span class="sxs-lookup"><span data-stu-id="4cd76-112">PARAMETERS</span></span>

### <span data-ttu-id="4cd76-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4cd76-113">-ApiId</span></span>
<span data-ttu-id="4cd76-114">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="4cd76-114">Identifier of existing API.</span></span>
<span data-ttu-id="4cd76-115">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cd76-116">-ApiRevision</span></span>
<span data-ttu-id="4cd76-117">Identificador da revisão de API existente.</span><span class="sxs-lookup"><span data-stu-id="4cd76-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="4cd76-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="4cd76-119">-AuthorizationScope</span></span>
<span data-ttu-id="4cd76-120">Escopo de operações OAuth.</span><span class="sxs-lookup"><span data-stu-id="4cd76-120">OAuth operations scope.</span></span>
<span data-ttu-id="4cd76-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-121">This parameter is optional.</span></span>
<span data-ttu-id="4cd76-122">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-122">Default value is $null.</span></span>

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

### <span data-ttu-id="4cd76-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="4cd76-123">-AuthorizationServerId</span></span>
<span data-ttu-id="4cd76-124">Identificador do servidor de autorização OAuth.</span><span class="sxs-lookup"><span data-stu-id="4cd76-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="4cd76-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-125">This parameter is optional.</span></span>
<span data-ttu-id="4cd76-126">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-126">Default value is $null.</span></span>
<span data-ttu-id="4cd76-127">Deve ser especificado se AuthorizationScope for especificado.</span><span class="sxs-lookup"><span data-stu-id="4cd76-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="4cd76-128">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4cd76-128">-Context</span></span>
<span data-ttu-id="4cd76-129">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4cd76-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4cd76-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-130">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd76-131">-DefaultProfile</span></span>
<span data-ttu-id="4cd76-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd76-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cd76-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4cd76-133">-Description</span></span>
<span data-ttu-id="4cd76-134">Descrição da API Web.</span><span class="sxs-lookup"><span data-stu-id="4cd76-134">Web API description.</span></span>
<span data-ttu-id="4cd76-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cd76-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cd76-136">-InputObject</span></span>
<span data-ttu-id="4cd76-137">Instância do PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4cd76-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="4cd76-138">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-138">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cd76-139">-Name</span></span>
<span data-ttu-id="4cd76-140">Nome da API da Web.</span><span class="sxs-lookup"><span data-stu-id="4cd76-140">Web API name.</span></span>
<span data-ttu-id="4cd76-141">Nome público da API como seria exibido nos portais de desenvolvedor e de administração.</span><span class="sxs-lookup"><span data-stu-id="4cd76-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="4cd76-142">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-142">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cd76-143">-PassThru</span></span>
<span data-ttu-id="4cd76-144">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement... Model. PsApiManagementApi que representa a API Set.</span><span class="sxs-lookup"><span data-stu-id="4cd76-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="4cd76-145">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4cd76-145">-Path</span></span>
<span data-ttu-id="4cd76-146">Caminho de API Web.</span><span class="sxs-lookup"><span data-stu-id="4cd76-146">Web API Path.</span></span>
<span data-ttu-id="4cd76-147">Última parte da URL pública da API.</span><span class="sxs-lookup"><span data-stu-id="4cd76-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="4cd76-148">Esta URL será usada por consumidores de API para enviar solicitações ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd76-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="4cd76-149">Deve ter de 1 a 400 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="4cd76-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="4cd76-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-150">This parameter is optional.</span></span>
<span data-ttu-id="4cd76-151">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-151">Default value is $null.</span></span>

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

### <span data-ttu-id="4cd76-152">-Protocolos</span><span class="sxs-lookup"><span data-stu-id="4cd76-152">-Protocols</span></span>
<span data-ttu-id="4cd76-153">Protocolos de API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="4cd76-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="4cd76-154">Protocolos em que a API é disponibilizada.</span><span class="sxs-lookup"><span data-stu-id="4cd76-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="4cd76-155">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-155">This parameter is required.</span></span>
<span data-ttu-id="4cd76-156">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-156">Default value is $null.</span></span>

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

### <span data-ttu-id="4cd76-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4cd76-157">-ServiceUrl</span></span>
<span data-ttu-id="4cd76-158">Uma URL do serviço Web que expõe a API.</span><span class="sxs-lookup"><span data-stu-id="4cd76-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="4cd76-159">Essa URL será usada apenas pelo gerenciamento de APIs do Azure e não será publicada.</span><span class="sxs-lookup"><span data-stu-id="4cd76-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="4cd76-160">Deve ter de 1 a 2000 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="4cd76-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="4cd76-161">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd76-161">This parameter is required.</span></span>

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

### <span data-ttu-id="4cd76-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="4cd76-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="4cd76-163">Nome do cabeçalho da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4cd76-163">Subscription key header name.</span></span>
<span data-ttu-id="4cd76-164">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-164">This parameter is optional.</span></span>
<span data-ttu-id="4cd76-165">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-165">Default value is $null.</span></span>

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

### <span data-ttu-id="4cd76-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="4cd76-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="4cd76-167">Nome do parâmetro da cadeia de consulta da chave de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4cd76-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="4cd76-168">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="4cd76-168">This parameter is optional.</span></span>
<span data-ttu-id="4cd76-169">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="4cd76-169">Default value is $null.</span></span>

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

### <span data-ttu-id="4cd76-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cd76-170">-Confirm</span></span>
<span data-ttu-id="4cd76-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd76-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cd76-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd76-172">-WhatIf</span></span>
<span data-ttu-id="4cd76-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cd76-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd76-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cd76-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cd76-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd76-175">CommonParameters</span></span>
<span data-ttu-id="4cd76-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd76-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd76-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd76-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd76-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cd76-178">INPUTS</span></span>

### <span data-ttu-id="4cd76-179">System. String</span><span class="sxs-lookup"><span data-stu-id="4cd76-179">System.String</span></span>

### <span data-ttu-id="4cd76-180">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cd76-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cd76-181">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cd76-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="4cd76-182">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="4cd76-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="4cd76-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4cd76-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cd76-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cd76-184">OUTPUTS</span></span>

### <span data-ttu-id="4cd76-185">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cd76-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4cd76-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cd76-186">NOTES</span></span>

## <span data-ttu-id="4cd76-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cd76-187">RELATED LINKS</span></span>

[<span data-ttu-id="4cd76-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cd76-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="4cd76-189">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cd76-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="4cd76-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cd76-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)