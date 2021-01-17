---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430184"
---
# <span data-ttu-id="7a595-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7a595-101">New-AzVMConfig</span></span>

## <span data-ttu-id="7a595-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a595-102">SYNOPSIS</span></span>
<span data-ttu-id="7a595-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="7a595-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="7a595-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a595-104">SYNTAX</span></span>

### <span data-ttu-id="7a595-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a595-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a595-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a595-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a595-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a595-107">DESCRIPTION</span></span>
<span data-ttu-id="7a595-108">O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a595-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="7a595-109">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="7a595-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="7a595-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a595-110">EXAMPLES</span></span>

### <span data-ttu-id="7a595-111">Exemplo 1: criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7a595-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="7a595-112">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7a595-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="7a595-113">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7a595-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7a595-114">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7a595-115">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7a595-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="7a595-116">OS</span><span class="sxs-lookup"><span data-stu-id="7a595-116">PARAMETERS</span></span>

### <span data-ttu-id="7a595-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="7a595-117">-AvailabilitySetId</span></span>
<span data-ttu-id="7a595-118">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a595-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="7a595-119">Para obter um objeto do conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7a595-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="7a595-120">O objeto de conjunto de disponibilidade contém uma propriedade de ID.</span><span class="sxs-lookup"><span data-stu-id="7a595-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="7a595-121">Máquinas virtuais especificadas no mesmo conjunto de disponibilidade são alocadas para nós diferentes para maximizar a disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a595-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="7a595-122">Para obter mais informações sobre conjuntos de disponibilidade, consulte [gerenciar a disponibilidade de máquinas virtuais](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="7a595-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="7a595-123">Para obter mais informações sobre a manutenção planejada do Azure, consulte [manutenção planejada para máquinas virtuais no Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="7a595-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="7a595-124">Atualmente, uma VM só pode ser adicionada ao conjunto de disponibilidade no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="7a595-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="7a595-125">O conjunto de disponibilidade para o qual a VM está sendo adicionada deve estar no mesmo grupo de recursos que o recurso de conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a595-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="7a595-126">Uma VM existente não pode ser adicionada a um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a595-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="7a595-127">Essa propriedade não pode existir juntamente com uma referência não nula. virtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="7a595-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a595-128">-DefaultProfile</span></span>
<span data-ttu-id="7a595-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a595-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a595-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7a595-130">-EnableUltraSSD</span></span>
<span data-ttu-id="7a595-131">Habilita um recurso para ter um ou mais discos de dados gerenciados com UltraSSD_LRS tipo de conta de armazenamento na VM.</span><span class="sxs-lookup"><span data-stu-id="7a595-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="7a595-132">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="7a595-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a595-133">-EvictionPolicy</span></span>
<span data-ttu-id="7a595-134">A política de remoção para a máquina virtual do Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="7a595-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="7a595-135">Os valores com suporte são ' canallocate ' e ' Delete '.</span><span class="sxs-lookup"><span data-stu-id="7a595-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="7a595-136">-Hostid</span><span class="sxs-lookup"><span data-stu-id="7a595-136">-HostId</span></span>
<span data-ttu-id="7a595-137">A ID do host</span><span class="sxs-lookup"><span data-stu-id="7a595-137">The Id of Host</span></span>

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

### <span data-ttu-id="7a595-138">-Identityid</span><span class="sxs-lookup"><span data-stu-id="7a595-138">-IdentityId</span></span>
<span data-ttu-id="7a595-139">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7a595-140">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="7a595-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7a595-141">-IdentityType</span></span>
<span data-ttu-id="7a595-142">A identidade da máquina virtual, se estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="7a595-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7a595-143">-LicenseType</span></span>
<span data-ttu-id="7a595-144">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foram licenciados no local.</span><span class="sxs-lookup"><span data-stu-id="7a595-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="7a595-145">Os possíveis valores para o Windows Server são:</span><span class="sxs-lookup"><span data-stu-id="7a595-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="7a595-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="7a595-146">Windows_Client</span></span>
- <span data-ttu-id="7a595-147">Windows_Server possíveis valores para o sistema operacional do servidor Linux são:</span><span class="sxs-lookup"><span data-stu-id="7a595-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="7a595-148">RHEL_BYOS (para RHEL)</span><span class="sxs-lookup"><span data-stu-id="7a595-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="7a595-149">SLES_BYOS (para SUSE)</span><span class="sxs-lookup"><span data-stu-id="7a595-149">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7a595-150">-MaxPrice</span></span>
<span data-ttu-id="7a595-151">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="7a595-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7a595-152">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="7a595-152">This price is in US Dollars.</span></span> <span data-ttu-id="7a595-153">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="7a595-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7a595-154">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="7a595-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7a595-155">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="7a595-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7a595-156">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="7a595-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7a595-157">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="7a595-157">Example: 0.01538.</span></span>  <span data-ttu-id="7a595-158">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="7a595-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7a595-159">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="7a595-159">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="7a595-160">-EncryptionAtHost</span></span>
<span data-ttu-id="7a595-161">A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a criptografia do host para a máquina virtual ou o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="7a595-162">Isso habilitará a criptografia para todos os discos, incluindo o disco de recursos/temporários no próprio host.</span><span class="sxs-lookup"><span data-stu-id="7a595-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="7a595-163">Padrão: a criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7a595-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="7a595-164">-Priority</span></span>
<span data-ttu-id="7a595-165">A prioridade da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="7a595-166">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="7a595-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="7a595-167">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="7a595-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="7a595-168">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="7a595-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="7a595-169">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="7a595-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="7a595-170">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="7a595-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="7a595-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7a595-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7a595-172">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="7a595-173">-Marcas</span><span class="sxs-lookup"><span data-stu-id="7a595-173">-Tags</span></span>
<span data-ttu-id="7a595-174">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="7a595-174">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="7a595-175">-VMName</span></span>
<span data-ttu-id="7a595-176">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-176">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="7a595-177">-VMSize</span></span>
<span data-ttu-id="7a595-178">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-178">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="7a595-179">-VmssId</span></span>
<span data-ttu-id="7a595-180">A ID do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7a595-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="7a595-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="7a595-181">-Zone</span></span>
<span data-ttu-id="7a595-182">Especifica a lista de zonas de disponibilidade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7a595-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="7a595-183">Os valores permitidos dependem das funcionalidades da região.</span><span class="sxs-lookup"><span data-stu-id="7a595-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="7a595-184">Os valores permitidos normalmente serão 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="7a595-184">Allowed values will normally be 1,2,3.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a595-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a595-185">CommonParameters</span></span>
<span data-ttu-id="7a595-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a595-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a595-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a595-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a595-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a595-188">INPUTS</span></span>

### <span data-ttu-id="7a595-189">System. String</span><span class="sxs-lookup"><span data-stu-id="7a595-189">System.String</span></span>

### <span data-ttu-id="7a595-190">System. String []</span><span class="sxs-lookup"><span data-stu-id="7a595-190">System.String[]</span></span>

### <span data-ttu-id="7a595-191">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a595-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7a595-192">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a595-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a595-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a595-193">OUTPUTS</span></span>

### <span data-ttu-id="7a595-194">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7a595-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7a595-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a595-195">NOTES</span></span>

## <span data-ttu-id="7a595-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a595-196">RELATED LINKS</span></span>

[<span data-ttu-id="7a595-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7a595-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="7a595-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7a595-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7a595-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7a595-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="7a595-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a595-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


