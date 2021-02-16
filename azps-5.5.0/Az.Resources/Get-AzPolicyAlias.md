---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113343"
---
# <span data-ttu-id="b61d6-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="b61d6-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="b61d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b61d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b61d6-103">Get-AzPolicyAlias recupera e saídas tipos de recursos de provedores do Azure que têm aliases definidos e corresponderem aos valores de parâmetros determinados.</span><span class="sxs-lookup"><span data-stu-id="b61d6-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="b61d6-104">Se nenhum parâmetro for fornecido, todos os tipos de recursos do provedor que contêm um alias serão saída.</span><span class="sxs-lookup"><span data-stu-id="b61d6-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="b61d6-105">A opção -ListAvailable modifica esse comportamento listando todos os tipos de recursos correspondentes, incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="b61d6-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="b61d6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b61d6-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61d6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b61d6-107">DESCRIPTION</span></span>
<span data-ttu-id="b61d6-108">O cmdlet **Get-AzPolicyAlias** obtém uma listagem de aliases de política.</span><span class="sxs-lookup"><span data-stu-id="b61d6-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="b61d6-109">Aliases de política são usados pela Política do Azure para se referir às propriedades do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b61d6-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="b61d6-110">São fornecidos parâmetros que limitam os itens na listagem, combinando várias propriedades do tipo de recurso ou seus aliases.</span><span class="sxs-lookup"><span data-stu-id="b61d6-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="b61d6-111">Um determinado valor de match corresponde se a cadeia de caracteres de destino contiver-a usando a comparação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b61d6-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="b61d6-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b61d6-112">EXAMPLES</span></span>

### <span data-ttu-id="b61d6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b61d6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

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

<span data-ttu-id="b61d6-114">Lista todos os tipos de recursos do provedor que têm um alias.</span><span class="sxs-lookup"><span data-stu-id="b61d6-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="b61d6-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b61d6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="b61d6-116">Lista todos os tipos de recursos do provedor, incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="b61d6-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="b61d6-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b61d6-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="b61d6-118">Lista todos os tipos de recursos do provedor cujo namespace corresponde a 'computar' e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="b61d6-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="b61d6-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b61d6-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

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

<span data-ttu-id="b61d6-120">Lista todos os tipos de recursos do provedor cujo tipo de recurso corresponde a "virtual" e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="b61d6-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="b61d6-121">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="b61d6-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

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

<span data-ttu-id="b61d6-122">Lista todos os tipos de recursos do provedor cujo tipo de recurso corresponde a "virtual", incluindo aqueles sem aliases.</span><span class="sxs-lookup"><span data-stu-id="b61d6-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="b61d6-123">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="b61d6-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="b61d6-124">Lista todos os tipos de recursos do provedor cujo namespace corresponde a "computação" e o tipo de recurso corresponde a "virtual" e contém um alias.</span><span class="sxs-lookup"><span data-stu-id="b61d6-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="b61d6-125">Observação: -NamespaceMatch e -ResourceTypeMatch fornecem jogos exclusivos, enquanto os outros são inclusivos.</span><span class="sxs-lookup"><span data-stu-id="b61d6-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="b61d6-126">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="b61d6-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

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

<span data-ttu-id="b61d6-127">Lista todos os tipos de recursos do provedor que contêm um alias 'virtual' correspondente.</span><span class="sxs-lookup"><span data-stu-id="b61d6-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="b61d6-128">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="b61d6-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

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

<span data-ttu-id="b61d6-129">Lista todos os tipos de recursos do provedor que contêm um alias correspondente "virtual" ou um alias com uma 'rede' correspondente ao caminho.</span><span class="sxs-lookup"><span data-stu-id="b61d6-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="b61d6-130">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="b61d6-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="b61d6-131">Lista todos os tipos de recursos do provedor com a versão da api alfa ou contendo um alias com uma versão da api alfa.</span><span class="sxs-lookup"><span data-stu-id="b61d6-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="b61d6-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b61d6-132">PARAMETERS</span></span>

### <span data-ttu-id="b61d6-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-133">-AliasMatch</span></span>
<span data-ttu-id="b61d6-134">Inclui nos itens de saída com aliases cujo nome corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="b61d6-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b61d6-135">-ApiVersion</span></span>
<span data-ttu-id="b61d6-136">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b61d6-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="b61d6-137">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b61d6-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="b61d6-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-138">-ApiVersionMatch</span></span>
<span data-ttu-id="b61d6-139">Inclui nos itens de saída cujos tipos de recursos ou aliases têm uma versão de api correspondente.</span><span class="sxs-lookup"><span data-stu-id="b61d6-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="b61d6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61d6-140">-DefaultProfile</span></span>
<span data-ttu-id="b61d6-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b61d6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b61d6-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b61d6-142">-ListAvailable</span></span>
<span data-ttu-id="b61d6-143">Inclui os itens correspondentes de saída com e sem aliases.</span><span class="sxs-lookup"><span data-stu-id="b61d6-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-144">-LocationMatch</span></span>
<span data-ttu-id="b61d6-145">Inclui nos itens de saída cujos tipos de recursos têm um local correspondente.</span><span class="sxs-lookup"><span data-stu-id="b61d6-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-146">-NamespaceMatch</span></span>
<span data-ttu-id="b61d6-147">Limita a saída para itens cujo namespace corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="b61d6-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-148">-PathMatch</span></span>
<span data-ttu-id="b61d6-149">Inclui nos itens de saída com aliases que contêm um caminho que corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="b61d6-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-150">-Pré-</span><span class="sxs-lookup"><span data-stu-id="b61d6-150">-Pre</span></span>
<span data-ttu-id="b61d6-151">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b61d6-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="b61d6-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="b61d6-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="b61d6-153">Limita a saída para itens cujo tipo de recurso corresponde a esse valor.</span><span class="sxs-lookup"><span data-stu-id="b61d6-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61d6-154">CommonParameters</span></span>
<span data-ttu-id="b61d6-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61d6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61d6-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b61d6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61d6-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="b61d6-157">INPUTS</span></span>

### <span data-ttu-id="b61d6-158">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b61d6-158">None</span></span>

## <span data-ttu-id="b61d6-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="b61d6-159">OUTPUTS</span></span>

### <span data-ttu-id="b61d6-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="b61d6-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="b61d6-161">Notas</span><span class="sxs-lookup"><span data-stu-id="b61d6-161">NOTES</span></span>

* <span data-ttu-id="b61d6-162">Para expandir os Aliases ou qualquer outra propriedade, canaliza a saída para `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="b61d6-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="b61d6-163">Por exemplo: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="b61d6-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="b61d6-164">Propriedades adicionais estão disponíveis na saída e podem ser exibidas por meio da canalização da saída `Format-List` para.</span><span class="sxs-lookup"><span data-stu-id="b61d6-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="b61d6-165">Por exemplo: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="b61d6-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="b61d6-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b61d6-166">RELATED LINKS</span></span>
