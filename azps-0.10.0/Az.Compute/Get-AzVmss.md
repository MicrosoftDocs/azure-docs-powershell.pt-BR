---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776999"
---
# <span data-ttu-id="fbbbc-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-101">Get-AzVmss</span></span>

## <span data-ttu-id="fbbbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbbc-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="fbbbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbbbc-104">SYNTAX</span></span>

### <span data-ttu-id="fbbbc-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="fbbbc-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbbbc-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fbbbc-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbbbc-107">DESCRIPTION</span></span>
<span data-ttu-id="fbbbc-108">O cmdlet **Get-AzVmss** Obtém o modelo e a exibição de instância de um VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="fbbbc-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fbbbc-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="fbbbc-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="fbbbc-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="fbbbc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbbbc-112">EXAMPLES</span></span>

### <span data-ttu-id="fbbbc-113">Exemplo 1: obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="fbbbc-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fbbbc-114">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="fbbbc-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="fbbbc-116">OS</span><span class="sxs-lookup"><span data-stu-id="fbbbc-116">PARAMETERS</span></span>

### <span data-ttu-id="fbbbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbbc-117">-DefaultProfile</span></span>
<span data-ttu-id="fbbbc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbbbc-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="fbbbc-119">-InstanceView</span></span>
<span data-ttu-id="fbbbc-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbbc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbbc-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbbbc-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="fbbbc-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fbbbc-123">-VMScaleSetName</span></span>
<span data-ttu-id="fbbbc-124">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="fbbbc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbbc-125">CommonParameters</span></span>
<span data-ttu-id="fbbbc-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbbc-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbbc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbbc-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbbbc-128">INPUTS</span></span>

### <span data-ttu-id="fbbbc-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fbbbc-129">None</span></span>
<span data-ttu-id="fbbbc-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbbbc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbbbc-131">OUTPUTS</span></span>

### <span data-ttu-id="fbbbc-132">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fbbbc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbbbc-133">NOTES</span></span>

## <span data-ttu-id="fbbbc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbbbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbbbc-135">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="fbbbc-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fbbbc-137">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fbbbc-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fbbbc-139">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fbbbc-140">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fbbbc-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fbbbc-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


