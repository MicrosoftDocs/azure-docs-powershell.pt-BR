---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776958"
---
# <span data-ttu-id="04311-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="04311-101">New-AzVMConfig</span></span>

## <span data-ttu-id="04311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04311-102">SYNOPSIS</span></span>
<span data-ttu-id="04311-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="04311-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="04311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04311-104">SYNTAX</span></span>

### <span data-ttu-id="04311-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="04311-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04311-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="04311-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04311-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="04311-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04311-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04311-108">DESCRIPTION</span></span>
<span data-ttu-id="04311-109">O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="04311-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="04311-110">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="04311-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="04311-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04311-111">EXAMPLES</span></span>

### <span data-ttu-id="04311-112">Exemplo 1: criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="04311-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="04311-113">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="04311-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="04311-114">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="04311-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="04311-115">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="04311-116">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="04311-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="04311-117">OS</span><span class="sxs-lookup"><span data-stu-id="04311-117">PARAMETERS</span></span>

### <span data-ttu-id="04311-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="04311-118">-AssignIdentity</span></span>
<span data-ttu-id="04311-119">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04311-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="04311-120">-AvailabilitySetId</span></span>
<span data-ttu-id="04311-121">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="04311-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="04311-122">Para obter um objeto do conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="04311-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="04311-123">O objeto de conjunto de disponibilidade contém uma propriedade de ID.</span><span class="sxs-lookup"><span data-stu-id="04311-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04311-124">-DefaultProfile</span></span>
<span data-ttu-id="04311-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04311-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04311-126">-Identityid</span><span class="sxs-lookup"><span data-stu-id="04311-126">-IdentityId</span></span>
<span data-ttu-id="04311-127">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="04311-128">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="04311-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="04311-129">-IdentityType</span></span>
<span data-ttu-id="04311-130">A identidade da máquina virtual, se estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="04311-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04311-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="04311-131">-LicenseType</span></span>
<span data-ttu-id="04311-132">O tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="04311-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04311-133">-Marcas</span><span class="sxs-lookup"><span data-stu-id="04311-133">-Tags</span></span>
<span data-ttu-id="04311-134">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="04311-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="04311-135">-VMName</span></span>
<span data-ttu-id="04311-136">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="04311-137">-VMSize</span></span>
<span data-ttu-id="04311-138">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="04311-139">-Zone</span></span>
<span data-ttu-id="04311-140">Especifica a lista de zonas para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="04311-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04311-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04311-141">CommonParameters</span></span>
<span data-ttu-id="04311-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04311-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04311-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04311-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04311-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04311-144">INPUTS</span></span>

### <span data-ttu-id="04311-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04311-145">None</span></span>
<span data-ttu-id="04311-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="04311-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04311-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04311-147">OUTPUTS</span></span>

### <span data-ttu-id="04311-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="04311-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="04311-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04311-149">NOTES</span></span>

## <span data-ttu-id="04311-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04311-150">RELATED LINKS</span></span>

[<span data-ttu-id="04311-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="04311-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="04311-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="04311-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="04311-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="04311-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="04311-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="04311-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


