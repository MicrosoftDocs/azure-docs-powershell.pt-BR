---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258886"
---
# <span data-ttu-id="78849-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="78849-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="78849-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78849-102">SYNOPSIS</span></span>
<span data-ttu-id="78849-103">Atualiza um serviço fhir healthcareApis existente.</span><span class="sxs-lookup"><span data-stu-id="78849-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="78849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78849-104">SYNTAX</span></span>

### <span data-ttu-id="78849-105">ServiceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="78849-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78849-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78849-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78849-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78849-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78849-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78849-108">DESCRIPTION</span></span>
<span data-ttu-id="78849-109">Atualiza um serviço fhir healthcareApis existente.</span><span class="sxs-lookup"><span data-stu-id="78849-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="78849-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78849-110">EXAMPLES</span></span>

### <span data-ttu-id="78849-111">Exemplo 1: atualiza o serviço healthcareapis existente chamado MyService no grupo de recursos MyResource do grupo de recursos com o cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="78849-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="78849-112">Exemplo 2: atualiza o serviço healthcareapis existente chamado MyService no grupo de recursos MyResource do grupo de recursos com o cosmosdb OfferThroughput = 500 e o URI da chave do Key Vault "https:// \<my-keyvault> . Vault.Azure.net/Keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="78849-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

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

## <span data-ttu-id="78849-113">OS</span><span class="sxs-lookup"><span data-stu-id="78849-113">PARAMETERS</span></span>

### <span data-ttu-id="78849-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="78849-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="78849-115">Lista de IDs de objetos de política de acesso.</span><span class="sxs-lookup"><span data-stu-id="78849-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="78849-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="78849-116">-AllowCorsCredential</span></span>
<span data-ttu-id="78849-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="78849-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="78849-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78849-118">-AsJob</span></span>
<span data-ttu-id="78849-119">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="78849-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="78849-120">-Audiência</span><span class="sxs-lookup"><span data-stu-id="78849-120">-Audience</span></span>
<span data-ttu-id="78849-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="78849-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="78849-122">-Autoridade</span><span class="sxs-lookup"><span data-stu-id="78849-122">-Authority</span></span>
<span data-ttu-id="78849-123">Autoridade HealthcareApis FhirService.</span><span class="sxs-lookup"><span data-stu-id="78849-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="78849-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="78849-124">-CorsHeader</span></span>
<span data-ttu-id="78849-125">HealthcareApis FhirService lista de cabeçalhos CORS.</span><span class="sxs-lookup"><span data-stu-id="78849-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="78849-126">Especifique os cabeçalhos HTTP que podem ser usados durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="78849-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="78849-127">Use "\*" para qualquer cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="78849-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="78849-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="78849-128">-CorsMaxAge</span></span>
<span data-ttu-id="78849-129">HealthcareApis FhirService CORS de idade máxima.</span><span class="sxs-lookup"><span data-stu-id="78849-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="78849-130">Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.</span><span class="sxs-lookup"><span data-stu-id="78849-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="78849-131">Exemplo: 600 significa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="78849-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="78849-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="78849-132">-CorsMethod</span></span>
<span data-ttu-id="78849-133">HealthcareApis FhirService lista de métodos CORS.</span><span class="sxs-lookup"><span data-stu-id="78849-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="78849-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="78849-134">-CorsOrigin</span></span>
<span data-ttu-id="78849-135">HealthcareApis FhirService lista de origens CORS.</span><span class="sxs-lookup"><span data-stu-id="78849-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="78849-136">Especifique as URLs de sites de origem que podem acessar essa API ou use "\*" para permitir o acesso de qualquer site.</span><span class="sxs-lookup"><span data-stu-id="78849-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="78849-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="78849-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="78849-138">HealthcareApis Fhir de serviço do CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="78849-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="78849-139">O URI da chave gerenciada pelo cliente para o banco de dados de backup.</span><span class="sxs-lookup"><span data-stu-id="78849-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="78849-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="78849-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="78849-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="78849-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="78849-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78849-142">-DefaultProfile</span></span>
<span data-ttu-id="78849-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78849-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78849-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="78849-144">-DisableCorsCredential</span></span>
<span data-ttu-id="78849-145">HealthcareApis FhirService CorsCredentials não permitido.</span><span class="sxs-lookup"><span data-stu-id="78849-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="78849-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="78849-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="78849-147">Desabilitar identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="78849-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="78849-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="78849-148">-DisableSmartProxy</span></span>
<span data-ttu-id="78849-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="78849-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="78849-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="78849-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="78849-151">Habilitar identidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="78849-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="78849-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="78849-152">-EnableSmartProxy</span></span>
<span data-ttu-id="78849-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="78849-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="78849-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="78849-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="78849-155">Nome da conta de armazenamento de exportação do serviço de HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="78849-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="78849-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78849-156">-InputObject</span></span>
<span data-ttu-id="78849-157">HealthcareApis fhir xxxx xxxx xxxx xxxx-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="78849-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="78849-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="78849-158">-Name</span></span>
<span data-ttu-id="78849-159">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="78849-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="78849-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="78849-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="78849-161">O tipo de acesso à rede para o serviço Fhir.</span><span class="sxs-lookup"><span data-stu-id="78849-161">The network access type for Fhir service.</span></span> <span data-ttu-id="78849-162">Comumente `Enabled` ou `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="78849-162">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="78849-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78849-163">-ResourceGroupName</span></span>
<span data-ttu-id="78849-164">Nome do grupo de recursos de serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="78849-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="78849-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78849-165">-ResourceId</span></span>
<span data-ttu-id="78849-166">ResourceId do serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="78849-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="78849-167">-Marca</span><span class="sxs-lookup"><span data-stu-id="78849-167">-Tag</span></span>
<span data-ttu-id="78849-168">HealthcareApis Fhir de conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="78849-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="78849-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78849-169">-Confirm</span></span>
<span data-ttu-id="78849-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78849-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78849-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78849-171">-WhatIf</span></span>
<span data-ttu-id="78849-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78849-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78849-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78849-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78849-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78849-174">CommonParameters</span></span>
<span data-ttu-id="78849-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78849-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78849-176">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78849-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78849-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78849-177">INPUTS</span></span>

### <span data-ttu-id="78849-178">Microsoft. Azure. Commands. HealthcareApis. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="78849-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="78849-179">System. String</span><span class="sxs-lookup"><span data-stu-id="78849-179">System.String</span></span>

## <span data-ttu-id="78849-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78849-180">OUTPUTS</span></span>

### <span data-ttu-id="78849-181">Microsoft. Azure. Commands. HealthcareApis. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="78849-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="78849-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78849-182">NOTES</span></span>

## <span data-ttu-id="78849-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78849-183">RELATED LINKS</span></span>
