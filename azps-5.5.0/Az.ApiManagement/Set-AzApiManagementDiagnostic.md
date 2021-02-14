---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127159"
---
# <span data-ttu-id="84606-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84606-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="84606-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84606-102">SYNOPSIS</span></span>
<span data-ttu-id="84606-103">Modifica um diagnóstico de Gerenciamento de API no escopo Global ou api.</span><span class="sxs-lookup"><span data-stu-id="84606-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="84606-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84606-104">SYNTAX</span></span>

### <span data-ttu-id="84606-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="84606-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84606-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84606-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84606-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84606-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84606-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84606-108">DESCRIPTION</span></span>
<span data-ttu-id="84606-109">O cmdlet **Set-AzApiManagementDiagnostic** atualiza o diagnóstico que está configurado no Escopo global ou da Api.</span><span class="sxs-lookup"><span data-stu-id="84606-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="84606-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84606-110">EXAMPLES</span></span>

### <span data-ttu-id="84606-111">Exemplo 1: Modificar um diagnóstico no escopo Global</span><span class="sxs-lookup"><span data-stu-id="84606-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="84606-112">Este comando modifica a Porcentagem de Amostragem de Diagnóstico especificada de 100 a 50%</span><span class="sxs-lookup"><span data-stu-id="84606-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="84606-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="84606-113">Example 2</span></span>

<span data-ttu-id="84606-114">Modifica um diagnóstico de Gerenciamento de API no escopo Global ou api.</span><span class="sxs-lookup"><span data-stu-id="84606-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="84606-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="84606-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="84606-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84606-116">PARAMETERS</span></span>

### <span data-ttu-id="84606-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="84606-117">-AlwaysLog</span></span>
<span data-ttu-id="84606-118">Especifica quais tipos de configurações de amostragem de mensagens não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="84606-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="84606-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84606-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="84606-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="84606-120">-ApiId</span></span>
<span data-ttu-id="84606-121">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="84606-121">Identifier of existing API.</span></span>
<span data-ttu-id="84606-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84606-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="84606-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="84606-123">-BackendSetting</span></span>
<span data-ttu-id="84606-124">Configuração de diagnóstico para mensagens http de entrada/saída no Backend.</span><span class="sxs-lookup"><span data-stu-id="84606-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="84606-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84606-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="84606-126">-Contexto</span><span class="sxs-lookup"><span data-stu-id="84606-126">-Context</span></span>
<span data-ttu-id="84606-127">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84606-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="84606-128">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="84606-128">This parameter is required.</span></span>

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

### <span data-ttu-id="84606-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84606-129">-DefaultProfile</span></span>
<span data-ttu-id="84606-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84606-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84606-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="84606-131">-DiagnosticId</span></span>
<span data-ttu-id="84606-132">Identificador de Diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="84606-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="84606-133">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="84606-133">This parameter is required.</span></span>

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

### <span data-ttu-id="84606-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="84606-134">-FrontEndSetting</span></span>
<span data-ttu-id="84606-135">Configuração de diagnóstico para mensagens http de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="84606-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="84606-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84606-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="84606-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84606-137">-InputObject</span></span>
<span data-ttu-id="84606-138">Instância de PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="84606-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="84606-139">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="84606-139">This parameter is required.</span></span>

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

### <span data-ttu-id="84606-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="84606-140">-LoggerId</span></span>
<span data-ttu-id="84606-141">Identificador do loção para pressionar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="84606-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="84606-142">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="84606-142">This parameter is required.</span></span>

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

### <span data-ttu-id="84606-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84606-143">-PassThru</span></span>
<span data-ttu-id="84606-144">Se especificado, então instância de Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic que representa o diagnóstico definido.</span><span class="sxs-lookup"><span data-stu-id="84606-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="84606-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84606-145">-ResourceId</span></span>
<span data-ttu-id="84606-146">Arm ResourceId de Diagnóstico ou Diagnóstico da Api.</span><span class="sxs-lookup"><span data-stu-id="84606-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="84606-147">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="84606-147">This parameter is required.</span></span>

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

### <span data-ttu-id="84606-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="84606-148">-SamplingSetting</span></span>
<span data-ttu-id="84606-149">Configuração de Amostragem do Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="84606-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="84606-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84606-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="84606-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="84606-151">-Confirm</span></span>
<span data-ttu-id="84606-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84606-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84606-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84606-153">-WhatIf</span></span>
<span data-ttu-id="84606-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="84606-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84606-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84606-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84606-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84606-156">CommonParameters</span></span>
<span data-ttu-id="84606-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84606-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84606-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84606-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84606-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="84606-159">INPUTS</span></span>

### <span data-ttu-id="84606-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84606-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84606-161">System.String</span><span class="sxs-lookup"><span data-stu-id="84606-161">System.String</span></span>

### <span data-ttu-id="84606-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84606-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="84606-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="84606-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="84606-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="84606-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="84606-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84606-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84606-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="84606-166">OUTPUTS</span></span>

### <span data-ttu-id="84606-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84606-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="84606-168">Notas</span><span class="sxs-lookup"><span data-stu-id="84606-168">NOTES</span></span>

## <span data-ttu-id="84606-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84606-169">RELATED LINKS</span></span>
