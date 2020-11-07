---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777040"
---
# <span data-ttu-id="e48fa-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-101">Get-AzVM</span></span>

## <span data-ttu-id="e48fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e48fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e48fa-103">Obtém as propriedades de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e48fa-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="e48fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e48fa-104">SYNTAX</span></span>

### <span data-ttu-id="e48fa-105">ListAllVirtualMachinesParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e48fa-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e48fa-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e48fa-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e48fa-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e48fa-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e48fa-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="e48fa-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e48fa-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e48fa-109">DESCRIPTION</span></span>
<span data-ttu-id="e48fa-110">O cmdlet **Get-AzVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e48fa-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="e48fa-111">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e48fa-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="e48fa-112">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e48fa-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="e48fa-113">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e48fa-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="e48fa-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e48fa-114">EXAMPLES</span></span>

### <span data-ttu-id="e48fa-115">Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="e48fa-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e48fa-116">Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="e48fa-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="e48fa-117">Exemplo 2: obter propriedades do modo de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="e48fa-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="e48fa-118">Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="e48fa-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="e48fa-119">Esse comando especifica o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="e48fa-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="e48fa-120">Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="e48fa-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="e48fa-121">Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e48fa-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e48fa-122">Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e48fa-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="e48fa-123">Exemplo 4: obter todas as máquinas virtuais na sua assinatura</span><span class="sxs-lookup"><span data-stu-id="e48fa-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="e48fa-124">Este comando obtém todas as máquinas virtuais na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="e48fa-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="e48fa-125">OS</span><span class="sxs-lookup"><span data-stu-id="e48fa-125">PARAMETERS</span></span>

### <span data-ttu-id="e48fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48fa-126">-DefaultProfile</span></span>
<span data-ttu-id="e48fa-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e48fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e48fa-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="e48fa-128">-DisplayHint</span></span>
<span data-ttu-id="e48fa-129">Determina como o objeto de máquina virtual é exibido.</span><span class="sxs-lookup"><span data-stu-id="e48fa-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="e48fa-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e48fa-130">Valid values are:</span></span>

<span data-ttu-id="e48fa-131">--Compact: exibe apenas as propriedades de nível superior</span><span class="sxs-lookup"><span data-stu-id="e48fa-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="e48fa-132">--Expandir: exibe todas as propriedades em todos os níveis</span><span class="sxs-lookup"><span data-stu-id="e48fa-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48fa-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e48fa-133">-Name</span></span>
<span data-ttu-id="e48fa-134">Especifica o nome da máquina virtual a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e48fa-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48fa-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="e48fa-135">-NextLink</span></span>
<span data-ttu-id="e48fa-136">Especifica o próximo link.</span><span class="sxs-lookup"><span data-stu-id="e48fa-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48fa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48fa-137">-ResourceGroupName</span></span>
<span data-ttu-id="e48fa-138">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e48fa-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48fa-139">-Status</span><span class="sxs-lookup"><span data-stu-id="e48fa-139">-Status</span></span>
<span data-ttu-id="e48fa-140">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e48fa-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48fa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48fa-141">CommonParameters</span></span>
<span data-ttu-id="e48fa-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e48fa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48fa-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48fa-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48fa-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e48fa-144">INPUTS</span></span>

### <span data-ttu-id="e48fa-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e48fa-145">None</span></span>
<span data-ttu-id="e48fa-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e48fa-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e48fa-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e48fa-147">OUTPUTS</span></span>

### <span data-ttu-id="e48fa-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e48fa-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e48fa-149">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="e48fa-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="e48fa-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e48fa-150">NOTES</span></span>

## <span data-ttu-id="e48fa-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e48fa-151">RELATED LINKS</span></span>

[<span data-ttu-id="e48fa-152">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e48fa-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e48fa-154">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="e48fa-155">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e48fa-156">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e48fa-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e48fa-157">Update-AzVM</span></span>](./Update-AzVM.md)


