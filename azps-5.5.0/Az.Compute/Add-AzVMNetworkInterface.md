---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116558"
---
# <span data-ttu-id="c2c70-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2c70-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="c2c70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2c70-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c70-103">Adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c2c70-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="c2c70-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2c70-104">SYNTAX</span></span>

### <span data-ttu-id="c2c70-105">GetNicFromNicId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c2c70-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2c70-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="c2c70-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c70-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2c70-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c70-108">O **cmdlet Add-AzVMNetworkInterface** adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c2c70-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="c2c70-109">Você pode adicionar uma interface ao criar uma máquina virtual ou adicioná-la a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="c2c70-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="c2c70-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2c70-110">EXAMPLES</span></span>

### <span data-ttu-id="c2c70-111">Exemplo 1: Adicionar uma interface de rede a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c2c70-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="c2c70-112">O primeiro comando cria um objeto virtual de máquina e, em seguida, o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="c2c70-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c2c70-113">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c2c70-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c2c70-114">O segundo comando adiciona uma interface de rede à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c2c70-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="c2c70-115">Exemplo 2: Adicionar uma interface de rede a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="c2c70-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c2c70-116">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="c2c70-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="c2c70-117">O comando armazena a máquina virtual na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="c2c70-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c2c70-118">O segundo comando adiciona uma interface de rede à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c2c70-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c2c70-119">O comando final atualiza o estado da máquina virtual armazenada $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c2c70-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="c2c70-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2c70-120">PARAMETERS</span></span>

### <span data-ttu-id="c2c70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c70-121">-DefaultProfile</span></span>
<span data-ttu-id="c2c70-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c2c70-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c70-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c2c70-123">-Id</span></span>
<span data-ttu-id="c2c70-124">Especifica a ID de uma interface de rede para adicionar a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c2c70-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="c2c70-125">Você pode usar o cmdlet [Get-AzNetworkInterface para](/powershell/module/az.network/get-aznetworkinterface) obter uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c2c70-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="c2c70-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c2c70-126">-NetworkInterface</span></span>
<span data-ttu-id="c2c70-127">Especifica a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c2c70-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="c2c70-128">-Principal</span><span class="sxs-lookup"><span data-stu-id="c2c70-128">-Primary</span></span>
<span data-ttu-id="c2c70-129">Indica que esse cmdlet adiciona a interface de rede como a interface principal.</span><span class="sxs-lookup"><span data-stu-id="c2c70-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="c2c70-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c2c70-130">-VM</span></span>
<span data-ttu-id="c2c70-131">Especifica um objeto de máquina virtual local ao qual adicionar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c2c70-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="c2c70-132">Para criar uma máquina virtual, use o cmdlet **New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="c2c70-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="c2c70-133">Para obter uma máquina virtual existente, use **o cmdlet Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="c2c70-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="c2c70-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c70-134">CommonParameters</span></span>
<span data-ttu-id="c2c70-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c70-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c70-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2c70-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c70-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2c70-137">INPUTS</span></span>

### <span data-ttu-id="c2c70-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c2c70-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c2c70-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c2c70-139">System.String</span></span>

### <span data-ttu-id="c2c70-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c2c70-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c2c70-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2c70-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2c70-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="c2c70-142">OUTPUTS</span></span>

### <span data-ttu-id="c2c70-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c2c70-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c2c70-144">Notas</span><span class="sxs-lookup"><span data-stu-id="c2c70-144">NOTES</span></span>

## <span data-ttu-id="c2c70-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2c70-145">RELATED LINKS</span></span>

[<span data-ttu-id="c2c70-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c2c70-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="c2c70-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c2c70-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c2c70-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c2c70-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
