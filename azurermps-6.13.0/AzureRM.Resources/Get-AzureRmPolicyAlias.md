---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRm.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAlias.md
ms.openlocfilehash: ee37ae0d7ed03bb760486c727df20f8579fa77c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603132"
---
# <span data-ttu-id="63f8e-101">Get-AzureRmPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="63f8e-101">Get-AzureRmPolicyAlias</span></span>

## <span data-ttu-id="63f8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="63f8e-103">Get-AzureRmPolicyAlias recupera e gera os tipos de recursos do provedor do Azure que têm aliases definidos e correspondem aos valores de parâmetro especificados.</span><span class="sxs-lookup"><span data-stu-id="63f8e-103">Get-AzureRmPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="63f8e-104">Se nenhum parâmetro for fornecido, todos os tipos de recursos de provedor que contiverem um alias serão de saída.</span><span class="sxs-lookup"><span data-stu-id="63f8e-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="63f8e-105">A opção-ListAvailable modifica esse comportamento listando todos os tipos de recurso correspondentes, incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="63f8e-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f8e-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63f8e-106">SYNTAX</span></span>

```
Get-AzureRmPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f8e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="63f8e-108">O cmdlet **Get-AzureRmPolicyAlias** Obtém uma listagem de aliases de política.</span><span class="sxs-lookup"><span data-stu-id="63f8e-108">The **Get-AzureRmPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="63f8e-109">Os aliases de política são usados pela política do Azure para se referir a propriedades de tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="63f8e-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="63f8e-110">Os parâmetros são fornecidos para limitar os itens na listagem combinando várias propriedades do tipo de recurso ou seus aliases.</span><span class="sxs-lookup"><span data-stu-id="63f8e-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="63f8e-111">Um determinado valor correspondente corresponde se a cadeia de caracteres de destino o contém usando a comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="63f8e-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="63f8e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63f8e-112">EXAMPLES</span></span>

### <span data-ttu-id="63f8e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63f8e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="63f8e-114">Lista todos os tipos de recursos de provedor que têm um alias.</span><span class="sxs-lookup"><span data-stu-id="63f8e-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="63f8e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="63f8e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="63f8e-116">Lista todos os tipos de recursos do provedor, incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="63f8e-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="63f8e-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="63f8e-117">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="63f8e-118">Lista todos os tipos de recursos de provedor cujo namespace corresponde a ' Compute ' e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="63f8e-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="63f8e-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="63f8e-119">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="63f8e-120">Lista todos os tipos de recursos de provedor cujo tipo de recurso corresponde a ' virtual ' e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="63f8e-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="63f8e-121">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="63f8e-121">Example 5</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="63f8e-122">Lista todos os tipos de recursos de provedor cujo tipo de recurso corresponde a ' virtual ', incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="63f8e-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="63f8e-123">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="63f8e-123">Example 6</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="63f8e-124">Lista todos os tipos de recursos de provedor cujo namespace coincide com ' Compute ' e o tipo de recurso corresponde ' virtual ' e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="63f8e-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="63f8e-125">Observação:-NamespaceMatch e-ResourceTypeMatch fornecem correspondências exclusivas, enquanto as outras são inclusivas.</span><span class="sxs-lookup"><span data-stu-id="63f8e-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="63f8e-126">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="63f8e-126">Example 7</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="63f8e-127">Lista todos os tipos de recursos do provedor que contêm um alias correspondente ' virtual '.</span><span class="sxs-lookup"><span data-stu-id="63f8e-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="63f8e-128">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="63f8e-128">Example 8</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="63f8e-129">Lista todos os tipos de recursos do provedor que contêm um alias correspondente ' virtual ' ou um alias com um caminho correspondente a ' Network '.</span><span class="sxs-lookup"><span data-stu-id="63f8e-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="63f8e-130">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="63f8e-130">Example 9</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="63f8e-131">Lista todos os tipos de recursos do provedor com a versão da API Alpha ou que contém um alias com uma versão da API alfa.</span><span class="sxs-lookup"><span data-stu-id="63f8e-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="63f8e-132">OS</span><span class="sxs-lookup"><span data-stu-id="63f8e-132">PARAMETERS</span></span>

### <span data-ttu-id="63f8e-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-133">-AliasMatch</span></span>
<span data-ttu-id="63f8e-134">Inclui os itens de saída com aliases cujo nome corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="63f8e-134">Includes in the output items with aliases whose name matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="63f8e-135">-ApiVersion</span></span>
<span data-ttu-id="63f8e-136">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="63f8e-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="63f8e-137">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="63f8e-137">If not specified, the API version is automatically determined as the latest available.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-138">-ApiVersionMatch</span></span>
<span data-ttu-id="63f8e-139">Inclui os itens de saída cujos tipos de recursos ou aliases têm uma versão de API correspondente.</span><span class="sxs-lookup"><span data-stu-id="63f8e-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f8e-140">-DefaultProfile</span></span>
<span data-ttu-id="63f8e-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63f8e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="63f8e-142">-ListAvailable</span></span>
<span data-ttu-id="63f8e-143">Inclui na saída itens correspondentes com e sem aliases.</span><span class="sxs-lookup"><span data-stu-id="63f8e-143">Includes in the output matching items with and without aliases.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-144">-LocationMatch</span></span>
<span data-ttu-id="63f8e-145">Inclui os itens de saída cujos tipos de recursos têm um local correspondente.</span><span class="sxs-lookup"><span data-stu-id="63f8e-145">Includes in the output items whose resource types have a matching location.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-146">-NamespaceMatch</span></span>
<span data-ttu-id="63f8e-147">Limita a saída para itens cujo namespace corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="63f8e-147">Limits the output to items whose namespace matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-148">-PathMatch</span></span>
<span data-ttu-id="63f8e-149">Inclui os itens de saída com aliases contendo um caminho que corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="63f8e-149">Includes in the output items with aliases containing a path that matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="63f8e-150">-Pre</span></span>
<span data-ttu-id="63f8e-151">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="63f8e-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="63f8e-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="63f8e-153">Limita a saída para itens cujo tipo de recurso corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="63f8e-153">Limits the output to items whose resource type matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f8e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f8e-154">CommonParameters</span></span>
<span data-ttu-id="63f8e-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f8e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f8e-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f8e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f8e-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63f8e-157">INPUTS</span></span>

## <span data-ttu-id="63f8e-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63f8e-158">OUTPUTS</span></span>

### <span data-ttu-id="63f8e-159">Microsoft. Azure. Commands. ResourceManager. cmdlets. Implementation. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="63f8e-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="63f8e-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63f8e-160">NOTES</span></span>

* <span data-ttu-id="63f8e-161">Para expandir os aliases ou qualquer outra propriedade, canalize a saída para `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="63f8e-161">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="63f8e-162">Por exemplo: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="63f8e-162">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="63f8e-163">As propriedades adicionais estão disponíveis na saída e podem ser exibidas ao canalizar a saída `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="63f8e-163">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="63f8e-164">Por exemplo: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="63f8e-164">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="63f8e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63f8e-165">RELATED LINKS</span></span>
