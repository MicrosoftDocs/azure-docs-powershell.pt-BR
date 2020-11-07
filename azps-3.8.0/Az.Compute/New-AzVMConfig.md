---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941444"
---
# <span data-ttu-id="93345-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="93345-101">New-AzVMConfig</span></span>

## <span data-ttu-id="93345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93345-102">SYNOPSIS</span></span>
<span data-ttu-id="93345-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="93345-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="93345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93345-104">SYNTAX</span></span>

### <span data-ttu-id="93345-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="93345-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93345-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="93345-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93345-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="93345-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93345-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93345-108">DESCRIPTION</span></span>
<span data-ttu-id="93345-109">O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="93345-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="93345-110">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="93345-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="93345-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93345-111">EXAMPLES</span></span>

### <span data-ttu-id="93345-112">Exemplo 1: criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="93345-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="93345-113">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="93345-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="93345-114">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="93345-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="93345-115">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="93345-116">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="93345-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="93345-117">OS</span><span class="sxs-lookup"><span data-stu-id="93345-117">PARAMETERS</span></span>

### <span data-ttu-id="93345-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="93345-118">-AssignIdentity</span></span>
<span data-ttu-id="93345-119">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93345-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="93345-120">-AvailabilitySetId</span></span>
<span data-ttu-id="93345-121">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="93345-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="93345-122">Para obter um objeto do conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="93345-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="93345-123">O objeto de conjunto de disponibilidade contém uma propriedade de ID.</span><span class="sxs-lookup"><span data-stu-id="93345-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="93345-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93345-124">-DefaultProfile</span></span>
<span data-ttu-id="93345-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93345-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93345-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="93345-126">-EnableUltraSSD</span></span>
<span data-ttu-id="93345-127">Habilita um recurso para ter um ou mais discos de dados gerenciados com UltraSSD_LRS tipo de conta de armazenamento na VM.</span><span class="sxs-lookup"><span data-stu-id="93345-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="93345-128">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="93345-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="93345-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="93345-129">-EvictionPolicy</span></span>
<span data-ttu-id="93345-130">A política de remoção para a máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="93345-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="93345-131">Somente o valor com suporte é ' desallocate '.</span><span class="sxs-lookup"><span data-stu-id="93345-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="93345-132">-Hostid</span><span class="sxs-lookup"><span data-stu-id="93345-132">-HostId</span></span>
<span data-ttu-id="93345-133">A ID do host</span><span class="sxs-lookup"><span data-stu-id="93345-133">The Id of Host</span></span>

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

### <span data-ttu-id="93345-134">-Identityid</span><span class="sxs-lookup"><span data-stu-id="93345-134">-IdentityId</span></span>
<span data-ttu-id="93345-135">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="93345-136">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="93345-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="93345-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="93345-137">-IdentityType</span></span>
<span data-ttu-id="93345-138">A identidade da máquina virtual, se estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="93345-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="93345-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="93345-139">-LicenseType</span></span>
<span data-ttu-id="93345-140">O tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="93345-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="93345-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="93345-141">-MaxPrice</span></span>
<span data-ttu-id="93345-142">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="93345-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="93345-143">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="93345-143">This price is in US Dollars.</span></span> <span data-ttu-id="93345-144">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="93345-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="93345-145">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="93345-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="93345-146">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="93345-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="93345-147">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="93345-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="93345-148">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="93345-148">Example: 0.01538.</span></span>  <span data-ttu-id="93345-149">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="93345-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="93345-150">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="93345-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="93345-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="93345-151">-Priority</span></span>
<span data-ttu-id="93345-152">A prioridade da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="93345-153">Somente os valores com suporte são ' regular ', ' spot ' e ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="93345-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="93345-154">' Regular ' é para a máquina virtual normal.</span><span class="sxs-lookup"><span data-stu-id="93345-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="93345-155">' Spot ' é para máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="93345-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="93345-156">' Low ' também é para máquina virtual Spot, mas é substituído por ' spot '.</span><span class="sxs-lookup"><span data-stu-id="93345-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="93345-157">Use ' spot ' em vez de ' baixo '.</span><span class="sxs-lookup"><span data-stu-id="93345-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="93345-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="93345-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="93345-159">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="93345-160">-Marcas</span><span class="sxs-lookup"><span data-stu-id="93345-160">-Tags</span></span>
<span data-ttu-id="93345-161">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="93345-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="93345-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="93345-162">-VMName</span></span>
<span data-ttu-id="93345-163">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="93345-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="93345-164">-VMSize</span></span>
<span data-ttu-id="93345-165">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="93345-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="93345-166">-VmssId</span></span>
<span data-ttu-id="93345-167">A ID do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="93345-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="93345-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="93345-168">-Zone</span></span>
<span data-ttu-id="93345-169">Especifica a lista de zonas de disponibilidade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93345-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="93345-170">Os valores permitidos dependem das funcionalidades da região.</span><span class="sxs-lookup"><span data-stu-id="93345-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="93345-171">Os valores permitidos normalmente serão 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="93345-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="93345-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93345-172">CommonParameters</span></span>
<span data-ttu-id="93345-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93345-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93345-174">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93345-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93345-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93345-175">INPUTS</span></span>

### <span data-ttu-id="93345-176">System. String</span><span class="sxs-lookup"><span data-stu-id="93345-176">System.String</span></span>

### <span data-ttu-id="93345-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="93345-177">System.String[]</span></span>

### <span data-ttu-id="93345-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="93345-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="93345-179">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93345-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93345-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93345-180">OUTPUTS</span></span>

### <span data-ttu-id="93345-181">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="93345-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="93345-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93345-182">NOTES</span></span>

## <span data-ttu-id="93345-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93345-183">RELATED LINKS</span></span>

[<span data-ttu-id="93345-184">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="93345-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="93345-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="93345-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="93345-186">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="93345-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="93345-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="93345-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


