---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609849"
---
# <span data-ttu-id="cb2dd-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="cb2dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2dd-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb2dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb2dd-104">SYNTAX</span></span>

### <span data-ttu-id="cb2dd-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb2dd-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2dd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cb2dd-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2dd-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="cb2dd-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb2dd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb2dd-108">DESCRIPTION</span></span>
<span data-ttu-id="cb2dd-109">O cmdlet **Get-AzureRmVmss** Obtém o modelo e a exibição de instância de um VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="cb2dd-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cb2dd-110">O modo de exibição de modelo é o usuário especificado Propriedades do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="cb2dd-111">O modo de exibição de instância é o status do nível da instância do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="cb2dd-112">Especifique o parâmetro *InstanceView* para obter apenas o modo de exibição de instância de um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="cb2dd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb2dd-113">EXAMPLES</span></span>

### <span data-ttu-id="cb2dd-114">Exemplo 1: obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="cb2dd-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cb2dd-115">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="cb2dd-116">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="cb2dd-117">OS</span><span class="sxs-lookup"><span data-stu-id="cb2dd-117">PARAMETERS</span></span>

### <span data-ttu-id="cb2dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2dd-118">-DefaultProfile</span></span>
<span data-ttu-id="cb2dd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2dd-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="cb2dd-120">-InstanceView</span></span>
<span data-ttu-id="cb2dd-121">Indica que esse cmdlet obtém apenas o modo de exibição de instância do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="cb2dd-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="cb2dd-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="cb2dd-123">Indica que esse cmdlet lista o histórico de atualização do sistema operacional do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb2dd-125">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-125">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2dd-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cb2dd-126">-VMScaleSetName</span></span>
<span data-ttu-id="cb2dd-127">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2dd-128">CommonParameters</span></span>
<span data-ttu-id="cb2dd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2dd-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2dd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb2dd-131">INPUTS</span></span>

### <span data-ttu-id="cb2dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2dd-132">System.String</span></span>

## <span data-ttu-id="cb2dd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb2dd-133">OUTPUTS</span></span>

### <span data-ttu-id="cb2dd-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cb2dd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cb2dd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb2dd-135">NOTES</span></span>

## <span data-ttu-id="cb2dd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb2dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb2dd-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-142">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="cb2dd-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb2dd-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


