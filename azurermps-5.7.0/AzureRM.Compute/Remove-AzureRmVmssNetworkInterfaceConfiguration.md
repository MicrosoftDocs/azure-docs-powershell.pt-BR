---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429846"
---
# <span data-ttu-id="14d81-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="14d81-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="14d81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14d81-102">SYNOPSIS</span></span>
<span data-ttu-id="14d81-103">Remove uma configuração de interface de rede de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="14d81-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14d81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14d81-104">SYNTAX</span></span>

### <span data-ttu-id="14d81-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d81-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d81-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d81-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d81-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14d81-107">DESCRIPTION</span></span>
<span data-ttu-id="14d81-108">O cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** remove uma configuração de interface de rede de um conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="14d81-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="14d81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14d81-109">EXAMPLES</span></span>

### <span data-ttu-id="14d81-110">Exemplo 1: remover uma configuração de interface</span><span class="sxs-lookup"><span data-stu-id="14d81-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="14d81-111">O primeiro comando obtém um VMSS usando o cmdlet Get-AzureRmVmss e, em seguida, armazena-o na variável $VMSS.</span><span class="sxs-lookup"><span data-stu-id="14d81-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="14d81-112">O segundo comando Remove a configuração de interface de rede chamada ContosoVmssInterface02 do conjunto em $VMSS.</span><span class="sxs-lookup"><span data-stu-id="14d81-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="14d81-113">OS</span><span class="sxs-lookup"><span data-stu-id="14d81-113">PARAMETERS</span></span>

### <span data-ttu-id="14d81-114">-ID</span><span class="sxs-lookup"><span data-stu-id="14d81-114">-Id</span></span>
<span data-ttu-id="14d81-115">Especifica a ID da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="14d81-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d81-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="14d81-116">-Name</span></span>
<span data-ttu-id="14d81-117">Especifica o nome da configuração da interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="14d81-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d81-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14d81-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="14d81-119">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="14d81-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d81-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14d81-120">-Confirm</span></span>
<span data-ttu-id="14d81-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d81-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d81-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d81-122">-WhatIf</span></span>
<span data-ttu-id="14d81-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14d81-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14d81-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14d81-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d81-125">CommonParameters</span></span>
<span data-ttu-id="14d81-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d81-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d81-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d81-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14d81-128">INPUTS</span></span>

### <span data-ttu-id="14d81-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="14d81-129">None</span></span>
<span data-ttu-id="14d81-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="14d81-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14d81-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14d81-131">OUTPUTS</span></span>

## <span data-ttu-id="14d81-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14d81-132">NOTES</span></span>

## <span data-ttu-id="14d81-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14d81-133">RELATED LINKS</span></span>

[<span data-ttu-id="14d81-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="14d81-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="14d81-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="14d81-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


