---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115109"
---
# <span data-ttu-id="150b3-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="150b3-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="150b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="150b3-102">SYNOPSIS</span></span>
<span data-ttu-id="150b3-103">Obtenha detalhes do diagnóstico configurado no nível de serviço ou no nível de API.</span><span class="sxs-lookup"><span data-stu-id="150b3-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="150b3-104">O diagnóstico é usado para registrar solicitações/respostas do gateway de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="150b3-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="150b3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="150b3-105">SYNTAX</span></span>

### <span data-ttu-id="150b3-106">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="150b3-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="150b3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="150b3-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="150b3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="150b3-108">DESCRIPTION</span></span>
<span data-ttu-id="150b3-109">**Get-AzApiManagementDiagnostic** Obtém detalhes dos diagnósticos configurados no serviço de gerenciamento de API em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="150b3-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="150b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="150b3-110">EXAMPLES</span></span>

### <span data-ttu-id="150b3-111">Exemplo 1: Obtenha todos os diagnósticos configurados no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="150b3-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="150b3-112">Esse comando obtém todos os diagnósticos configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="150b3-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="150b3-113">Exemplo 2: obter todos os diagnósticos configurados no escopo da API</span><span class="sxs-lookup"><span data-stu-id="150b3-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="150b3-114">Esse comando obtém todos os diagnósticos configurados no `echo-api` escopo da API</span><span class="sxs-lookup"><span data-stu-id="150b3-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="150b3-115">Exemplo 3: obter o diagnóstico de escopo de API especificado por uma ID</span><span class="sxs-lookup"><span data-stu-id="150b3-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="150b3-116">Esse comando obtém o `applicationinsights` diagnóstico configurado na API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="150b3-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="150b3-117">OS</span><span class="sxs-lookup"><span data-stu-id="150b3-117">PARAMETERS</span></span>

### <span data-ttu-id="150b3-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="150b3-118">-ApiId</span></span>
<span data-ttu-id="150b3-119">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="150b3-119">Identifier of existing API.</span></span>
<span data-ttu-id="150b3-120">Se especificado, retornará o diagnóstico de escopo de API.</span><span class="sxs-lookup"><span data-stu-id="150b3-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="150b3-121">Estes parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="150b3-121">This parameters is required.</span></span>

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

### <span data-ttu-id="150b3-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="150b3-122">-Context</span></span>
<span data-ttu-id="150b3-123">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="150b3-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="150b3-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="150b3-124">This parameter is required.</span></span>

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

### <span data-ttu-id="150b3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150b3-125">-DefaultProfile</span></span>
<span data-ttu-id="150b3-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="150b3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="150b3-127">-Diagnosticid</span><span class="sxs-lookup"><span data-stu-id="150b3-127">-DiagnosticId</span></span>
<span data-ttu-id="150b3-128">Identificador de diagnóstico existente.</span><span class="sxs-lookup"><span data-stu-id="150b3-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="150b3-129">Se especificado, retornará a política de escopo do produto.</span><span class="sxs-lookup"><span data-stu-id="150b3-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="150b3-130">Esses parâmetros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="150b3-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="150b3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="150b3-131">-ResourceId</span></span>
<span data-ttu-id="150b3-132">Identificador de recursos ARM de um diagnóstico ou diagnóstico de API.</span><span class="sxs-lookup"><span data-stu-id="150b3-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="150b3-133">Se especificado, tenta encontrar o diagnóstico pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="150b3-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="150b3-134">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="150b3-134">This parameter is required.</span></span>

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

### <span data-ttu-id="150b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150b3-135">CommonParameters</span></span>
<span data-ttu-id="150b3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150b3-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="150b3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150b3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="150b3-138">INPUTS</span></span>

### <span data-ttu-id="150b3-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="150b3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="150b3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="150b3-140">System.String</span></span>

## <span data-ttu-id="150b3-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="150b3-141">OUTPUTS</span></span>

### <span data-ttu-id="150b3-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="150b3-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="150b3-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="150b3-143">NOTES</span></span>

## <span data-ttu-id="150b3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="150b3-144">RELATED LINKS</span></span>
