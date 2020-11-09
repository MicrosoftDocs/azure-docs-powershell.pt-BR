---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284114"
---
# <span data-ttu-id="df0e2-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="df0e2-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="df0e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="df0e2-103">Obtém as propriedades de uma máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="df0e2-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="df0e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df0e2-104">SYNTAX</span></span>

### <span data-ttu-id="df0e2-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="df0e2-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df0e2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="df0e2-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df0e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df0e2-107">DESCRIPTION</span></span>
<span data-ttu-id="df0e2-108">O cmdlet **Get-AzVmssVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de um computador virtual de faixa de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="df0e2-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="df0e2-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="df0e2-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="df0e2-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="df0e2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df0e2-112">EXAMPLES</span></span>

### <span data-ttu-id="df0e2-113">Exemplo 1: obter as propriedades de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="df0e2-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="df0e2-114">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="df0e2-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="df0e2-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="df0e2-116">Exemplo 2: obter as propriedades do modo de exibição de modelo de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="df0e2-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="df0e2-117">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="df0e2-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="df0e2-118">O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="df0e2-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="df0e2-119">Exemplo 3: obter as propriedades do modo de exibição de instância de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="df0e2-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="df0e2-120">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="df0e2-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="df0e2-121">Como o comando especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="df0e2-122">O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="df0e2-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="df0e2-123">OS</span><span class="sxs-lookup"><span data-stu-id="df0e2-123">PARAMETERS</span></span>

### <span data-ttu-id="df0e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0e2-124">-DefaultProfile</span></span>
<span data-ttu-id="df0e2-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df0e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df0e2-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="df0e2-126">-InstanceId</span></span>
<span data-ttu-id="df0e2-127">Especifica a ID da instância para a qual obter o modo de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="df0e2-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="df0e2-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="df0e2-128">-InstanceView</span></span>
<span data-ttu-id="df0e2-129">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df0e2-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="df0e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df0e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="df0e2-131">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="df0e2-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="df0e2-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="df0e2-132">-VMScaleSetName</span></span>
<span data-ttu-id="df0e2-133">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="df0e2-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="df0e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0e2-134">CommonParameters</span></span>
<span data-ttu-id="df0e2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0e2-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df0e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0e2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df0e2-137">INPUTS</span></span>

### <span data-ttu-id="df0e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df0e2-138">System.String</span></span>

## <span data-ttu-id="df0e2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df0e2-139">OUTPUTS</span></span>

### <span data-ttu-id="df0e2-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="df0e2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="df0e2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df0e2-141">NOTES</span></span>

## <span data-ttu-id="df0e2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df0e2-142">RELATED LINKS</span></span>

[<span data-ttu-id="df0e2-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="df0e2-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="df0e2-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="df0e2-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


