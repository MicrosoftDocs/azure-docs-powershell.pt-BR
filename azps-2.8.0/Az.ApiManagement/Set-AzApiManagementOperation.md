---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 0e5764ec40c05c6894715e718926714a4cbc7070
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597928"
---
# <span data-ttu-id="47508-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="47508-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="47508-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47508-102">SYNOPSIS</span></span>
<span data-ttu-id="47508-103">Define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="47508-103">Sets API operation details.</span></span>

## <span data-ttu-id="47508-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47508-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47508-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47508-105">DESCRIPTION</span></span>
<span data-ttu-id="47508-106">O cmdlet **set-AzApiManagementOperation** define detalhes da operação da API.</span><span class="sxs-lookup"><span data-stu-id="47508-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="47508-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47508-107">EXAMPLES</span></span>

### <span data-ttu-id="47508-108">Exemplo 1: definir os detalhes da operação</span><span class="sxs-lookup"><span data-stu-id="47508-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="47508-109">Esse comando define os detalhes da operação para gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="47508-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="47508-110">OS</span><span class="sxs-lookup"><span data-stu-id="47508-110">PARAMETERS</span></span>

### <span data-ttu-id="47508-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="47508-111">-ApiId</span></span>
<span data-ttu-id="47508-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="47508-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="47508-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="47508-113">-ApiRevision</span></span>
<span data-ttu-id="47508-114">Identificador da revisão da API.</span><span class="sxs-lookup"><span data-stu-id="47508-114">Identifier of API Revision.</span></span> <span data-ttu-id="47508-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="47508-115">This parameter is optional.</span></span> <span data-ttu-id="47508-116">Se não for especificado, a operação será atualizada na revisão da API ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="47508-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="47508-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="47508-117">-Context</span></span>
<span data-ttu-id="47508-118">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="47508-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47508-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47508-119">-DefaultProfile</span></span>
<span data-ttu-id="47508-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47508-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47508-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="47508-121">-Description</span></span>
<span data-ttu-id="47508-122">Especifica a descrição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="47508-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="47508-123">-Método</span><span class="sxs-lookup"><span data-stu-id="47508-123">-Method</span></span>
<span data-ttu-id="47508-124">Especifica o método HTTP da nova operação.</span><span class="sxs-lookup"><span data-stu-id="47508-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="47508-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="47508-125">-Name</span></span>
<span data-ttu-id="47508-126">Especifica o nome de exibição da nova operação.</span><span class="sxs-lookup"><span data-stu-id="47508-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="47508-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="47508-127">-OperationId</span></span>
<span data-ttu-id="47508-128">Especifica o identificador da operação existente.</span><span class="sxs-lookup"><span data-stu-id="47508-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="47508-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47508-129">-PassThru</span></span>
<span data-ttu-id="47508-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="47508-130">passthru</span></span>

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

### <span data-ttu-id="47508-131">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="47508-131">-Request</span></span>
<span data-ttu-id="47508-132">Especifica os detalhes da solicitação de operação.</span><span class="sxs-lookup"><span data-stu-id="47508-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="47508-133">-Respostas</span><span class="sxs-lookup"><span data-stu-id="47508-133">-Responses</span></span>
<span data-ttu-id="47508-134">Especifica uma matriz de respostas de operação possíveis.</span><span class="sxs-lookup"><span data-stu-id="47508-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="47508-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="47508-135">-TemplateParameters</span></span>
<span data-ttu-id="47508-136">Especifica uma matriz ou parâmetros definidos no parâmetro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="47508-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="47508-137">Se você não especificar um valor, um valor padrão será gerado com base no UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="47508-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="47508-138">Use o parâmetro para fornecer mais detalhes sobre parâmetros como descrição, tipo e outros valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="47508-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="47508-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="47508-139">-UrlTemplate</span></span>
<span data-ttu-id="47508-140">Especifica o modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="47508-140">Specifies the URL template.</span></span>
<span data-ttu-id="47508-141">Por exemplo: clientes/{CID}/Orders/{oId}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="47508-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="47508-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47508-142">-Confirm</span></span>
<span data-ttu-id="47508-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47508-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47508-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47508-144">-WhatIf</span></span>
<span data-ttu-id="47508-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47508-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47508-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47508-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47508-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47508-147">CommonParameters</span></span>
<span data-ttu-id="47508-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47508-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47508-149">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47508-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47508-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47508-150">INPUTS</span></span>

### <span data-ttu-id="47508-151">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47508-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47508-152">System. String</span><span class="sxs-lookup"><span data-stu-id="47508-152">System.String</span></span>

### <span data-ttu-id="47508-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="47508-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="47508-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="47508-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="47508-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="47508-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="47508-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47508-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47508-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47508-157">OUTPUTS</span></span>

### <span data-ttu-id="47508-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="47508-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="47508-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47508-159">NOTES</span></span>

## <span data-ttu-id="47508-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47508-160">RELATED LINKS</span></span>

[<span data-ttu-id="47508-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="47508-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="47508-162">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="47508-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="47508-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="47508-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


