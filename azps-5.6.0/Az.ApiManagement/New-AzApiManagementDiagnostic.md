---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890033"
---
# <span data-ttu-id="9b8b7-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9b8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8b7-103">Cria um novo diagnóstico no escopo Global ou no Escopo da Api.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="9b8b7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b8b7-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b8b7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8b7-106">O cmdlet **New-AzApiManagementDiagnostic** cria uma entidade de diagnóstico no escopo Global ou no escopo de Api específico.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="9b8b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8b7-108">Exemplo 1: Criar um novo Diagnóstico de escopo global</span><span class="sxs-lookup"><span data-stu-id="9b8b7-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="9b8b7-109">Este exemplo cria uma entidade de diagnóstico no Escopo Global.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="9b8b7-110">Exemplo 2: Criar um diagnóstico no escopo da Api</span><span class="sxs-lookup"><span data-stu-id="9b8b7-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="9b8b7-111">O exemplo acima cria um diagnóstico para a API registrar o `httpbin` Header e 100 Bytes de Corpo no `azuremonitor` log.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="9b8b7-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-112">PARAMETERS</span></span>

### <span data-ttu-id="9b8b7-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="9b8b7-113">-AlwaysLog</span></span>
<span data-ttu-id="9b8b7-114">Especifica para que tipo de configurações de amostragem de mensagens não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="9b8b7-115">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b8b7-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9b8b7-116">-ApiId</span></span>
<span data-ttu-id="9b8b7-117">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-117">Identifier of existing API.</span></span>
<span data-ttu-id="9b8b7-118">Se especificado, definirá a política de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="9b8b7-119">Esses parâmetros são necessários.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-119">This parameters is required.</span></span>

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

### <span data-ttu-id="9b8b7-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-120">-BackendSetting</span></span>
<span data-ttu-id="9b8b7-121">Configuração de diagnóstico para mensagens Http de entrada/saída para o Backend.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="9b8b7-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b8b7-123">-Context</span><span class="sxs-lookup"><span data-stu-id="9b8b7-123">-Context</span></span>
<span data-ttu-id="9b8b7-124">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b8b7-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8b7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8b7-126">-DefaultProfile</span></span>
<span data-ttu-id="9b8b7-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b8b7-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9b8b7-128">-DiagnosticId</span></span>
<span data-ttu-id="9b8b7-129">Identificador da entidade de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="9b8b7-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b8b7-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-131">-FrontEndSetting</span></span>
<span data-ttu-id="9b8b7-132">Configuração de diagnóstico para mensagens Http de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="9b8b7-133">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b8b7-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="9b8b7-134">-LoggerId</span></span>
<span data-ttu-id="9b8b7-135">Identificador do madeireiro para o que fazer o diagnóstico por push.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="9b8b7-136">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-136">This parameter is required.</span></span>

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

### <span data-ttu-id="9b8b7-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-137">-SamplingSetting</span></span>
<span data-ttu-id="9b8b7-138">Configuração de Amostragem do Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="9b8b7-139">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b8b7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b8b7-140">-Confirm</span></span>
<span data-ttu-id="9b8b7-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8b7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8b7-142">-WhatIf</span></span>
<span data-ttu-id="9b8b7-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8b7-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8b7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8b7-145">CommonParameters</span></span>
<span data-ttu-id="9b8b7-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8b7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8b7-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b8b7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8b7-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-148">INPUTS</span></span>

### <span data-ttu-id="9b8b7-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b8b7-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b8b7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9b8b7-150">System.String</span></span>

### <span data-ttu-id="9b8b7-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="9b8b7-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="9b8b7-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-153">OUTPUTS</span></span>

### <span data-ttu-id="9b8b7-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="9b8b7-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b8b7-155">NOTES</span></span>

## <span data-ttu-id="9b8b7-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b8b7-156">RELATED LINKS</span></span>

[<span data-ttu-id="9b8b7-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9b8b7-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9b8b7-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9b8b7-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9b8b7-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="9b8b7-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="9b8b7-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)