---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 1d735e82ced497268ec13ce228736eee32674a90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771415"
---
# <span data-ttu-id="8149a-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8149a-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="8149a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8149a-102">SYNOPSIS</span></span>
<span data-ttu-id="8149a-103">Cria uma operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-103">Creates an API management operation.</span></span>

## <span data-ttu-id="8149a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8149a-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8149a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8149a-105">DESCRIPTION</span></span>
<span data-ttu-id="8149a-106">O cmdlet **New-AzApiManagementOperation** cria uma operação de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="8149a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8149a-107">EXAMPLES</span></span>

### <span data-ttu-id="8149a-108">Exemplo 1: criar uma operação de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="8149a-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="8149a-109">Esse comando cria uma operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="8149a-110">Exemplo 2: criar uma operação de gerenciamento de API com detalhes de solicitação e resposta</span><span class="sxs-lookup"><span data-stu-id="8149a-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="8149a-111">Este exemplo cria uma operação de gerenciamento de API com detalhes de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="8149a-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="8149a-112">OS</span><span class="sxs-lookup"><span data-stu-id="8149a-112">PARAMETERS</span></span>

### <span data-ttu-id="8149a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8149a-113">-ApiId</span></span>
<span data-ttu-id="8149a-114">Especifica o identificador da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="8149a-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8149a-115">-ApiRevision</span></span>
<span data-ttu-id="8149a-116">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="8149a-116">Identifier of API Revision.</span></span> <span data-ttu-id="8149a-117">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8149a-117">This parameter is optional.</span></span> <span data-ttu-id="8149a-118">Se não for especificado, a operação será anexada à revisão da API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="8149a-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="8149a-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8149a-119">-Context</span></span>
<span data-ttu-id="8149a-120">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8149a-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8149a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8149a-121">-DefaultProfile</span></span>
<span data-ttu-id="8149a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8149a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8149a-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8149a-123">-Description</span></span>
<span data-ttu-id="8149a-124">Especifica a descrição da nova operação de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="8149a-125">-Método</span><span class="sxs-lookup"><span data-stu-id="8149a-125">-Method</span></span>
<span data-ttu-id="8149a-126">Especifica o método HTTP da nova operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="8149a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8149a-127">-Name</span></span>
<span data-ttu-id="8149a-128">Especifica o nome de exibição da nova operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="8149a-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8149a-129">-OperationId</span></span>
<span data-ttu-id="8149a-130">Especifica o identificador da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="8149a-131">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="8149a-131">-Request</span></span>
<span data-ttu-id="8149a-132">Especifica os detalhes da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8149a-133">-Respostas</span><span class="sxs-lookup"><span data-stu-id="8149a-133">-Responses</span></span>
<span data-ttu-id="8149a-134">Especifica uma matriz de possíveis respostas de operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="8149a-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8149a-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="8149a-135">-TemplateParameters</span></span>
<span data-ttu-id="8149a-136">Especifica uma matriz de parâmetros definidos no parâmetro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="8149a-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="8149a-137">Se você não especificar esse parâmetro, um valor padrão será gerado com base no *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="8149a-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8149a-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="8149a-138">-UrlTemplate</span></span>
<span data-ttu-id="8149a-139">Especifica o modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="8149a-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="8149a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8149a-140">CommonParameters</span></span>
<span data-ttu-id="8149a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8149a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8149a-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8149a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8149a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8149a-143">INPUTS</span></span>

### <span data-ttu-id="8149a-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8149a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8149a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8149a-145">System.String</span></span>

### <span data-ttu-id="8149a-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="8149a-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="8149a-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="8149a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="8149a-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="8149a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="8149a-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8149a-149">OUTPUTS</span></span>

### <span data-ttu-id="8149a-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8149a-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="8149a-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8149a-151">NOTES</span></span>

## <span data-ttu-id="8149a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8149a-152">RELATED LINKS</span></span>

[<span data-ttu-id="8149a-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8149a-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="8149a-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8149a-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="8149a-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8149a-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


