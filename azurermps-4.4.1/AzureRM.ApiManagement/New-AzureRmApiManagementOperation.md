---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431219"
---
# <span data-ttu-id="61dcc-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="61dcc-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="61dcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="61dcc-103">Cria uma operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61dcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61dcc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61dcc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="61dcc-106">O cmdlet **New-AzureRmApiManagementOperation** cria uma operação de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="61dcc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61dcc-107">EXAMPLES</span></span>

### <span data-ttu-id="61dcc-108">Exemplo 1: criar uma operação de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="61dcc-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="61dcc-109">Esse comando cria uma operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="61dcc-110">Exemplo 2: criar uma operação de gerenciamento de API com detalhes de solicitação e resposta</span><span class="sxs-lookup"><span data-stu-id="61dcc-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="61dcc-111">Este exemplo cria uma operação de gerenciamento de API com detalhes de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="61dcc-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="61dcc-112">OS</span><span class="sxs-lookup"><span data-stu-id="61dcc-112">PARAMETERS</span></span>

### <span data-ttu-id="61dcc-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="61dcc-113">-ApiId</span></span>
<span data-ttu-id="61dcc-114">Especifica o identificador da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="61dcc-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="61dcc-115">-Context</span></span>
<span data-ttu-id="61dcc-116">Especifica a instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="61dcc-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="61dcc-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="61dcc-117">-Description</span></span>
<span data-ttu-id="61dcc-118">Especifica a descrição da nova operação de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="61dcc-119">-Método</span><span class="sxs-lookup"><span data-stu-id="61dcc-119">-Method</span></span>
<span data-ttu-id="61dcc-120">Especifica o método HTTP da nova operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="61dcc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="61dcc-121">-Name</span></span>
<span data-ttu-id="61dcc-122">Especifica o nome de exibição da nova operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="61dcc-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="61dcc-123">-OperationId</span></span>
<span data-ttu-id="61dcc-124">Especifica o identificador da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="61dcc-125">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="61dcc-125">-Request</span></span>
<span data-ttu-id="61dcc-126">Especifica os detalhes da operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="61dcc-127">-Respostas</span><span class="sxs-lookup"><span data-stu-id="61dcc-127">-Responses</span></span>
<span data-ttu-id="61dcc-128">Especifica uma matriz de possíveis respostas de operação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="61dcc-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="61dcc-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="61dcc-129">-TemplateParameters</span></span>
<span data-ttu-id="61dcc-130">Especifica uma matriz de parâmetros definidos no parâmetro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="61dcc-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="61dcc-131">Se você não especificar esse parâmetro, um valor padrão será gerado com base no *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="61dcc-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="61dcc-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="61dcc-132">-UrlTemplate</span></span>
<span data-ttu-id="61dcc-133">Especifica o modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="61dcc-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="61dcc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dcc-134">-DefaultProfile</span></span>
<span data-ttu-id="61dcc-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61dcc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61dcc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dcc-136">CommonParameters</span></span>
<span data-ttu-id="61dcc-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dcc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dcc-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61dcc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dcc-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61dcc-139">INPUTS</span></span>

## <span data-ttu-id="61dcc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61dcc-140">OUTPUTS</span></span>

### <span data-ttu-id="61dcc-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="61dcc-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="61dcc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61dcc-142">NOTES</span></span>

## <span data-ttu-id="61dcc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61dcc-143">RELATED LINKS</span></span>

[<span data-ttu-id="61dcc-144">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="61dcc-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="61dcc-145">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="61dcc-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="61dcc-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="61dcc-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


