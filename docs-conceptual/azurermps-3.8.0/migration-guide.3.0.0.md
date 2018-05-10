# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="e5660-101">Alterações interruptivas no Microsoft Azure PowerShell 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="e5660-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="e5660-102">Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5660-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="e5660-103">Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.</span><span class="sxs-lookup"><span data-stu-id="e5660-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="e5660-104">Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.</span><span class="sxs-lookup"><span data-stu-id="e5660-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="e5660-105">Sumário</span><span class="sxs-lookup"><span data-stu-id="e5660-105">Table of Contents</span></span>
1. [<span data-ttu-id="e5660-106">Alterações interruptivas nos cmdlets do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e5660-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="e5660-107">Alterações interruptivas em cmdlets de ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5660-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="e5660-108">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="e5660-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="e5660-109">Alterações interruptivas nos cmdlets do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e5660-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="e5660-110">Os seguintes cmdlets foram afetados por esta versão ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span><span class="sxs-lookup"><span data-stu-id="e5660-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="e5660-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="e5660-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="e5660-112">Esse cmdlet foi removido e substituído por ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="e5660-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="e5660-113">O cmdlet antigo retornou um objeto complexo que representa a lista de controle de acesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="e5660-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="e5660-114">O novo cmdlet retorna uma lista simples de entradas na ACL do caminho escolhido.</span><span class="sxs-lookup"><span data-stu-id="e5660-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="e5660-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="e5660-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="e5660-116">Esse cmdlet substitui o cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` antigo.</span><span class="sxs-lookup"><span data-stu-id="e5660-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="e5660-117">O novo cmdlet retorna uma lista simples de entradas na ACL do caminho escolhido, com o tipo ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="e5660-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="e5660-118">A saída desse cmdlet pode ser passada para o parâmetro ``-Acl`` dos cmdlets a seguir:</span><span class="sxs-lookup"><span data-stu-id="e5660-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="e5660-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="e5660-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="e5660-120">Esses cmdlets agora aceitam ``DataLakeStoreItemAce[]`` como parâmetro de ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="e5660-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="e5660-121">``DataLakeStoreItemAce[]`` é retornado por ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="e5660-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="e5660-122">Alterações interruptivas em cmdlets de ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e5660-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="e5660-123">Os seguintes cmdlets foram afetados por esta versão ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span><span class="sxs-lookup"><span data-stu-id="e5660-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="e5660-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="e5660-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="e5660-125">Os parâmetros necessários para fazer referência a uma rede virtual alterada de exigir SubnetName e VnetId para SubnetResourceId no formato ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span><span class="sxs-lookup"><span data-stu-id="e5660-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="e5660-126">**Substituição do cmdlet Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="e5660-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="e5660-127">O Cmdlet foi preterido porque havia mais de uma maneira de definir a Rede Virtual associada à implantação de ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e5660-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="e5660-128">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="e5660-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="e5660-129">Os seguintes cmdlets foram afetados por esta versão ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span><span class="sxs-lookup"><span data-stu-id="e5660-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="e5660-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="e5660-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="e5660-131">Descrição do que foi alterado ``:- Bool parameter:-ActiveActive`` foi removido e ``SwitchParameter:-EnableActiveActiveFeature`` foi adicionado para habilitar o recurso Ativo-Ativo no gateway de rede virtual recém-criado.</span><span class="sxs-lookup"><span data-stu-id="e5660-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="e5660-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e5660-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="e5660-133">Descrição do que foi alterado ``:- Bool parameter:-ActiveActive`` foi removido e dois ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` foram adicionados para habilitar e desabilitar o recurso Ativo-Ativo no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5660-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```