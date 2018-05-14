# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Alterações interruptivas no Microsoft Azure PowerShell 3.0.0.

Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.  Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.  Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.

## <a name="table-of-contents"></a>Sumário
1. [Alterações interruptivas nos cmdlets do Data Lake Store](#breaking-changes-to-data-lake-store-cmdlets)
2. [Alterações interruptivas em cmdlets de ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
3. [Alterações interruptivas em cmdlets de Rede](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Alterações interruptivas nos cmdlets do Data Lake Store

Os seguintes cmdlets foram afetados por esta versão ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Esse cmdlet foi removido e substituído por ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- O cmdlet antigo retornou um objeto complexo que representa a lista de controle de acesso (ACL). O novo cmdlet retorna uma lista simples de entradas na ACL do caminho escolhido.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Esse cmdlet substitui o cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)`` antigo.
- O novo cmdlet retorna uma lista simples de entradas na ACL do caminho escolhido, com o tipo ``DataLakeStoreItemAce[]``.
- A saída desse cmdlet pode ser passada para o parâmetro ``-Acl`` dos cmdlets a seguir:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Esses cmdlets agora aceitam ``DataLakeStoreItemAce[]`` como parâmetro de ``-Acl``.
- ``DataLakeStoreItemAce[]`` é retornado por ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Alterações interruptivas em cmdlets de ApiManagement

Os seguintes cmdlets foram afetados por esta versão ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):

**New-AzureRmApiManagementVirtualNetwork**
- Os parâmetros necessários para fazer referência a uma rede virtual alterada de exigir SubnetName e VnetId para SubnetResourceId no formato ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Substituição do cmdlet Set-AzureRmApiManagementVirtualNetworks**
- O Cmdlet foi preterido porque havia mais de uma maneira de definir a Rede Virtual associada à implantação de ApiManagement.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Alterações interruptivas em cmdlets de Rede

Os seguintes cmdlets foram afetados por esta versão ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):

**New-AzureRmVirtualNetworkGateway**
- Descrição do que foi alterado ``:- Bool parameter:-ActiveActive`` foi removido e ``SwitchParameter:-EnableActiveActiveFeature`` foi adicionado para habilitar o recurso Ativo-Ativo no gateway de rede virtual recém-criado.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- Descrição do que foi alterado ``:- Bool parameter:-ActiveActive`` foi removido e dois ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` foram adicionados para habilitar e desabilitar o recurso Ativo-Ativo no gateway de rede virtual.

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