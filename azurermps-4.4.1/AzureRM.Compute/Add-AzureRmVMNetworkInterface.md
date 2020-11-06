---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 528b03171f1d1ccbc5820ef0a69197e8240cd038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427000"
---
# <span data-ttu-id="8033d-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8033d-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="8033d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8033d-102">SYNOPSIS</span></span>
<span data-ttu-id="8033d-103">Adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8033d-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8033d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8033d-104">SYNTAX</span></span>

### <span data-ttu-id="8033d-105">GetNicFromNicId (padrão)</span><span class="sxs-lookup"><span data-stu-id="8033d-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8033d-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="8033d-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8033d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8033d-107">DESCRIPTION</span></span>
<span data-ttu-id="8033d-108">O cmdlet **Add-AzureRmVMNetworkInterface** adiciona uma interface de rede a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8033d-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="8033d-109">Você pode adicionar uma interface quando criar uma máquina virtual ou adicionar uma a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="8033d-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="8033d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8033d-110">EXAMPLES</span></span>

### <span data-ttu-id="8033d-111">Exemplo 1: adicionar uma interface de rede a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8033d-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="8033d-112">O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8033d-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8033d-113">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8033d-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="8033d-114">O segundo comando adiciona uma interface de rede à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8033d-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="8033d-115">Exemplo 2: adicionar uma interface de rede a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="8033d-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -VM $VirtualMachine
```

<span data-ttu-id="8033d-116">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="8033d-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="8033d-117">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8033d-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8033d-118">O segundo comando adiciona uma interface de rede à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8033d-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="8033d-119">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8033d-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="8033d-120">OS</span><span class="sxs-lookup"><span data-stu-id="8033d-120">PARAMETERS</span></span>

### <span data-ttu-id="8033d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8033d-121">-DefaultProfile</span></span>
<span data-ttu-id="8033d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8033d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8033d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="8033d-123">-Id</span></span>
<span data-ttu-id="8033d-124">Especifica a ID de uma interface de rede a ser adicionada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8033d-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="8033d-125">Você pode usar o cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) para obter uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8033d-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8033d-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8033d-126">-NetworkInterface</span></span>
<span data-ttu-id="8033d-127">Especifica a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8033d-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="8033d-128">-Principal</span><span class="sxs-lookup"><span data-stu-id="8033d-128">-Primary</span></span>
<span data-ttu-id="8033d-129">Indica que esse cmdlet adiciona a interface de rede como a interface principal.</span><span class="sxs-lookup"><span data-stu-id="8033d-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8033d-130">-VM</span><span class="sxs-lookup"><span data-stu-id="8033d-130">-VM</span></span>
<span data-ttu-id="8033d-131">Especifica um objeto de máquina virtual local ao qual adicionar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8033d-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="8033d-132">Para criar uma máquina virtual, use o cmdlet **New-AzureRmVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="8033d-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="8033d-133">Para obter uma máquina virtual existente, use o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="8033d-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8033d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8033d-134">CommonParameters</span></span>
<span data-ttu-id="8033d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8033d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8033d-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8033d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8033d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8033d-137">INPUTS</span></span>

### <span data-ttu-id="8033d-138">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="8033d-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="8033d-139">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="8033d-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="8033d-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8033d-140">PSVirtualMachine</span></span>
<span data-ttu-id="8033d-141">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8033d-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8033d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8033d-142">OUTPUTS</span></span>

### <span data-ttu-id="8033d-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8033d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8033d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8033d-144">NOTES</span></span>

## <span data-ttu-id="8033d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8033d-145">RELATED LINKS</span></span>

[<span data-ttu-id="8033d-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="8033d-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="8033d-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8033d-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8033d-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8033d-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
