---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440508"
---
# <span data-ttu-id="f425c-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="f425c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f425c-102">SYNOPSIS</span></span>
<span data-ttu-id="f425c-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="f425c-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f425c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f425c-104">SYNTAX</span></span>

### <span data-ttu-id="f425c-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f425c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="f425c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f425c-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="f425c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f425c-107">DESCRIPTION</span></span>
<span data-ttu-id="f425c-108">O cmdlet **Get-AzureRmVmss** Obtém o modelo e a exibição de instância de um VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="f425c-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f425c-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f425c-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="f425c-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f425c-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="f425c-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f425c-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="f425c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f425c-112">EXAMPLES</span></span>

### <span data-ttu-id="f425c-113">Exemplo 1: obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="f425c-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f425c-114">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="f425c-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="f425c-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f425c-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="f425c-116">OS</span><span class="sxs-lookup"><span data-stu-id="f425c-116">PARAMETERS</span></span>

### <span data-ttu-id="f425c-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="f425c-117">-InstanceView</span></span>
<span data-ttu-id="f425c-118">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f425c-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f425c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f425c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f425c-120">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f425c-120">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f425c-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f425c-121">-VMScaleSetName</span></span>
<span data-ttu-id="f425c-122">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f425c-122">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f425c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f425c-123">CommonParameters</span></span>
<span data-ttu-id="f425c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f425c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f425c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f425c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f425c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f425c-126">INPUTS</span></span>

### <span data-ttu-id="f425c-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f425c-127">None</span></span>
<span data-ttu-id="f425c-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f425c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f425c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f425c-129">OUTPUTS</span></span>

### <span data-ttu-id="f425c-130">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f425c-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f425c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f425c-131">NOTES</span></span>

## <span data-ttu-id="f425c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f425c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f425c-133">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f425c-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f425c-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f425c-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="f425c-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f425c-138">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f425c-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f425c-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


