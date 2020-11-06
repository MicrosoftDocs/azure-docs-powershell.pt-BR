---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601306"
---
# <span data-ttu-id="5fee6-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5fee6-101">New-AzVMConfig</span></span>

## <span data-ttu-id="5fee6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fee6-102">SYNOPSIS</span></span>
<span data-ttu-id="5fee6-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="5fee6-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="5fee6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fee6-104">SYNTAX</span></span>

### <span data-ttu-id="5fee6-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fee6-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fee6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fee6-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fee6-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fee6-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fee6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fee6-108">DESCRIPTION</span></span>
<span data-ttu-id="5fee6-109">O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fee6-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="5fee6-110">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="5fee6-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="5fee6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fee6-111">EXAMPLES</span></span>

### <span data-ttu-id="5fee6-112">Exemplo 1: criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="5fee6-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="5fee6-113">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fee6-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5fee6-114">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5fee6-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5fee6-115">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5fee6-116">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fee6-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="5fee6-117">OS</span><span class="sxs-lookup"><span data-stu-id="5fee6-117">PARAMETERS</span></span>

### <span data-ttu-id="5fee6-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5fee6-118">-AssignIdentity</span></span>
<span data-ttu-id="5fee6-119">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="5fee6-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5fee6-120">-AvailabilitySetId</span></span>
<span data-ttu-id="5fee6-121">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5fee6-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="5fee6-122">Para obter um objeto do conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="5fee6-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="5fee6-123">O objeto de conjunto de disponibilidade contém uma propriedade de ID.</span><span class="sxs-lookup"><span data-stu-id="5fee6-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="5fee6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fee6-124">-DefaultProfile</span></span>
<span data-ttu-id="5fee6-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fee6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fee6-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5fee6-126">-EnableUltraSSD</span></span>
<span data-ttu-id="5fee6-127">Habilita um recurso para ter um ou mais discos de dados gerenciados com UltraSSD_LRS tipo de conta de armazenamento na VM.</span><span class="sxs-lookup"><span data-stu-id="5fee6-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="5fee6-128">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="5fee6-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="5fee6-129">-Identityid</span><span class="sxs-lookup"><span data-stu-id="5fee6-129">-IdentityId</span></span>
<span data-ttu-id="5fee6-130">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5fee6-131">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="5fee6-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5fee6-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5fee6-132">-IdentityType</span></span>
<span data-ttu-id="5fee6-133">A identidade da máquina virtual, se estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="5fee6-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="5fee6-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5fee6-134">-LicenseType</span></span>
<span data-ttu-id="5fee6-135">O tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="5fee6-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5fee6-136">-Marcas</span><span class="sxs-lookup"><span data-stu-id="5fee6-136">-Tags</span></span>
<span data-ttu-id="5fee6-137">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="5fee6-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="5fee6-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="5fee6-138">-VMName</span></span>
<span data-ttu-id="5fee6-139">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="5fee6-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5fee6-140">-VMSize</span></span>
<span data-ttu-id="5fee6-141">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="5fee6-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="5fee6-142">-Zone</span></span>
<span data-ttu-id="5fee6-143">Especifica a lista de zonas de disponibilidade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5fee6-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="5fee6-144">Os valores permitidos dependem das funcionalidades da região.</span><span class="sxs-lookup"><span data-stu-id="5fee6-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="5fee6-145">Os valores permitidos normalmente serão 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="5fee6-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="5fee6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fee6-146">CommonParameters</span></span>
<span data-ttu-id="5fee6-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fee6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fee6-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fee6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fee6-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fee6-149">INPUTS</span></span>

### <span data-ttu-id="5fee6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5fee6-150">System.String</span></span>

### <span data-ttu-id="5fee6-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="5fee6-151">System.String[]</span></span>

### <span data-ttu-id="5fee6-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5fee6-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5fee6-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5fee6-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fee6-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fee6-154">OUTPUTS</span></span>

### <span data-ttu-id="5fee6-155">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5fee6-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5fee6-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fee6-156">NOTES</span></span>

## <span data-ttu-id="5fee6-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fee6-157">RELATED LINKS</span></span>

[<span data-ttu-id="5fee6-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5fee6-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="5fee6-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5fee6-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="5fee6-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5fee6-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="5fee6-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5fee6-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


