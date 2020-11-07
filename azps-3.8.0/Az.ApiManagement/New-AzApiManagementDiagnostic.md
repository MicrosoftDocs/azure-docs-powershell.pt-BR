---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: 1c3bea7efffe066ec85b44ec9e5f0f7c222efcf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942241"
---
# <span data-ttu-id="6e3e9-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="6e3e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3e9-103">Cria um novo diagnóstico no escopo global ou na API.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="6e3e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e3e9-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e3e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e3e9-105">DESCRIPTION</span></span>
<span data-ttu-id="6e3e9-106">O cmdlet **New-AzApiManagementDiagnostic** cria uma entidade de diagnóstico em escopo global ou escopo de API específico.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="6e3e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e3e9-107">EXAMPLES</span></span>

### <span data-ttu-id="6e3e9-108">Exemplo 1: criar um novo diagnóstico de escopo global</span><span class="sxs-lookup"><span data-stu-id="6e3e9-108">Example 1 : Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="6e3e9-109">Este exemplo cria uma entidade de diagnóstico no escopo global.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="6e3e9-110">Exemplo 2: criar um diagnóstico no escopo da API</span><span class="sxs-lookup"><span data-stu-id="6e3e9-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="6e3e9-111">O exemplo acima cria um diagnóstico para a API `httpbin` para registrar o cabeçalho e 100 bytes de corpo no `azuremonitor` Logger.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="6e3e9-112">OS</span><span class="sxs-lookup"><span data-stu-id="6e3e9-112">PARAMETERS</span></span>

### <span data-ttu-id="6e3e9-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="6e3e9-113">-AlwaysLog</span></span>
<span data-ttu-id="6e3e9-114">Especifica para quais tipos de mensagens as configurações de amostragem não devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="6e3e9-115">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e3e9-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6e3e9-116">-ApiId</span></span>
<span data-ttu-id="6e3e9-117">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-117">Identifier of existing API.</span></span>
<span data-ttu-id="6e3e9-118">Se especificado, definirá a política de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="6e3e9-119">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-119">This parameters is required.</span></span>

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

### <span data-ttu-id="6e3e9-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-120">-BackendSetting</span></span>
<span data-ttu-id="6e3e9-121">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o back-end.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="6e3e9-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e3e9-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6e3e9-123">-Context</span></span>
<span data-ttu-id="6e3e9-124">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6e3e9-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-125">This parameter is required.</span></span>

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

### <span data-ttu-id="6e3e9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3e9-126">-DefaultProfile</span></span>
<span data-ttu-id="6e3e9-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3e9-128">-Diagnosticid</span><span class="sxs-lookup"><span data-stu-id="6e3e9-128">-DiagnosticId</span></span>
<span data-ttu-id="6e3e9-129">Identificador da entidade de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="6e3e9-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e3e9-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-131">-FrontEndSetting</span></span>
<span data-ttu-id="6e3e9-132">Configuração de diagnóstico para mensagens HTTP de entrada/saída para o gateway.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="6e3e9-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e3e9-134">-Loggerid</span><span class="sxs-lookup"><span data-stu-id="6e3e9-134">-LoggerId</span></span>
<span data-ttu-id="6e3e9-135">Identificador do agente para o qual enviar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="6e3e9-136">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-136">This parameter is required.</span></span>

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

### <span data-ttu-id="6e3e9-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-137">-SamplingSetting</span></span>
<span data-ttu-id="6e3e9-138">Configuração de amostragem do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="6e3e9-139">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e3e9-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e3e9-140">-Confirm</span></span>
<span data-ttu-id="6e3e9-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e3e9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e3e9-142">-WhatIf</span></span>
<span data-ttu-id="6e3e9-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e3e9-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e3e9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3e9-145">CommonParameters</span></span>
<span data-ttu-id="6e3e9-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3e9-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e3e9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3e9-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e3e9-148">INPUTS</span></span>

### <span data-ttu-id="6e3e9-149">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e3e9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e3e9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6e3e9-150">System.String</span></span>

### <span data-ttu-id="6e3e9-151">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="6e3e9-152">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6e3e9-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e3e9-153">OUTPUTS</span></span>

### <span data-ttu-id="6e3e9-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="6e3e9-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e3e9-155">NOTES</span></span>

## <span data-ttu-id="6e3e9-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e3e9-156">RELATED LINKS</span></span>

[<span data-ttu-id="6e3e9-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6e3e9-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6e3e9-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6e3e9-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6e3e9-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="6e3e9-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6e3e9-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)