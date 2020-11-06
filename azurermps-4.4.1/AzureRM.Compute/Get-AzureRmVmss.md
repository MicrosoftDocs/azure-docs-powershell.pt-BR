---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432640"
---
# <span data-ttu-id="c4b0d-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="c4b0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b0d-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4b0d-104">SYNTAX</span></span>

### <span data-ttu-id="c4b0d-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4b0d-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b0d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c4b0d-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4b0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4b0d-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b0d-108">O cmdlet **Get-AzureRmVmss** Obtém o modelo e a exibição de instância de um VMSS (conjunto de escala de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="c4b0d-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c4b0d-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="c4b0d-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="c4b0d-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="c4b0d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4b0d-112">EXAMPLES</span></span>

### <span data-ttu-id="c4b0d-113">Exemplo 1: obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="c4b0d-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c4b0d-114">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c4b0d-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="c4b0d-116">OS</span><span class="sxs-lookup"><span data-stu-id="c4b0d-116">PARAMETERS</span></span>

### <span data-ttu-id="c4b0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b0d-117">-DefaultProfile</span></span>
<span data-ttu-id="c4b0d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b0d-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c4b0d-119">-InstanceView</span></span>
<span data-ttu-id="c4b0d-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="c4b0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4b0d-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="c4b0d-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c4b0d-123">-VMScaleSetName</span></span>
<span data-ttu-id="c4b0d-124">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="c4b0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b0d-125">CommonParameters</span></span>
<span data-ttu-id="c4b0d-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b0d-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b0d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b0d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4b0d-128">INPUTS</span></span>

## <span data-ttu-id="c4b0d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4b0d-129">OUTPUTS</span></span>

### <span data-ttu-id="c4b0d-130">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c4b0d-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c4b0d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4b0d-131">NOTES</span></span>

## <span data-ttu-id="c4b0d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4b0d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4b0d-133">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-137">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-138">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c4b0d-139">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4b0d-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


