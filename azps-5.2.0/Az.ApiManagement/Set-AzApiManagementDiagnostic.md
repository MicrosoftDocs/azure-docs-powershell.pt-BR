---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263454"
---
# <span data-ttu-id="84d23-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84d23-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="84d23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84d23-102">SYNOPSIS</span></span>
<span data-ttu-id="84d23-103">Modifica um diagnóstico de gerenciamento de API no escopo global ou de API.</span><span class="sxs-lookup"><span data-stu-id="84d23-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="84d23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84d23-104">SYNTAX</span></span>

### <span data-ttu-id="84d23-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="84d23-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d23-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84d23-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d23-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84d23-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d23-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84d23-108">DESCRIPTION</span></span>
<span data-ttu-id="84d23-109">O cmdlet **set-AzApiManagementDiagnostic** atualiza o diagnóstico que é configurado no escopo global ou da API.</span><span class="sxs-lookup"><span data-stu-id="84d23-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="84d23-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84d23-110">EXAMPLES</span></span>

### <span data-ttu-id="84d23-111">Exemplo 1: modificar um diagnóstico no escopo global</span><span class="sxs-lookup"><span data-stu-id="84d23-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="84d23-112">Esse comando modifica a porcentagem de amostragem de diagnóstico especificada de 100 para 50%</span><span class="sxs-lookup"><span data-stu-id="84d23-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="84d23-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="84d23-113">Example 2</span></span>

<span data-ttu-id="84d23-114">Modifica um diagnóstico de gerenciamento de API no escopo global ou de API.</span><span class="sxs-lookup"><span data-stu-id="84d23-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="84d23-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="84d23-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="84d23-116">OS</span><span class="sxs-lookup"><span data-stu-id="84d23-116">PARAMETERS</span></span>

### <span data-ttu-id="84d23-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="84d23-117">-AlwaysLog</span></span>
<span data-ttu-id="84d23-118">Especifica para quais tipos de mensagens as configurações de amostragem não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="84d23-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="84d23-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84d23-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="84d23-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="84d23-120">-ApiId</span></span>
<span data-ttu-id="84d23-121">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="84d23-121">Identifier of existing API.</span></span>
<span data-ttu-id="84d23-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84d23-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="84d23-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="84d23-123">-BackendSetting</span></span>
<span data-ttu-id="84d23-124">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o back-end.</span><span class="sxs-lookup"><span data-stu-id="84d23-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="84d23-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84d23-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="84d23-126">-Contexto</span><span class="sxs-lookup"><span data-stu-id="84d23-126">-Context</span></span>
<span data-ttu-id="84d23-127">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84d23-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="84d23-128">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="84d23-128">This parameter is required.</span></span>

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

### <span data-ttu-id="84d23-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d23-129">-DefaultProfile</span></span>
<span data-ttu-id="84d23-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84d23-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d23-131">-Diagnosticid</span><span class="sxs-lookup"><span data-stu-id="84d23-131">-DiagnosticId</span></span>
<span data-ttu-id="84d23-132">Identificador de diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="84d23-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="84d23-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="84d23-133">This parameter is required.</span></span>

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

### <span data-ttu-id="84d23-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="84d23-134">-FrontEndSetting</span></span>
<span data-ttu-id="84d23-135">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="84d23-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="84d23-136">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84d23-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="84d23-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d23-137">-InputObject</span></span>
<span data-ttu-id="84d23-138">Instância do PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="84d23-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="84d23-139">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="84d23-139">This parameter is required.</span></span>

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

### <span data-ttu-id="84d23-140">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="84d23-140">-LoggerId</span></span>
<span data-ttu-id="84d23-141">Identificador do agente para o qual enviar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="84d23-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="84d23-142">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="84d23-142">This parameter is required.</span></span>

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

### <span data-ttu-id="84d23-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d23-143">-PassThru</span></span>
<span data-ttu-id="84d23-144">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. PsApiManagementDiagnostic. Models. que representa o tipo de diagnóstico definido.</span><span class="sxs-lookup"><span data-stu-id="84d23-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="84d23-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d23-145">-ResourceId</span></span>
<span data-ttu-id="84d23-146">Resourcebinding de diagnóstico ou diagnóstico de API.</span><span class="sxs-lookup"><span data-stu-id="84d23-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="84d23-147">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="84d23-147">This parameter is required.</span></span>

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

### <span data-ttu-id="84d23-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="84d23-148">-SamplingSetting</span></span>
<span data-ttu-id="84d23-149">Configuração de amostragem do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="84d23-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="84d23-150">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="84d23-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="84d23-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84d23-151">-Confirm</span></span>
<span data-ttu-id="84d23-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d23-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d23-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d23-153">-WhatIf</span></span>
<span data-ttu-id="84d23-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84d23-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84d23-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84d23-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d23-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d23-156">CommonParameters</span></span>
<span data-ttu-id="84d23-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d23-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d23-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d23-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d23-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84d23-159">INPUTS</span></span>

### <span data-ttu-id="84d23-160">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84d23-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84d23-161">System. String</span><span class="sxs-lookup"><span data-stu-id="84d23-161">System.String</span></span>

### <span data-ttu-id="84d23-162">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84d23-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="84d23-163">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="84d23-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="84d23-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="84d23-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="84d23-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84d23-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84d23-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84d23-166">OUTPUTS</span></span>

### <span data-ttu-id="84d23-167">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="84d23-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="84d23-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84d23-168">NOTES</span></span>

## <span data-ttu-id="84d23-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84d23-169">RELATED LINKS</span></span>
