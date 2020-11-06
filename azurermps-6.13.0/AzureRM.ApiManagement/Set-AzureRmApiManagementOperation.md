---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427339"
---
# <span data-ttu-id="f4fe9-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f4fe9-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f4fe9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fe9-103">Define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4fe9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4fe9-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4fe9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="f4fe9-106">O cmdlet **set-AzureRmApiManagementOperation** define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="f4fe9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4fe9-107">EXAMPLES</span></span>

### <span data-ttu-id="f4fe9-108">Exemplo 1: definir os detalhes da operação</span><span class="sxs-lookup"><span data-stu-id="f4fe9-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="f4fe9-109">Esse comando define os detalhes da operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="f4fe9-110">OS</span><span class="sxs-lookup"><span data-stu-id="f4fe9-110">PARAMETERS</span></span>

### <span data-ttu-id="f4fe9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f4fe9-111">-ApiId</span></span>
<span data-ttu-id="f4fe9-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="f4fe9-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f4fe9-113">-ApiRevision</span></span>
<span data-ttu-id="f4fe9-114">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-114">Identifier of API Revision.</span></span> <span data-ttu-id="f4fe9-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-115">This parameter is optional.</span></span> <span data-ttu-id="f4fe9-116">Se não for especificado, a operação será atualizada na revisão da API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="f4fe9-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f4fe9-117">-Context</span></span>
<span data-ttu-id="f4fe9-118">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f4fe9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fe9-119">-DefaultProfile</span></span>
<span data-ttu-id="f4fe9-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fe9-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f4fe9-121">-Description</span></span>
<span data-ttu-id="f4fe9-122">Especifica a descrição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="f4fe9-123">-Método</span><span class="sxs-lookup"><span data-stu-id="f4fe9-123">-Method</span></span>
<span data-ttu-id="f4fe9-124">Especifica o método HTTP da nova operação.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="f4fe9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4fe9-125">-Name</span></span>
<span data-ttu-id="f4fe9-126">Especifica o nome de exibição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="f4fe9-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f4fe9-127">-OperationId</span></span>
<span data-ttu-id="f4fe9-128">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="f4fe9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4fe9-129">-PassThru</span></span>
<span data-ttu-id="f4fe9-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="f4fe9-130">passthru</span></span>

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

### <span data-ttu-id="f4fe9-131">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="f4fe9-131">-Request</span></span>
<span data-ttu-id="f4fe9-132">Especifica os detalhes da solicitação de operação.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="f4fe9-133">-Respostas</span><span class="sxs-lookup"><span data-stu-id="f4fe9-133">-Responses</span></span>
<span data-ttu-id="f4fe9-134">Especifica uma matriz de respostas de operação possíveis.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="f4fe9-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="f4fe9-135">-TemplateParameters</span></span>
<span data-ttu-id="f4fe9-136">Especifica uma matriz ou parâmetros definidos no parâmetro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f4fe9-137">Se você não especificar um valor, um valor padrão será gerado com base no UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="f4fe9-138">Use o parâmetro para fornecer mais detalhes sobre parâmetros como descrição, tipo e outros valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="f4fe9-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f4fe9-139">-UrlTemplate</span></span>
<span data-ttu-id="f4fe9-140">Especifica o modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-140">Specifies the URL template.</span></span>
<span data-ttu-id="f4fe9-141">Por exemplo: clientes/{CID}/Orders/{oId}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="f4fe9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fe9-142">CommonParameters</span></span>
<span data-ttu-id="f4fe9-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4fe9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fe9-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fe9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fe9-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4fe9-145">INPUTS</span></span>

### <span data-ttu-id="f4fe9-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4fe9-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4fe9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fe9-147">System.String</span></span>

### <span data-ttu-id="f4fe9-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="f4fe9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="f4fe9-149">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="f4fe9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="f4fe9-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="f4fe9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="f4fe9-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4fe9-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4fe9-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4fe9-152">OUTPUTS</span></span>

### <span data-ttu-id="f4fe9-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f4fe9-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f4fe9-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4fe9-154">NOTES</span></span>

## <span data-ttu-id="f4fe9-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4fe9-155">RELATED LINKS</span></span>

[<span data-ttu-id="f4fe9-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f4fe9-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f4fe9-157">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f4fe9-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f4fe9-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f4fe9-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


