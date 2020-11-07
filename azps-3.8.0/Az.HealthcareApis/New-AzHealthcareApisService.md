---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f4bc87424707fe3f26da04a4984b2ae122d98a3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777362"
---
# <span data-ttu-id="9c520-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="9c520-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="9c520-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c520-102">SYNOPSIS</span></span>
<span data-ttu-id="9c520-103">Cria os metadados de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="9c520-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="9c520-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c520-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c520-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c520-105">DESCRIPTION</span></span>
<span data-ttu-id="9c520-106">Cria ou atualiza os metadados de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="9c520-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="9c520-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c520-107">EXAMPLES</span></span>

### <span data-ttu-id="9c520-108">Exemplo 1: cria um novo serviço do healthcareapis fhir do Azure chamado MyService no grupo de recursos MyResource do grupo de recursos em um local westus2 com cosmosdb oferecer throughput = 400</span><span class="sxs-lookup"><span data-stu-id="9c520-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

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

## <span data-ttu-id="9c520-109">OS</span><span class="sxs-lookup"><span data-stu-id="9c520-109">PARAMETERS</span></span>

### <span data-ttu-id="9c520-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="9c520-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="9c520-111">Lista de IDs de objetos de política de acesso.</span><span class="sxs-lookup"><span data-stu-id="9c520-111">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="9c520-112">-AllowCorsCredential</span></span>
<span data-ttu-id="9c520-113">HealthcareApis Fhir de serviço do AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="9c520-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c520-114">-AsJob</span></span>
<span data-ttu-id="9c520-115">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9c520-115">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-116">-Audiência</span><span class="sxs-lookup"><span data-stu-id="9c520-116">-Audience</span></span>
<span data-ttu-id="9c520-117">Público-alvo do serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="9c520-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="9c520-118">-Autoridade</span><span class="sxs-lookup"><span data-stu-id="9c520-118">-Authority</span></span>
<span data-ttu-id="9c520-119">Autoridade de serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="9c520-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="9c520-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="9c520-120">-CorsHeader</span></span>
<span data-ttu-id="9c520-121">Lista de serviços Fhir HealthcareApis do cabeçalho CORS.</span><span class="sxs-lookup"><span data-stu-id="9c520-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="9c520-122">Especifique os cabeçalhos HTTP que podem ser usados durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9c520-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="9c520-123">Use \* em qualquer cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9c520-123">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="9c520-124">-CorsMaxAge</span></span>
<span data-ttu-id="9c520-125">HealthcareApis Fhir de tempo máximo do CORS do serviço.</span><span class="sxs-lookup"><span data-stu-id="9c520-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="9c520-126">Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.</span><span class="sxs-lookup"><span data-stu-id="9c520-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="9c520-127">Exemplo: 600 significa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="9c520-127">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="9c520-128">-CorsMethod</span></span>
<span data-ttu-id="9c520-129">Lista de serviços Fhir HealthcareApis do método CORS.</span><span class="sxs-lookup"><span data-stu-id="9c520-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="9c520-130">-CorsOrigin</span></span>
<span data-ttu-id="9c520-131">Lista de serviços Fhir HealthcareApis da origem CORS.</span><span class="sxs-lookup"><span data-stu-id="9c520-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="9c520-132">Especifique as URLs de sites de origem que podem acessar essa API ou use \* para permitir o acesso de qualquer site.</span><span class="sxs-lookup"><span data-stu-id="9c520-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="9c520-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="9c520-134">HealthcareApis Fhir de serviço do CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="9c520-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c520-135">-DefaultProfile</span></span>
<span data-ttu-id="9c520-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c520-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c520-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="9c520-137">-EnableSmartProxy</span></span>
<span data-ttu-id="9c520-138">HealthcareApis Fhir de serviço do EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="9c520-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-139">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="9c520-139">-FhirVersion</span></span>
<span data-ttu-id="9c520-140">Versão do Fhir.</span><span class="sxs-lookup"><span data-stu-id="9c520-140">Fhir Version.</span></span>

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

### <span data-ttu-id="9c520-141">-Kind</span><span class="sxs-lookup"><span data-stu-id="9c520-141">-Kind</span></span>
<span data-ttu-id="9c520-142">Tipo de serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="9c520-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="9c520-143">O valor padrão é Fhir</span><span class="sxs-lookup"><span data-stu-id="9c520-143">The default value is Fhir</span></span>

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

### <span data-ttu-id="9c520-144">-Local</span><span class="sxs-lookup"><span data-stu-id="9c520-144">-Location</span></span>
<span data-ttu-id="9c520-145">Local do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="9c520-145">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="9c520-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c520-146">-Name</span></span>
<span data-ttu-id="9c520-147">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="9c520-147">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="9c520-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c520-148">-ResourceGroupName</span></span>
<span data-ttu-id="9c520-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c520-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c520-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="9c520-150">-Tag</span></span>
<span data-ttu-id="9c520-151">HealthcareApis Fhir de conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="9c520-151">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c520-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c520-152">-Confirm</span></span>
<span data-ttu-id="9c520-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c520-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c520-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c520-154">-WhatIf</span></span>
<span data-ttu-id="9c520-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c520-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c520-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c520-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c520-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c520-157">CommonParameters</span></span>
<span data-ttu-id="9c520-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c520-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c520-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c520-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c520-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c520-160">INPUTS</span></span>

### <span data-ttu-id="9c520-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9c520-161">System.String</span></span>

## <span data-ttu-id="9c520-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c520-162">OUTPUTS</span></span>

### <span data-ttu-id="9c520-163">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="9c520-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="9c520-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c520-164">NOTES</span></span>

## <span data-ttu-id="9c520-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c520-165">RELATED LINKS</span></span>
