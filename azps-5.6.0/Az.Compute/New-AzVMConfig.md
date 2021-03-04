---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890450"
---
# <span data-ttu-id="d8705-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d8705-101">New-AzVMConfig</span></span>

## <span data-ttu-id="d8705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8705-102">SYNOPSIS</span></span>
<span data-ttu-id="d8705-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="d8705-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="d8705-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8705-104">SYNTAX</span></span>

### <span data-ttu-id="d8705-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8705-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8705-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8705-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8705-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8705-107">DESCRIPTION</span></span>
<span data-ttu-id="d8705-108">O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8705-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="d8705-109">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="d8705-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="d8705-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8705-110">EXAMPLES</span></span>

### <span data-ttu-id="d8705-111">Exemplo 1: Criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d8705-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="d8705-112">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d8705-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="d8705-113">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d8705-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d8705-114">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d8705-115">A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d8705-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="d8705-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8705-116">PARAMETERS</span></span>

### <span data-ttu-id="d8705-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="d8705-117">-AvailabilitySetId</span></span>
<span data-ttu-id="d8705-118">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d8705-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="d8705-119">Para obter um objeto de conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d8705-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="d8705-120">O objeto de conjunto de disponibilidade contém uma propriedade ID.</span><span class="sxs-lookup"><span data-stu-id="d8705-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="d8705-121">As máquinas virtuais especificadas no mesmo conjunto de disponibilidade são alocadas para nós diferentes para maximizar a disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d8705-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="d8705-122">Para obter mais informações sobre conjuntos de disponibilidade, consulte [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="d8705-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="d8705-123">Para obter mais informações sobre a manutenção planejada do Azure, consulte [Manutenção planejada para máquinas virtuais no Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="d8705-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="d8705-124">Atualmente, uma VM só pode ser adicionada ao conjunto de disponibilidade no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="d8705-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="d8705-125">O conjunto de disponibilidade ao qual a VM está sendo adicionada deve estar no mesmo grupo de recursos que o recurso de conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d8705-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="d8705-126">Uma VM existente não pode ser adicionada a um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d8705-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="d8705-127">Essa propriedade não pode existir juntamente com uma referência properties não nulo.virtualMachineScaleSet.</span><span class="sxs-lookup"><span data-stu-id="d8705-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="d8705-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8705-128">-DefaultProfile</span></span>
<span data-ttu-id="d8705-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d8705-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8705-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="d8705-130">-EnableUltraSSD</span></span>
<span data-ttu-id="d8705-131">Permite que um recurso tenha um ou mais discos de dados gerenciados com UltraSSD_LRS tipo de conta de armazenamento na VM.</span><span class="sxs-lookup"><span data-stu-id="d8705-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="d8705-132">Discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d8705-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="d8705-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8705-133">-EvictionPolicy</span></span>
<span data-ttu-id="d8705-134">A política de despejo da máquina virtual do Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="d8705-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="d8705-135">Os valores com suporte são 'Deallocate' e 'Delete'.</span><span class="sxs-lookup"><span data-stu-id="d8705-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="d8705-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="d8705-136">-HostId</span></span>
<span data-ttu-id="d8705-137">A ID do Host</span><span class="sxs-lookup"><span data-stu-id="d8705-137">The Id of Host</span></span>

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

### <span data-ttu-id="d8705-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="d8705-138">-IdentityId</span></span>
<span data-ttu-id="d8705-139">Especifica a lista de identidades de usuário associadas ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="d8705-140">As referências de identidade do usuário serão ARM ids de recurso no formato: '/subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identity/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="d8705-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="d8705-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d8705-141">-IdentityType</span></span>
<span data-ttu-id="d8705-142">A identidade da máquina virtual, se configurada.</span><span class="sxs-lookup"><span data-stu-id="d8705-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="d8705-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d8705-143">-LicenseType</span></span>
<span data-ttu-id="d8705-144">Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foi licenciada no local.</span><span class="sxs-lookup"><span data-stu-id="d8705-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="d8705-145">Os valores possíveis para o Windows Server são:</span><span class="sxs-lookup"><span data-stu-id="d8705-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="d8705-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="d8705-146">Windows_Client</span></span>
- <span data-ttu-id="d8705-147">Windows_Server valores possíveis para o sistema operacional Linux Server são:</span><span class="sxs-lookup"><span data-stu-id="d8705-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="d8705-148">RHEL_BYOS (para RHEL)</span><span class="sxs-lookup"><span data-stu-id="d8705-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="d8705-149">SLES_BYOS (para SUSE)</span><span class="sxs-lookup"><span data-stu-id="d8705-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="d8705-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="d8705-150">-MaxPrice</span></span>
<span data-ttu-id="d8705-151">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="d8705-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="d8705-152">Esse preço está em dólares dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d8705-152">This price is in US Dollars.</span></span> <span data-ttu-id="d8705-153">Esse preço será comparado com o preço atual de baixa prioridade para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="d8705-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="d8705-154">Além disso, os preços são comparados no momento da criação/atualização da VM/VMSS de baixa prioridade e a operação só terá êxito se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="d8705-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="d8705-155">O maxPrice também será usado para despejar uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade for além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="d8705-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="d8705-156">Os valores possíveis são: qualquer valor decimal maior que zero.</span><span class="sxs-lookup"><span data-stu-id="d8705-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="d8705-157">Exemplo: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="d8705-157">Example: 0.01538.</span></span>  <span data-ttu-id="d8705-158">-1 indica que a VM/VMSS de baixa prioridade não deve ser despejada por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="d8705-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="d8705-159">Além disso, o preço máximo padrão será -1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="d8705-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="d8705-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="d8705-160">-EncryptionAtHost</span></span>
<span data-ttu-id="d8705-161">A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a Criptografia de Host para o conjunto de escala de máquina virtual ou máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="d8705-162">Isso habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="d8705-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="d8705-163">Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8705-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="d8705-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="d8705-164">-Priority</span></span>
<span data-ttu-id="d8705-165">A prioridade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="d8705-166">Somente os valores com suporte são 'Regular', 'Spot' e 'Low'.</span><span class="sxs-lookup"><span data-stu-id="d8705-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="d8705-167">'Regular' é para máquina virtual regular.</span><span class="sxs-lookup"><span data-stu-id="d8705-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="d8705-168">'Spot' é para máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="d8705-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="d8705-169">'Baixo' também é para máquina virtual local, mas é substituído por 'Spot'.</span><span class="sxs-lookup"><span data-stu-id="d8705-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="d8705-170">Use 'Spot' em vez de 'Low'.</span><span class="sxs-lookup"><span data-stu-id="d8705-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="d8705-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d8705-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="d8705-172">A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="d8705-173">-Tags</span><span class="sxs-lookup"><span data-stu-id="d8705-173">-Tags</span></span>
<span data-ttu-id="d8705-174">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="d8705-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="d8705-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8705-175">-VMName</span></span>
<span data-ttu-id="d8705-176">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="d8705-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="d8705-177">-VMSize</span></span>
<span data-ttu-id="d8705-178">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="d8705-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="d8705-179">-VmssId</span></span>
<span data-ttu-id="d8705-180">A ID do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d8705-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="d8705-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="d8705-181">-Zone</span></span>
<span data-ttu-id="d8705-182">Especifica a lista de zonas de disponibilidade da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8705-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="d8705-183">Os valores permitidos dependem dos recursos da região.</span><span class="sxs-lookup"><span data-stu-id="d8705-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="d8705-184">Os valores permitidos normalmente serão 1,2,3.</span><span class="sxs-lookup"><span data-stu-id="d8705-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="d8705-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8705-185">CommonParameters</span></span>
<span data-ttu-id="d8705-186">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8705-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8705-187">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8705-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8705-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8705-188">INPUTS</span></span>

### <span data-ttu-id="d8705-189">System.String</span><span class="sxs-lookup"><span data-stu-id="d8705-189">System.String</span></span>

### <span data-ttu-id="d8705-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d8705-190">System.String[]</span></span>

### <span data-ttu-id="d8705-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8705-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d8705-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d8705-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d8705-193">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8705-193">OUTPUTS</span></span>

### <span data-ttu-id="d8705-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d8705-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d8705-195">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8705-195">NOTES</span></span>

## <span data-ttu-id="d8705-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8705-196">RELATED LINKS</span></span>

[<span data-ttu-id="d8705-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d8705-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="d8705-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d8705-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d8705-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d8705-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="d8705-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8705-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


