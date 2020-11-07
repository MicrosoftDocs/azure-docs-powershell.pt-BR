---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 832a7c81c9c7e8ffa5a5a6123162746d039ca71d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785557"
---
# <span data-ttu-id="3a428-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="3a428-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a428-102">SYNOPSIS</span></span>
<span data-ttu-id="3a428-103">Obtém as propriedades de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a428-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a428-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a428-104">SYNTAX</span></span>

### <span data-ttu-id="3a428-105">ListAllVirtualMachinesParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a428-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a428-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="3a428-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a428-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="3a428-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a428-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="3a428-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a428-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a428-109">DESCRIPTION</span></span>
<span data-ttu-id="3a428-110">O cmdlet **Get-AzureRmVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a428-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="3a428-111">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a428-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="3a428-112">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a428-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="3a428-113">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a428-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="3a428-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a428-114">EXAMPLES</span></span>

### <span data-ttu-id="3a428-115">Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="3a428-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3a428-116">Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3a428-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="3a428-117">Exemplo 2: obter propriedades do modo de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="3a428-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="3a428-118">Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3a428-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="3a428-119">Esse comando especifica o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="3a428-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="3a428-120">Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="3a428-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="3a428-121">Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3a428-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3a428-122">Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3a428-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="3a428-123">Exemplo 4: obter todas as máquinas virtuais na sua assinatura</span><span class="sxs-lookup"><span data-stu-id="3a428-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="3a428-124">Este comando obtém todas as máquinas virtuais na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a428-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="3a428-125">OS</span><span class="sxs-lookup"><span data-stu-id="3a428-125">PARAMETERS</span></span>

### <span data-ttu-id="3a428-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a428-126">-DefaultProfile</span></span>
<span data-ttu-id="3a428-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a428-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a428-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="3a428-128">-DisplayHint</span></span>
<span data-ttu-id="3a428-129">Determina como o objeto de máquina virtual é exibido.</span><span class="sxs-lookup"><span data-stu-id="3a428-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="3a428-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3a428-130">Valid values are:</span></span>

<span data-ttu-id="3a428-131">--Compact: exibe apenas as propriedades de nível superior</span><span class="sxs-lookup"><span data-stu-id="3a428-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="3a428-132">--Expandir: exibe todas as propriedades em todos os níveis</span><span class="sxs-lookup"><span data-stu-id="3a428-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="3a428-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a428-133">-Name</span></span>
<span data-ttu-id="3a428-134">Especifica o nome da máquina virtual a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="3a428-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="3a428-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="3a428-135">-NextLink</span></span>
<span data-ttu-id="3a428-136">Especifica o próximo link.</span><span class="sxs-lookup"><span data-stu-id="3a428-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="3a428-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a428-137">-ResourceGroupName</span></span>
<span data-ttu-id="3a428-138">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a428-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a428-139">-Status</span><span class="sxs-lookup"><span data-stu-id="3a428-139">-Status</span></span>
<span data-ttu-id="3a428-140">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a428-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="3a428-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a428-141">CommonParameters</span></span>
<span data-ttu-id="3a428-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a428-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a428-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a428-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a428-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a428-144">INPUTS</span></span>

### <span data-ttu-id="3a428-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3a428-145">None</span></span>
<span data-ttu-id="3a428-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3a428-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a428-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a428-147">OUTPUTS</span></span>

### <span data-ttu-id="3a428-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3a428-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3a428-149">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="3a428-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="3a428-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a428-150">NOTES</span></span>

## <span data-ttu-id="3a428-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a428-151">RELATED LINKS</span></span>

[<span data-ttu-id="3a428-152">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="3a428-153">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="3a428-154">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="3a428-155">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="3a428-156">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="3a428-157">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a428-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


