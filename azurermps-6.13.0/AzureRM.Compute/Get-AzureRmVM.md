---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428555"
---
# <span data-ttu-id="b9e8f-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="b9e8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e8f-103">Obtém as propriedades de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9e8f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e8f-105">ListAllVirtualMachinesParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9e8f-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9e8f-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b9e8f-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e8f-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b9e8f-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9e8f-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="b9e8f-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9e8f-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="b9e8f-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9e8f-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9e8f-110">DESCRIPTION</span></span>
<span data-ttu-id="b9e8f-111">O cmdlet **Get-AzureRmVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="b9e8f-112">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="b9e8f-113">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="b9e8f-114">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="b9e8f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e8f-115">EXAMPLES</span></span>

### <span data-ttu-id="b9e8f-116">Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="b9e8f-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b9e8f-117">Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b9e8f-118">Exemplo 2: obter propriedades do modo de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="b9e8f-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="b9e8f-119">Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="b9e8f-120">Esse comando especifica o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="b9e8f-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="b9e8f-121">Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="b9e8f-122">Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b9e8f-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b9e8f-123">Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b9e8f-124">Exemplo 4: obter todas as máquinas virtuais na sua assinatura</span><span class="sxs-lookup"><span data-stu-id="b9e8f-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="b9e8f-125">Este comando obtém todas as máquinas virtuais na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="b9e8f-126">Exemplo 5: obter todas as máquinas virtuais no local.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="b9e8f-127">Esse comando obtém todas as máquinas virtuais na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="b9e8f-128">OS</span><span class="sxs-lookup"><span data-stu-id="b9e8f-128">PARAMETERS</span></span>

### <span data-ttu-id="b9e8f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e8f-129">-DefaultProfile</span></span>
<span data-ttu-id="b9e8f-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="b9e8f-131">-DisplayHint</span></span>
<span data-ttu-id="b9e8f-132">Determina como o objeto de máquina virtual é exibido.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="b9e8f-133">Os valores válidos são:--Compact: exibe apenas as propriedades de nível superior--expande: exibe todas as propriedades em todos os níveis</span><span class="sxs-lookup"><span data-stu-id="b9e8f-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-134">-Local</span><span class="sxs-lookup"><span data-stu-id="b9e8f-134">-Location</span></span>
<span data-ttu-id="b9e8f-135">Especifica um local para as máquinas virtuais a serem listadas.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e8f-136">-Name</span></span>
<span data-ttu-id="b9e8f-137">Especifica o nome da máquina virtual a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="b9e8f-138">-NextLink</span></span>
<span data-ttu-id="b9e8f-139">Especifica o próximo link.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e8f-140">-ResourceGroupName</span></span>
<span data-ttu-id="b9e8f-141">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-142">-Status</span><span class="sxs-lookup"><span data-stu-id="b9e8f-142">-Status</span></span>
<span data-ttu-id="b9e8f-143">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e8f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e8f-144">CommonParameters</span></span>
<span data-ttu-id="b9e8f-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e8f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e8f-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e8f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e8f-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9e8f-147">INPUTS</span></span>

### <span data-ttu-id="b9e8f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b9e8f-148">System.String</span></span>

### <span data-ttu-id="b9e8f-149">System. URI</span><span class="sxs-lookup"><span data-stu-id="b9e8f-149">System.Uri</span></span>

### <span data-ttu-id="b9e8f-150">Microsoft. Azure. Commands. COMPUTE. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="b9e8f-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="b9e8f-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9e8f-151">OUTPUTS</span></span>

### <span data-ttu-id="b9e8f-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b9e8f-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b9e8f-153">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="b9e8f-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="b9e8f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9e8f-154">NOTES</span></span>

## <span data-ttu-id="b9e8f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e8f-155">RELATED LINKS</span></span>

[<span data-ttu-id="b9e8f-156">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b9e8f-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b9e8f-158">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b9e8f-159">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b9e8f-160">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b9e8f-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9e8f-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


