---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943857"
---
# <span data-ttu-id="e51ac-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e51ac-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="e51ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e51ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e51ac-103">Modifica um diagnóstico de gerenciamento de API no escopo global ou de API.</span><span class="sxs-lookup"><span data-stu-id="e51ac-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="e51ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e51ac-104">SYNTAX</span></span>

### <span data-ttu-id="e51ac-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="e51ac-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51ac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e51ac-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51ac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e51ac-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e51ac-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e51ac-108">DESCRIPTION</span></span>
<span data-ttu-id="e51ac-109">O cmdlet **set-AzApiManagementDiagnostic** atualiza o diagnóstico que é configurado no escopo global ou da API.</span><span class="sxs-lookup"><span data-stu-id="e51ac-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="e51ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e51ac-110">EXAMPLES</span></span>

### <span data-ttu-id="e51ac-111">Exemplo 1: modificar um diagnóstico no escopo global</span><span class="sxs-lookup"><span data-stu-id="e51ac-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="e51ac-112">Esse comando modifica a porcentagem de amostragem de diagnóstico especificada de 100 para 50%</span><span class="sxs-lookup"><span data-stu-id="e51ac-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="e51ac-113">OS</span><span class="sxs-lookup"><span data-stu-id="e51ac-113">PARAMETERS</span></span>

### <span data-ttu-id="e51ac-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="e51ac-114">-AlwaysLog</span></span>
<span data-ttu-id="e51ac-115">Especifica para quais tipos de mensagens as configurações de amostragem não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e51ac-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="e51ac-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e51ac-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e51ac-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e51ac-117">-ApiId</span></span>
<span data-ttu-id="e51ac-118">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="e51ac-118">Identifier of existing API.</span></span>
<span data-ttu-id="e51ac-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e51ac-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51ac-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="e51ac-120">-BackendSetting</span></span>
<span data-ttu-id="e51ac-121">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o back-end.</span><span class="sxs-lookup"><span data-stu-id="e51ac-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="e51ac-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e51ac-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51ac-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e51ac-123">-Context</span></span>
<span data-ttu-id="e51ac-124">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e51ac-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e51ac-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e51ac-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e51ac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51ac-126">-DefaultProfile</span></span>
<span data-ttu-id="e51ac-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e51ac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51ac-128">-Diagnosticid</span><span class="sxs-lookup"><span data-stu-id="e51ac-128">-DiagnosticId</span></span>
<span data-ttu-id="e51ac-129">Identificador de diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="e51ac-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="e51ac-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e51ac-130">This parameter is required.</span></span>

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

### <span data-ttu-id="e51ac-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="e51ac-131">-FrontEndSetting</span></span>
<span data-ttu-id="e51ac-132">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="e51ac-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="e51ac-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e51ac-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51ac-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e51ac-134">-InputObject</span></span>
<span data-ttu-id="e51ac-135">Instância do PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e51ac-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="e51ac-136">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e51ac-136">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51ac-137">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="e51ac-137">-LoggerId</span></span>
<span data-ttu-id="e51ac-138">Identificador do agente para o qual enviar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e51ac-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="e51ac-139">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e51ac-139">This parameter is required.</span></span>

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

### <span data-ttu-id="e51ac-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e51ac-140">-PassThru</span></span>
<span data-ttu-id="e51ac-141">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. PsApiManagementDiagnostic. Models. que representa o tipo de diagnóstico definido.</span><span class="sxs-lookup"><span data-stu-id="e51ac-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="e51ac-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51ac-142">-ResourceId</span></span>
<span data-ttu-id="e51ac-143">Resourcebinding de diagnóstico ou diagnóstico de API.</span><span class="sxs-lookup"><span data-stu-id="e51ac-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="e51ac-144">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e51ac-144">This parameter is required.</span></span>

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

### <span data-ttu-id="e51ac-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e51ac-145">-SamplingSetting</span></span>
<span data-ttu-id="e51ac-146">Configuração de amostragem do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e51ac-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="e51ac-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e51ac-147">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51ac-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e51ac-148">-Confirm</span></span>
<span data-ttu-id="e51ac-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e51ac-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e51ac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51ac-150">-WhatIf</span></span>
<span data-ttu-id="e51ac-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e51ac-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e51ac-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e51ac-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e51ac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51ac-153">CommonParameters</span></span>
<span data-ttu-id="e51ac-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51ac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51ac-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e51ac-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51ac-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e51ac-156">INPUTS</span></span>

### <span data-ttu-id="e51ac-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e51ac-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e51ac-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e51ac-158">System.String</span></span>

### <span data-ttu-id="e51ac-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e51ac-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="e51ac-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e51ac-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="e51ac-161">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e51ac-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="e51ac-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e51ac-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e51ac-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e51ac-163">OUTPUTS</span></span>

### <span data-ttu-id="e51ac-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e51ac-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="e51ac-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e51ac-165">NOTES</span></span>

## <span data-ttu-id="e51ac-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e51ac-166">RELATED LINKS</span></span>
