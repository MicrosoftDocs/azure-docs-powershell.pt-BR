---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597941"
---
# <span data-ttu-id="be739-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="be739-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="be739-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be739-102">SYNOPSIS</span></span>
<span data-ttu-id="be739-103">Modifica um diagnóstico de gerenciamento de API no escopo global ou de API.</span><span class="sxs-lookup"><span data-stu-id="be739-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="be739-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be739-104">SYNTAX</span></span>

### <span data-ttu-id="be739-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="be739-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be739-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="be739-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be739-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be739-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be739-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be739-108">DESCRIPTION</span></span>
<span data-ttu-id="be739-109">O cmdlet **set-AzApiManagementDiagnostic** atualiza o diagnóstico que é configurado no escopo global ou da API.</span><span class="sxs-lookup"><span data-stu-id="be739-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="be739-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be739-110">EXAMPLES</span></span>

### <span data-ttu-id="be739-111">Exemplo 1: modificar um diagnóstico no escopo global</span><span class="sxs-lookup"><span data-stu-id="be739-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="be739-112">Esse comando modifica a porcentagem de amostragem de diagnóstico especificada de 100 para 50%</span><span class="sxs-lookup"><span data-stu-id="be739-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="be739-113">OS</span><span class="sxs-lookup"><span data-stu-id="be739-113">PARAMETERS</span></span>

### <span data-ttu-id="be739-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="be739-114">-AlwaysLog</span></span>
<span data-ttu-id="be739-115">Especifica para quais tipos de mensagens as configurações de amostragem não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="be739-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="be739-116">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be739-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="be739-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="be739-117">-ApiId</span></span>
<span data-ttu-id="be739-118">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="be739-118">Identifier of existing API.</span></span>
<span data-ttu-id="be739-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be739-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="be739-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="be739-120">-BackendSetting</span></span>
<span data-ttu-id="be739-121">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o back-end.</span><span class="sxs-lookup"><span data-stu-id="be739-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="be739-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be739-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="be739-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="be739-123">-Context</span></span>
<span data-ttu-id="be739-124">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="be739-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="be739-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be739-125">This parameter is required.</span></span>

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

### <span data-ttu-id="be739-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be739-126">-DefaultProfile</span></span>
<span data-ttu-id="be739-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be739-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be739-128">-Diagnosticid</span><span class="sxs-lookup"><span data-stu-id="be739-128">-DiagnosticId</span></span>
<span data-ttu-id="be739-129">Identificador de diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="be739-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="be739-130">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be739-130">This parameter is required.</span></span>

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

### <span data-ttu-id="be739-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="be739-131">-FrontEndSetting</span></span>
<span data-ttu-id="be739-132">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="be739-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="be739-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be739-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="be739-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be739-134">-InputObject</span></span>
<span data-ttu-id="be739-135">Instância do PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="be739-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="be739-136">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be739-136">This parameter is required.</span></span>

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

### <span data-ttu-id="be739-137">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="be739-137">-LoggerId</span></span>
<span data-ttu-id="be739-138">Identificador do agente para o qual enviar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="be739-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="be739-139">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be739-139">This parameter is required.</span></span>

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

### <span data-ttu-id="be739-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be739-140">-PassThru</span></span>
<span data-ttu-id="be739-141">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. PsApiManagementDiagnostic. Models. que representa o tipo de diagnóstico definido.</span><span class="sxs-lookup"><span data-stu-id="be739-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="be739-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be739-142">-ResourceId</span></span>
<span data-ttu-id="be739-143">Resourcebinding de diagnóstico ou diagnóstico de API.</span><span class="sxs-lookup"><span data-stu-id="be739-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="be739-144">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="be739-144">This parameter is required.</span></span>

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

### <span data-ttu-id="be739-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="be739-145">-SamplingSetting</span></span>
<span data-ttu-id="be739-146">Configuração de amostragem do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="be739-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="be739-147">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="be739-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="be739-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be739-148">-Confirm</span></span>
<span data-ttu-id="be739-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be739-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be739-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be739-150">-WhatIf</span></span>
<span data-ttu-id="be739-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be739-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be739-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be739-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be739-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be739-153">CommonParameters</span></span>
<span data-ttu-id="be739-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be739-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be739-155">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be739-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be739-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be739-156">INPUTS</span></span>

### <span data-ttu-id="be739-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="be739-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="be739-158">System. String</span><span class="sxs-lookup"><span data-stu-id="be739-158">System.String</span></span>

### <span data-ttu-id="be739-159">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="be739-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="be739-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="be739-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="be739-161">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="be739-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="be739-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="be739-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be739-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be739-163">OUTPUTS</span></span>

### <span data-ttu-id="be739-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="be739-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="be739-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be739-165">NOTES</span></span>

## <span data-ttu-id="be739-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be739-166">RELATED LINKS</span></span>
