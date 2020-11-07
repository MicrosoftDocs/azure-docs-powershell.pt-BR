---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947728"
---
# <span data-ttu-id="b9ab0-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b9ab0-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="b9ab0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ab0-103">Atualiza um serviço fhir healthcareApis existente.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="b9ab0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9ab0-104">SYNTAX</span></span>

### <span data-ttu-id="b9ab0-105">ServiceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9ab0-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ab0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ab0-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ab0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ab0-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ab0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9ab0-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ab0-109">Atualiza um serviço fhir healthcareApis existente.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="b9ab0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9ab0-110">EXAMPLES</span></span>

### <span data-ttu-id="b9ab0-111">Exemplo 1: atualiza o serviço healthcareapis existente chamado MyService no grupo de recursos MyResource do grupo de recursos com o cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

### <span data-ttu-id="b9ab0-112">Exemplo 2: atualiza o serviço healthcareapis existente chamado MyService no grupo de recursos MyResource do grupo de recursos com o cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

## <span data-ttu-id="b9ab0-113">OS</span><span class="sxs-lookup"><span data-stu-id="b9ab0-113">PARAMETERS</span></span>

### <span data-ttu-id="b9ab0-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="b9ab0-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="b9ab0-115">Lista de IDs de objetos de política de acesso.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b9ab0-116">-AllowCorsCredential</span></span>
<span data-ttu-id="b9ab0-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9ab0-118">-AsJob</span></span>
<span data-ttu-id="b9ab0-119">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b9ab0-120">-Audiência</span><span class="sxs-lookup"><span data-stu-id="b9ab0-120">-Audience</span></span>
<span data-ttu-id="b9ab0-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-122">-Autoridade</span><span class="sxs-lookup"><span data-stu-id="b9ab0-122">-Authority</span></span>
<span data-ttu-id="b9ab0-123">Autoridade HealthcareApis FhirService.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="b9ab0-124">-CorsHeader</span></span>
<span data-ttu-id="b9ab0-125">Lista de serviços Fhir HealthcareApis do cabeçalho CORS.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="b9ab0-126">Especifique os cabeçalhos HTTP que podem ser usados durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="b9ab0-127">Use \* em qualquer cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-127">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="b9ab0-128">-CorsMaxAge</span></span>
<span data-ttu-id="b9ab0-129">HealthcareApis Fhir de tempo máximo do CORS do serviço.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="b9ab0-130">Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="b9ab0-131">Exemplo: 600 significa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="b9ab0-132">-CorsMethod</span></span>
<span data-ttu-id="b9ab0-133">HealthcareApis FhirService lista de métodos CORS.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="b9ab0-134">-CorsOrigin</span></span>
<span data-ttu-id="b9ab0-135">HealthcareApis FhirService lista de origens CORS.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="b9ab0-136">Lista de serviços Fhir HealthcareApis da origem CORS.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="b9ab0-137">Especifique as URLs de sites de origem que podem acessar essa API ou use \* para permitir o acesso de qualquer site.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="b9ab0-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="b9ab0-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ab0-140">-DefaultProfile</span></span>
<span data-ttu-id="b9ab0-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ab0-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b9ab0-142">-DisableCorsCredential</span></span>
<span data-ttu-id="b9ab0-143">HealthcareApis FhirService CorsCredentials não permitido.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ab0-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="b9ab0-145">Desabilitar identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-145">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b9ab0-146">-DisableSmartProxy</span></span>
<span data-ttu-id="b9ab0-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b9ab0-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="b9ab0-149">Habilitar identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-149">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b9ab0-150">-EnableSmartProxy</span></span>
<span data-ttu-id="b9ab0-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9ab0-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="b9ab0-153">Nome da conta de armazenamento de exportação do serviço de HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9ab0-154">-InputObject</span></span>
<span data-ttu-id="b9ab0-155">HealthcareApis fhir xxxx xxxx xxxx xxxx-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-156">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9ab0-156">-Name</span></span>
<span data-ttu-id="b9ab0-157">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="b9ab0-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ab0-158">-ResourceGroupName</span></span>
<span data-ttu-id="b9ab0-159">Nome do grupo de recursos de serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="b9ab0-160">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ab0-160">-ResourceId</span></span>
<span data-ttu-id="b9ab0-161">ResourceId do serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="b9ab0-162">-Marca</span><span class="sxs-lookup"><span data-stu-id="b9ab0-162">-Tag</span></span>
<span data-ttu-id="b9ab0-163">HealthcareApis Fhir de conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-163">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ab0-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9ab0-164">-Confirm</span></span>
<span data-ttu-id="b9ab0-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ab0-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ab0-166">-WhatIf</span></span>
<span data-ttu-id="b9ab0-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ab0-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ab0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ab0-169">CommonParameters</span></span>
<span data-ttu-id="b9ab0-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ab0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ab0-171">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9ab0-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ab0-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9ab0-172">INPUTS</span></span>

### <span data-ttu-id="b9ab0-173">System. String</span><span class="sxs-lookup"><span data-stu-id="b9ab0-173">System.String</span></span>

### <span data-ttu-id="b9ab0-174">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b9ab0-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b9ab0-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9ab0-175">OUTPUTS</span></span>

### <span data-ttu-id="b9ab0-176">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b9ab0-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b9ab0-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9ab0-177">NOTES</span></span>

## <span data-ttu-id="b9ab0-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ab0-178">RELATED LINKS</span></span>
