---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602279"
---
# <span data-ttu-id="8ddb8-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="8ddb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ddb8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddb8-103">Obtém as propriedades de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ddb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ddb8-104">SYNTAX</span></span>

### <span data-ttu-id="8ddb8-105">ListAllVirtualMachinesParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ddb8-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ddb8-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="8ddb8-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ddb8-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="8ddb8-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ddb8-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="8ddb8-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ddb8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ddb8-109">DESCRIPTION</span></span>
<span data-ttu-id="8ddb8-110">O cmdlet **Get-AzureRmVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="8ddb8-111">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="8ddb8-112">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="8ddb8-113">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="8ddb8-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ddb8-114">EXAMPLES</span></span>

### <span data-ttu-id="8ddb8-115">Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="8ddb8-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8ddb8-116">Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="8ddb8-117">Exemplo 2: obter propriedades do modo de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="8ddb8-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="8ddb8-118">Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="8ddb8-119">Esse comando especifica o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="8ddb8-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="8ddb8-120">Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="8ddb8-121">Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8ddb8-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8ddb8-122">Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="8ddb8-123">Exemplo 4: obter todas as máquinas virtuais na sua assinatura</span><span class="sxs-lookup"><span data-stu-id="8ddb8-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="8ddb8-124">Este comando obtém todas as máquinas virtuais na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="8ddb8-125">OS</span><span class="sxs-lookup"><span data-stu-id="8ddb8-125">PARAMETERS</span></span>

### <span data-ttu-id="8ddb8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddb8-126">-DefaultProfile</span></span>
<span data-ttu-id="8ddb8-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ddb8-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="8ddb8-128">-DisplayHint</span></span>
<span data-ttu-id="8ddb8-129">Determina como o objeto de máquina virtual é exibido.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="8ddb8-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="8ddb8-130">Valid values are:</span></span>

<span data-ttu-id="8ddb8-131">--Compact: exibe apenas as propriedades de nível superior</span><span class="sxs-lookup"><span data-stu-id="8ddb8-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="8ddb8-132">--Expandir: exibe todas as propriedades em todos os níveis</span><span class="sxs-lookup"><span data-stu-id="8ddb8-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="8ddb8-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ddb8-133">-Name</span></span>
<span data-ttu-id="8ddb8-134">Especifica o nome da máquina virtual a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="8ddb8-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="8ddb8-135">-NextLink</span></span>
<span data-ttu-id="8ddb8-136">Especifica o próximo link.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="8ddb8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddb8-137">-ResourceGroupName</span></span>
<span data-ttu-id="8ddb8-138">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8ddb8-139">-Status</span><span class="sxs-lookup"><span data-stu-id="8ddb8-139">-Status</span></span>
<span data-ttu-id="8ddb8-140">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="8ddb8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddb8-141">CommonParameters</span></span>
<span data-ttu-id="8ddb8-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ddb8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddb8-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddb8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddb8-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ddb8-144">INPUTS</span></span>

## <span data-ttu-id="8ddb8-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ddb8-145">OUTPUTS</span></span>

## <span data-ttu-id="8ddb8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ddb8-146">NOTES</span></span>

## <span data-ttu-id="8ddb8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ddb8-147">RELATED LINKS</span></span>

[<span data-ttu-id="8ddb8-148">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8ddb8-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="8ddb8-150">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8ddb8-151">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="8ddb8-152">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="8ddb8-153">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ddb8-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


