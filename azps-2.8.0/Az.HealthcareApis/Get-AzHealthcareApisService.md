---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 0f5aff6cfe499d9d0ef37d299babb178b437c2e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596314"
---
# <span data-ttu-id="de650-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="de650-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="de650-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de650-102">SYNOPSIS</span></span>
<span data-ttu-id="de650-103">Obter os metadados de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="de650-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="de650-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de650-104">SYNTAX</span></span>

### <span data-ttu-id="de650-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="de650-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de650-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de650-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de650-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de650-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de650-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de650-108">DESCRIPTION</span></span>
<span data-ttu-id="de650-109">Obtém contas de serviço fhir de healthcareApis existentes criadas na assinatura especificada ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de650-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="de650-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de650-110">EXAMPLES</span></span>

### <span data-ttu-id="de650-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de650-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="de650-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de650-112">Example 2</span></span>

<span data-ttu-id="de650-113">Obtém os metadados de todos os serviços do HealthcareApis no grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="de650-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="de650-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="de650-114">Example 3</span></span>

<span data-ttu-id="de650-115">Obtém os metadados de todos os serviços do HealthcareApis na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="de650-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="de650-116">OS</span><span class="sxs-lookup"><span data-stu-id="de650-116">PARAMETERS</span></span>

### <span data-ttu-id="de650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de650-117">-DefaultProfile</span></span>
<span data-ttu-id="de650-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de650-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de650-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="de650-119">-Name</span></span>
<span data-ttu-id="de650-120">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="de650-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de650-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de650-121">-ResourceGroupName</span></span>
<span data-ttu-id="de650-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de650-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de650-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de650-123">-ResourceId</span></span>
<span data-ttu-id="de650-124">Nome da identificação do recurso.</span><span class="sxs-lookup"><span data-stu-id="de650-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="de650-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de650-125">CommonParameters</span></span>
<span data-ttu-id="de650-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de650-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de650-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de650-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de650-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de650-128">INPUTS</span></span>

### <span data-ttu-id="de650-129">System. String</span><span class="sxs-lookup"><span data-stu-id="de650-129">System.String</span></span>

## <span data-ttu-id="de650-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de650-130">OUTPUTS</span></span>

### <span data-ttu-id="de650-131">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="de650-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="de650-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de650-132">NOTES</span></span>

## <span data-ttu-id="de650-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de650-133">RELATED LINKS</span></span>
