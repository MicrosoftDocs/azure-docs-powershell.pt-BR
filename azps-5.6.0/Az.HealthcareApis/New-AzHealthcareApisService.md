---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: e99c060cc7446cbecc46040ec4a498cf9f545e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893299"
---
# <span data-ttu-id="b386d-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b386d-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="b386d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b386d-102">SYNOPSIS</span></span>
<span data-ttu-id="b386d-103">Cria os metadados de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="b386d-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="b386d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b386d-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b386d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b386d-105">DESCRIPTION</span></span>
<span data-ttu-id="b386d-106">Cria ou atualiza os metadados de uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="b386d-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="b386d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b386d-107">EXAMPLES</span></span>

### <span data-ttu-id="b386d-108">Exemplo 1 : cria um novo serviço do Azure healthcareapis fhir chamado MyService no grupo de recursos MyResourceGroup em um local westus2 com a produtividade da oferta do cosmosdb = 400</span><span class="sxs-lookup"><span data-stu-id="b386d-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
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

### <span data-ttu-id="b386d-109">Exemplo 2 : cria um novo serviço do Azure healthcareapis fhir chamado MyService no grupo de recursos MyResourceGroup em um local westus2 com a produtividade da oferta do cosmosdb = 400 e uri de chave de chave de cofre "https:// \<my-keyvault> .vault.azure.net/keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="b386d-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="b386d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b386d-110">PARAMETERS</span></span>

### <span data-ttu-id="b386d-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="b386d-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="b386d-112">Lista de IDs de objeto da Política de Acesso.</span><span class="sxs-lookup"><span data-stu-id="b386d-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="b386d-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b386d-113">-AllowCorsCredential</span></span>
<span data-ttu-id="b386d-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="b386d-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="b386d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b386d-115">-AsJob</span></span>
<span data-ttu-id="b386d-116">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b386d-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b386d-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="b386d-117">-Audience</span></span>
<span data-ttu-id="b386d-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="b386d-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="b386d-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="b386d-119">-Authority</span></span>
<span data-ttu-id="b386d-120">Autoridade de Serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b386d-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="b386d-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="b386d-121">-CorsHeader</span></span>
<span data-ttu-id="b386d-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="b386d-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="b386d-123">Especifique cabeçalhos HTTP que podem ser usados durante a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b386d-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="b386d-124">Use " \* " para qualquer header.</span><span class="sxs-lookup"><span data-stu-id="b386d-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="b386d-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="b386d-125">-CorsMaxAge</span></span>
<span data-ttu-id="b386d-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="b386d-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="b386d-127">Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.</span><span class="sxs-lookup"><span data-stu-id="b386d-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="b386d-128">Exemplo: 600 significa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="b386d-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="b386d-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="b386d-129">-CorsMethod</span></span>
<span data-ttu-id="b386d-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="b386d-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="b386d-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="b386d-131">-CorsOrigin</span></span>
<span data-ttu-id="b386d-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="b386d-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="b386d-133">Especifique URLs de sites de origem que possam acessar essa API ou use " \* " para permitir o acesso de qualquer site.</span><span class="sxs-lookup"><span data-stu-id="b386d-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="b386d-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b386d-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="b386d-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="b386d-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="b386d-136">O URI da chave gerenciada pelo cliente para o banco de dados de suporte.</span><span class="sxs-lookup"><span data-stu-id="b386d-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="b386d-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="b386d-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="b386d-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="b386d-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="b386d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b386d-139">-DefaultProfile</span></span>
<span data-ttu-id="b386d-140">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b386d-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b386d-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b386d-141">-EnableSmartProxy</span></span>
<span data-ttu-id="b386d-142">Serviço HealthcareApis Fhir EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b386d-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="b386d-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b386d-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="b386d-144">HealthcareApis Fhir Service Export Storage Account Name.</span><span class="sxs-lookup"><span data-stu-id="b386d-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="b386d-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="b386d-145">-FhirVersion</span></span>
<span data-ttu-id="b386d-146">Versão Fhir.</span><span class="sxs-lookup"><span data-stu-id="b386d-146">Fhir Version.</span></span>

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

### <span data-ttu-id="b386d-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="b386d-147">-Kind</span></span>
<span data-ttu-id="b386d-148">Tipo de Serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b386d-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="b386d-149">O valor padrão é Fhir</span><span class="sxs-lookup"><span data-stu-id="b386d-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="b386d-150">-Location</span><span class="sxs-lookup"><span data-stu-id="b386d-150">-Location</span></span>
<span data-ttu-id="b386d-151">Local do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b386d-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="b386d-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b386d-152">-ManagedIdentity</span></span>
<span data-ttu-id="b386d-153">Usar Identidade Gerenciada?</span><span class="sxs-lookup"><span data-stu-id="b386d-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="b386d-154">-Name</span><span class="sxs-lookup"><span data-stu-id="b386d-154">-Name</span></span>
<span data-ttu-id="b386d-155">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b386d-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="b386d-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b386d-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="b386d-157">O tipo de acesso à rede para o serviço Fhir.</span><span class="sxs-lookup"><span data-stu-id="b386d-157">The network access type for Fhir service.</span></span> <span data-ttu-id="b386d-158">Normalmente `Enabled` ou `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="b386d-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b386d-159">-ResourceGroupName</span></span>
<span data-ttu-id="b386d-160">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b386d-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="b386d-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="b386d-161">-Tag</span></span>
<span data-ttu-id="b386d-162">Marcas de conta de serviço HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b386d-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="b386d-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b386d-163">-Confirm</span></span>
<span data-ttu-id="b386d-164">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b386d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b386d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b386d-165">-WhatIf</span></span>
<span data-ttu-id="b386d-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b386d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b386d-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b386d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b386d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b386d-168">CommonParameters</span></span>
<span data-ttu-id="b386d-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b386d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b386d-170">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b386d-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b386d-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b386d-171">INPUTS</span></span>

### <span data-ttu-id="b386d-172">System.String</span><span class="sxs-lookup"><span data-stu-id="b386d-172">System.String</span></span>

## <span data-ttu-id="b386d-173">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b386d-173">OUTPUTS</span></span>

### <span data-ttu-id="b386d-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b386d-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b386d-175">NOTES</span><span class="sxs-lookup"><span data-stu-id="b386d-175">NOTES</span></span>

## <span data-ttu-id="b386d-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b386d-176">RELATED LINKS</span></span>
