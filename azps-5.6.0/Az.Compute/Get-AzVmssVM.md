---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891875"
---
# <span data-ttu-id="cbcf3-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cbcf3-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="cbcf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf3-103">Obtém as propriedades de uma máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="cbcf3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbcf3-104">SYNTAX</span></span>

### <span data-ttu-id="cbcf3-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbcf3-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbcf3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cbcf3-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcf3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbcf3-107">DESCRIPTION</span></span>
<span data-ttu-id="cbcf3-108">O cmdlet **Get-AzVmssVM** obtém a exibição de modelo e a exibição de instância de uma máquina virtual VMSS (Conjunto de Escala de Máquina Virtual).</span><span class="sxs-lookup"><span data-stu-id="cbcf3-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="cbcf3-109">O modelo de exibição é as propriedades especificadas pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="cbcf3-110">O exemplo de exibição é o status de nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="cbcf3-111">*Especifique o parâmetro Status* para obter apenas a exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="cbcf3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-112">EXAMPLES</span></span>

### <span data-ttu-id="cbcf3-113">Exemplo 1: Obter as propriedades de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cbcf3-114">Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="cbcf3-115">Como o comando não especifica o parâmetro de opção *InstanceView,* o cmdlet obtém a exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="cbcf3-116">Exemplo 2: Obter as propriedades de exibição de modelo de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="cbcf3-117">Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cbcf3-118">O comando obtém a ID da instância armazenada na variável $ID para obter o exibição do modelo.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="cbcf3-119">Exemplo 3: Obter as propriedades de exibição de instância de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="cbcf3-120">Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cbcf3-121">Como o comando especifica o parâmetro de opção *InstanceView,* o cmdlet obtém a exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="cbcf3-122">O comando obtém a ID da instância armazenada na variável $ID para obter o exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="cbcf3-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-123">PARAMETERS</span></span>

### <span data-ttu-id="cbcf3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf3-124">-DefaultProfile</span></span>
<span data-ttu-id="cbcf3-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcf3-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cbcf3-126">-InstanceId</span></span>
<span data-ttu-id="cbcf3-127">Especifica a ID da instância para a qual obter o modelo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="cbcf3-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="cbcf3-128">-InstanceView</span></span>
<span data-ttu-id="cbcf3-129">Indica que esse cmdlet obtém apenas a exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf3-130">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf3-131">Especifica o nome do Grupo de Recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf3-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cbcf3-132">-VMScaleSetName</span></span>
<span data-ttu-id="cbcf3-133">Especiem o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf3-134">CommonParameters</span></span>
<span data-ttu-id="cbcf3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcf3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf3-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbcf3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-137">INPUTS</span></span>

### <span data-ttu-id="cbcf3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cbcf3-138">System.String</span></span>

## <span data-ttu-id="cbcf3-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-139">OUTPUTS</span></span>

### <span data-ttu-id="cbcf3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cbcf3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cbcf3-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbcf3-141">NOTES</span></span>

## <span data-ttu-id="cbcf3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbcf3-142">RELATED LINKS</span></span>

[<span data-ttu-id="cbcf3-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cbcf3-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="cbcf3-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cbcf3-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


