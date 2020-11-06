---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610218"
---
# <span data-ttu-id="ed80a-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed80a-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ed80a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed80a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed80a-103">Define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="ed80a-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed80a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed80a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed80a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed80a-105">DESCRIPTION</span></span>
<span data-ttu-id="ed80a-106">O cmdlet **set-AzureRmApiManagementOperation** define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="ed80a-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ed80a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed80a-107">EXAMPLES</span></span>

### <span data-ttu-id="ed80a-108">Exemplo 1: definir os detalhes da operação</span><span class="sxs-lookup"><span data-stu-id="ed80a-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ed80a-109">Esse comando define os detalhes da operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ed80a-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ed80a-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed80a-110">PARAMETERS</span></span>

### <span data-ttu-id="ed80a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ed80a-111">-ApiId</span></span>
<span data-ttu-id="ed80a-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="ed80a-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ed80a-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ed80a-113">-Context</span></span>
<span data-ttu-id="ed80a-114">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ed80a-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ed80a-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ed80a-115">-Description</span></span>
<span data-ttu-id="ed80a-116">Especifica a descrição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="ed80a-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ed80a-117">-Método</span><span class="sxs-lookup"><span data-stu-id="ed80a-117">-Method</span></span>
<span data-ttu-id="ed80a-118">Especifica o método HTTP da nova operação.</span><span class="sxs-lookup"><span data-stu-id="ed80a-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="ed80a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed80a-119">-Name</span></span>
<span data-ttu-id="ed80a-120">Especifica o nome de exibição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="ed80a-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="ed80a-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ed80a-121">-OperationId</span></span>
<span data-ttu-id="ed80a-122">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="ed80a-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="ed80a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed80a-123">-PassThru</span></span>
<span data-ttu-id="ed80a-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="ed80a-124">passthru</span></span>

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

### <span data-ttu-id="ed80a-125">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="ed80a-125">-Request</span></span>
<span data-ttu-id="ed80a-126">Especifica os detalhes da solicitação de operação.</span><span class="sxs-lookup"><span data-stu-id="ed80a-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="ed80a-127">-Respostas</span><span class="sxs-lookup"><span data-stu-id="ed80a-127">-Responses</span></span>
<span data-ttu-id="ed80a-128">Especifica uma matriz de respostas de operação possíveis.</span><span class="sxs-lookup"><span data-stu-id="ed80a-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="ed80a-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ed80a-129">-TemplateParameters</span></span>
<span data-ttu-id="ed80a-130">Especifica uma matriz ou parâmetros definidos no parâmetro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="ed80a-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ed80a-131">Se você não especificar um valor, um valor padrão será gerado com base no UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="ed80a-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ed80a-132">Use o parâmetro para fornecer mais detalhes sobre parâmetros como descrição, tipo e outros valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="ed80a-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="ed80a-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="ed80a-133">-UrlTemplate</span></span>
<span data-ttu-id="ed80a-134">Especifica o modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="ed80a-134">Specifies the URL template.</span></span>
<span data-ttu-id="ed80a-135">Por exemplo: clientes/{CID}/Orders/{oId}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="ed80a-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="ed80a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed80a-136">-DefaultProfile</span></span>
<span data-ttu-id="ed80a-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed80a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed80a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed80a-138">CommonParameters</span></span>
<span data-ttu-id="ed80a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed80a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed80a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed80a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed80a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed80a-141">INPUTS</span></span>

## <span data-ttu-id="ed80a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed80a-142">OUTPUTS</span></span>

### <span data-ttu-id="ed80a-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed80a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ed80a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed80a-144">NOTES</span></span>

## <span data-ttu-id="ed80a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed80a-145">RELATED LINKS</span></span>

[<span data-ttu-id="ed80a-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed80a-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ed80a-147">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed80a-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ed80a-148">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ed80a-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


