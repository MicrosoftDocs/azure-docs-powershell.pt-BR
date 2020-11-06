---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3ac2a0ba40b7bcd6b845bd069fced292e959cba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597518"
---
# <span data-ttu-id="004aa-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="004aa-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="004aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="004aa-102">SYNOPSIS</span></span>
<span data-ttu-id="004aa-103">Adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="004aa-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="004aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="004aa-104">SYNTAX</span></span>

### <span data-ttu-id="004aa-105">GetNicFromNicId (padrão)</span><span class="sxs-lookup"><span data-stu-id="004aa-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="004aa-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="004aa-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="004aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="004aa-107">DESCRIPTION</span></span>
<span data-ttu-id="004aa-108">O cmdlet **Add-AzVMNetworkInterface** adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="004aa-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="004aa-109">Você pode adicionar uma interface quando criar uma máquina virtual ou adicionar uma a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="004aa-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="004aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="004aa-110">EXAMPLES</span></span>

### <span data-ttu-id="004aa-111">Exemplo 1: adicionar uma interface de rede a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="004aa-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="004aa-112">O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="004aa-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="004aa-113">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="004aa-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="004aa-114">O segundo comando adiciona uma interface de rede à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="004aa-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="004aa-115">Exemplo 2: adicionar uma interface de rede a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="004aa-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="004aa-116">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="004aa-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="004aa-117">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="004aa-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="004aa-118">O segundo comando adiciona uma interface de rede à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="004aa-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="004aa-119">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="004aa-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="004aa-120">OS</span><span class="sxs-lookup"><span data-stu-id="004aa-120">PARAMETERS</span></span>

### <span data-ttu-id="004aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004aa-121">-DefaultProfile</span></span>
<span data-ttu-id="004aa-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="004aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="004aa-123">-ID</span><span class="sxs-lookup"><span data-stu-id="004aa-123">-Id</span></span>
<span data-ttu-id="004aa-124">Especifica a ID de uma interface de rede a ser adicionada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="004aa-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="004aa-125">Você pode usar o cmdlet [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) para obter uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="004aa-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004aa-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="004aa-126">-NetworkInterface</span></span>
<span data-ttu-id="004aa-127">Especifica a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="004aa-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="004aa-128">-Principal</span><span class="sxs-lookup"><span data-stu-id="004aa-128">-Primary</span></span>
<span data-ttu-id="004aa-129">Indica que esse cmdlet adiciona a interface de rede como a interface principal.</span><span class="sxs-lookup"><span data-stu-id="004aa-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004aa-130">-VM</span><span class="sxs-lookup"><span data-stu-id="004aa-130">-VM</span></span>
<span data-ttu-id="004aa-131">Especifica um objeto de máquina virtual local ao qual adicionar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="004aa-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="004aa-132">Para criar uma máquina virtual, use o cmdlet **New-AzVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="004aa-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="004aa-133">Para obter uma máquina virtual existente, use o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="004aa-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="004aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004aa-134">CommonParameters</span></span>
<span data-ttu-id="004aa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004aa-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="004aa-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004aa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="004aa-137">INPUTS</span></span>

### <span data-ttu-id="004aa-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="004aa-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="004aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="004aa-139">System.String</span></span>

### <span data-ttu-id="004aa-140">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="004aa-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="004aa-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="004aa-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="004aa-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="004aa-142">OUTPUTS</span></span>

### <span data-ttu-id="004aa-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="004aa-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="004aa-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="004aa-144">NOTES</span></span>

## <span data-ttu-id="004aa-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="004aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="004aa-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="004aa-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="004aa-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="004aa-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="004aa-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="004aa-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
