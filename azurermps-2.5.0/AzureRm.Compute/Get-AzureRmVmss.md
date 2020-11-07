---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785993"
---
# <span data-ttu-id="46731-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="46731-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46731-102">SYNOPSIS</span></span>
<span data-ttu-id="46731-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="46731-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46731-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46731-104">SYNTAX</span></span>

### <span data-ttu-id="46731-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="46731-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46731-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="46731-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46731-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46731-107">DESCRIPTION</span></span>
<span data-ttu-id="46731-108">O cmdlet **Get-AzureRmVmss** Obtém o modelo e a exibição de instância de um VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="46731-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="46731-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46731-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="46731-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46731-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="46731-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46731-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="46731-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46731-112">EXAMPLES</span></span>

### <span data-ttu-id="46731-113">Exemplo 1: obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="46731-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="46731-114">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="46731-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="46731-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46731-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="46731-116">OS</span><span class="sxs-lookup"><span data-stu-id="46731-116">PARAMETERS</span></span>

### <span data-ttu-id="46731-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46731-117">-DefaultProfile</span></span>
<span data-ttu-id="46731-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46731-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46731-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="46731-119">-InstanceView</span></span>
<span data-ttu-id="46731-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46731-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="46731-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46731-121">-ResourceGroupName</span></span>
<span data-ttu-id="46731-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="46731-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="46731-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="46731-123">-VMScaleSetName</span></span>
<span data-ttu-id="46731-124">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="46731-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="46731-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46731-125">CommonParameters</span></span>
<span data-ttu-id="46731-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46731-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46731-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46731-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46731-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46731-128">INPUTS</span></span>

### <span data-ttu-id="46731-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="46731-129">None</span></span>
<span data-ttu-id="46731-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="46731-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46731-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46731-131">OUTPUTS</span></span>

### <span data-ttu-id="46731-132">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="46731-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="46731-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46731-133">NOTES</span></span>

## <span data-ttu-id="46731-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46731-134">RELATED LINKS</span></span>

[<span data-ttu-id="46731-135">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="46731-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="46731-137">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="46731-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="46731-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="46731-140">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="46731-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="46731-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


