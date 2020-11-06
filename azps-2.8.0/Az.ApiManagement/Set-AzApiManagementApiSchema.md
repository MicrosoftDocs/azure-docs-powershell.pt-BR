---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597949"
---
# <span data-ttu-id="3ec7f-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ec7f-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3ec7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ec7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec7f-103">Modifica um esquema de API</span><span class="sxs-lookup"><span data-stu-id="3ec7f-103">Modifies an API Schema</span></span>

## <span data-ttu-id="3ec7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ec7f-104">SYNTAX</span></span>

### <span data-ttu-id="3ec7f-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ec7f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec7f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ec7f-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec7f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ec7f-108">DESCRIPTION</span></span>
<span data-ttu-id="3ec7f-109">O cmdlet **set-AzApiManagementApiSchema** modifica um esquema de API de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="3ec7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-110">EXAMPLES</span></span>

### <span data-ttu-id="3ec7f-111">Exemplo 1: modifica um esquema de API</span><span class="sxs-lookup"><span data-stu-id="3ec7f-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="3ec7f-112">O exemplo atualiza o esquema de API</span><span class="sxs-lookup"><span data-stu-id="3ec7f-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="3ec7f-113">OS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-113">PARAMETERS</span></span>

### <span data-ttu-id="3ec7f-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-114">-ApiId</span></span>
<span data-ttu-id="3ec7f-115">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-115">Identifier of existing API.</span></span>
<span data-ttu-id="3ec7f-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3ec7f-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3ec7f-117">-Context</span></span>
<span data-ttu-id="3ec7f-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ec7f-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec7f-120">-DefaultProfile</span></span>
<span data-ttu-id="3ec7f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec7f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ec7f-122">-InputObject</span></span>
<span data-ttu-id="3ec7f-123">Instância do PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="3ec7f-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ec7f-125">-PassThru</span></span>
<span data-ttu-id="3ec7f-126">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement... Model. PsApiManagementApi que representa a API Set.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="3ec7f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-127">-ResourceId</span></span>
<span data-ttu-id="3ec7f-128">Resourcebinding do esquema de diagnóstico ou API.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="3ec7f-129">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="3ec7f-130">-SchemaDocument</span></span>
<span data-ttu-id="3ec7f-131">Documento de esquema de API como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-131">Api schema document as a string.</span></span> <span data-ttu-id="3ec7f-132">Esse parâmetro é obrigatório porque-SchemaDocumentFile não está especificado.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="3ec7f-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="3ec7f-134">ContentType do esquema de API.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-134">ContentType of the api Schema.</span></span> <span data-ttu-id="3ec7f-135">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="3ec7f-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="3ec7f-137">Caminho do arquivo de documento do esquema de API.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-137">Api schema document file path.</span></span> <span data-ttu-id="3ec7f-138">Esse parâmetro é obrigatório porque-SchemaDocument não está especificado.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec7f-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3ec7f-139">-SchemaId</span></span>
<span data-ttu-id="3ec7f-140">Identificador do esquema existente.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="3ec7f-141">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-141">This parameter is required.</span></span>

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

### <span data-ttu-id="3ec7f-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ec7f-142">-Confirm</span></span>
<span data-ttu-id="3ec7f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec7f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec7f-144">-WhatIf</span></span>
<span data-ttu-id="3ec7f-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ec7f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec7f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec7f-147">CommonParameters</span></span>
<span data-ttu-id="3ec7f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec7f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec7f-149">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ec7f-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec7f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ec7f-150">INPUTS</span></span>

### <span data-ttu-id="3ec7f-151">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ec7f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ec7f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec7f-152">System.String</span></span>

### <span data-ttu-id="3ec7f-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ec7f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="3ec7f-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ec7f-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3ec7f-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ec7f-155">OUTPUTS</span></span>

### <span data-ttu-id="3ec7f-156">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ec7f-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3ec7f-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ec7f-157">NOTES</span></span>

## <span data-ttu-id="3ec7f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ec7f-158">RELATED LINKS</span></span>

[<span data-ttu-id="3ec7f-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ec7f-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="3ec7f-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ec7f-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="3ec7f-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3ec7f-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

