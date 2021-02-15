---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118083"
---
# <span data-ttu-id="c789d-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c789d-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="c789d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c789d-102">SYNOPSIS</span></span>
<span data-ttu-id="c789d-103">Obter detalhes do Diagnóstico configurado no nível de serviço ou no Nível da Api.</span><span class="sxs-lookup"><span data-stu-id="c789d-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="c789d-104">Os diagnósticos são usados para registrar solicitações/respostas do gateway de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="c789d-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="c789d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c789d-105">SYNTAX</span></span>

### <span data-ttu-id="c789d-106">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c789d-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c789d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c789d-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c789d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c789d-108">DESCRIPTION</span></span>
<span data-ttu-id="c789d-109">O **Get-AzApiManagementDiagnostic** obtém detalhes do diagnóstico configurado no serviço de gerenciamento de Api em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="c789d-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="c789d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c789d-110">EXAMPLES</span></span>

### <span data-ttu-id="c789d-111">Exemplo 1: Configure todo o diagnóstico no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="c789d-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="c789d-112">Esse comando configura todos os diagnósticos no serviço de Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="c789d-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="c789d-113">Exemplo 2: Configurar todos os diagnósticos no escopo da Api</span><span class="sxs-lookup"><span data-stu-id="c789d-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="c789d-114">Esse comando configura todos os diagnósticos no escopo `echo-api` da Api</span><span class="sxs-lookup"><span data-stu-id="c789d-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="c789d-115">Exemplo 3: Obter o diagnóstico de escopo da API especificado por uma ID</span><span class="sxs-lookup"><span data-stu-id="c789d-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="c789d-116">Esse comando configura `applicationinsights` o diagnóstico na `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="c789d-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="c789d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c789d-117">PARAMETERS</span></span>

### <span data-ttu-id="c789d-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c789d-118">-ApiId</span></span>
<span data-ttu-id="c789d-119">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="c789d-119">Identifier of existing API.</span></span>
<span data-ttu-id="c789d-120">Se especificado, retornará o diagnóstico de escopo da API.</span><span class="sxs-lookup"><span data-stu-id="c789d-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="c789d-121">Esses parâmetros são necessários.</span><span class="sxs-lookup"><span data-stu-id="c789d-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c789d-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c789d-122">-Context</span></span>
<span data-ttu-id="c789d-123">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c789d-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c789d-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c789d-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c789d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c789d-125">-DefaultProfile</span></span>
<span data-ttu-id="c789d-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c789d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c789d-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="c789d-127">-DiagnosticId</span></span>
<span data-ttu-id="c789d-128">Identificador de diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="c789d-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="c789d-129">Se especificado, retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="c789d-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="c789d-130">Esses parâmetros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="c789d-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c789d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c789d-131">-ResourceId</span></span>
<span data-ttu-id="c789d-132">Identificador de Recursos Arm de um Diagnóstico ou Diagnóstico de Api.</span><span class="sxs-lookup"><span data-stu-id="c789d-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="c789d-133">Se especificado, tentará encontrar o diagnóstico pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="c789d-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="c789d-134">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c789d-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c789d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c789d-135">CommonParameters</span></span>
<span data-ttu-id="c789d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c789d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c789d-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c789d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c789d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="c789d-138">INPUTS</span></span>

### <span data-ttu-id="c789d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c789d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c789d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c789d-140">System.String</span></span>

## <span data-ttu-id="c789d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="c789d-141">OUTPUTS</span></span>

### <span data-ttu-id="c789d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c789d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="c789d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="c789d-143">NOTES</span></span>

## <span data-ttu-id="c789d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c789d-144">RELATED LINKS</span></span>
