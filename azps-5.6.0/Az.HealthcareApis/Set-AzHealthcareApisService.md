---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 2ff0f9f03524368e01b6edbcad5b8db8fef4fb21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893297"
---
# <span data-ttu-id="14a49-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14a49-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="14a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a49-102">SYNOPSIS</span></span>
<span data-ttu-id="14a49-103">Atualiza um serviço healthcareApis fhir existente.</span><span class="sxs-lookup"><span data-stu-id="14a49-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="14a49-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14a49-104">SYNTAX</span></span>

### <span data-ttu-id="14a49-105">ServiceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14a49-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14a49-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a49-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14a49-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a49-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a49-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14a49-108">DESCRIPTION</span></span>
<span data-ttu-id="14a49-109">Atualiza um serviço healthcareApis fhir existente.</span><span class="sxs-lookup"><span data-stu-id="14a49-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="14a49-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14a49-110">EXAMPLES</span></span>

### <span data-ttu-id="14a49-111">Exemplo 1 : atualiza o serviço de healthcareapis existente chamado MyService no grupo de recursos MyResourceGroup com o cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="14a49-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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
CosmosKeyVaultKeyUri    : 
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

### <span data-ttu-id="14a49-112">Exemplo 2: atualiza o serviço de healthcareapis existente chamado MyService no grupo de recursos MyResourceGroup com o cosmosdb OfferThroughput = 500 e uri de chave do cofre de chaves "https:// \<my-keyvault> .vault.azure.net/keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="14a49-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="14a49-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14a49-113">PARAMETERS</span></span>

### <span data-ttu-id="14a49-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="14a49-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="14a49-115">Lista de IDs de objeto da Política de Acesso.</span><span class="sxs-lookup"><span data-stu-id="14a49-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="14a49-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="14a49-116">-AllowCorsCredential</span></span>
<span data-ttu-id="14a49-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="14a49-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="14a49-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a49-118">-AsJob</span></span>
<span data-ttu-id="14a49-119">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="14a49-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="14a49-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="14a49-120">-Audience</span></span>
<span data-ttu-id="14a49-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="14a49-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="14a49-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="14a49-122">-Authority</span></span>
<span data-ttu-id="14a49-123">Autoridade HealthcareApis FhirService.</span><span class="sxs-lookup"><span data-stu-id="14a49-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="14a49-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="14a49-124">-CorsHeader</span></span>
<span data-ttu-id="14a49-125">HealthcareApis FhirService Lista de headers do Cors.</span><span class="sxs-lookup"><span data-stu-id="14a49-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="14a49-126">Especifique cabeçalhos HTTP que podem ser usados durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="14a49-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="14a49-127">Use " \* " para qualquer header.</span><span class="sxs-lookup"><span data-stu-id="14a49-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="14a49-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="14a49-128">-CorsMaxAge</span></span>
<span data-ttu-id="14a49-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="14a49-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="14a49-130">Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.</span><span class="sxs-lookup"><span data-stu-id="14a49-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="14a49-131">Exemplo: 600 significa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="14a49-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="14a49-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="14a49-132">-CorsMethod</span></span>
<span data-ttu-id="14a49-133">HealthcareApis FhirService Lista de métodos Cors.</span><span class="sxs-lookup"><span data-stu-id="14a49-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="14a49-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="14a49-134">-CorsOrigin</span></span>
<span data-ttu-id="14a49-135">HealthcareApis FhirService Lista de origens do Cors.</span><span class="sxs-lookup"><span data-stu-id="14a49-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="14a49-136">Especifique URLs de sites de origem que possam acessar essa API ou use " \* " para permitir o acesso de qualquer site.</span><span class="sxs-lookup"><span data-stu-id="14a49-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="14a49-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="14a49-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="14a49-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="14a49-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="14a49-139">O URI da chave gerenciada pelo cliente para o banco de dados de suporte.</span><span class="sxs-lookup"><span data-stu-id="14a49-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="14a49-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="14a49-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="14a49-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="14a49-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="14a49-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a49-142">-DefaultProfile</span></span>
<span data-ttu-id="14a49-143">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14a49-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a49-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="14a49-144">-DisableCorsCredential</span></span>
<span data-ttu-id="14a49-145">HealthcareApis FhirService CorsCredentials Não Permitido.</span><span class="sxs-lookup"><span data-stu-id="14a49-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="14a49-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="14a49-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="14a49-147">Desabilitar a Identidade Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="14a49-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="14a49-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="14a49-148">-DisableSmartProxy</span></span>
<span data-ttu-id="14a49-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="14a49-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="14a49-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="14a49-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="14a49-151">Habilitar a Identidade Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="14a49-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="14a49-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="14a49-152">-EnableSmartProxy</span></span>
<span data-ttu-id="14a49-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="14a49-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="14a49-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14a49-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="14a49-155">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="14a49-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="14a49-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a49-156">-InputObject</span></span>
<span data-ttu-id="14a49-157">Serviço fhir HealthcareApis canalizou a partir de Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="14a49-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="14a49-158">-Name</span><span class="sxs-lookup"><span data-stu-id="14a49-158">-Name</span></span>
<span data-ttu-id="14a49-159">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="14a49-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="14a49-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="14a49-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="14a49-161">O tipo de acesso à rede para o serviço Fhir.</span><span class="sxs-lookup"><span data-stu-id="14a49-161">The network access type for Fhir service.</span></span> <span data-ttu-id="14a49-162">Normalmente `Enabled` ou `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="14a49-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a49-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a49-163">-ResourceGroupName</span></span>
<span data-ttu-id="14a49-164">Nome do grupo de recursos do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="14a49-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="14a49-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a49-165">-ResourceId</span></span>
<span data-ttu-id="14a49-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="14a49-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="14a49-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="14a49-167">-Tag</span></span>
<span data-ttu-id="14a49-168">Marcas de conta de serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="14a49-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="14a49-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a49-169">-Confirm</span></span>
<span data-ttu-id="14a49-170">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14a49-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a49-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a49-171">-WhatIf</span></span>
<span data-ttu-id="14a49-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14a49-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a49-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14a49-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a49-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a49-174">CommonParameters</span></span>
<span data-ttu-id="14a49-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a49-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a49-176">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14a49-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a49-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14a49-177">INPUTS</span></span>

### <span data-ttu-id="14a49-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14a49-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="14a49-179">System.String</span><span class="sxs-lookup"><span data-stu-id="14a49-179">System.String</span></span>

## <span data-ttu-id="14a49-180">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14a49-180">OUTPUTS</span></span>

### <span data-ttu-id="14a49-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14a49-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="14a49-182">NOTES</span><span class="sxs-lookup"><span data-stu-id="14a49-182">NOTES</span></span>

## <span data-ttu-id="14a49-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14a49-183">RELATED LINKS</span></span>
