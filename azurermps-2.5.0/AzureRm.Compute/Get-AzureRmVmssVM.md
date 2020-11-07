---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: bac1bf365ff1135366f2612bfbe5ba313e2300b8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786564"
---
# <span data-ttu-id="a0f94-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a0f94-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="a0f94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0f94-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f94-103">Obtém as propriedades de uma máquina virtual VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0f94-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f94-104">SYNTAX</span></span>

### <span data-ttu-id="a0f94-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0f94-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0f94-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a0f94-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f94-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0f94-107">DESCRIPTION</span></span>
<span data-ttu-id="a0f94-108">O cmdlet **Get-AzureRmVmssVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de um computador virtual de faixa de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a0f94-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="a0f94-109">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="a0f94-110">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="a0f94-111">Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="a0f94-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0f94-112">EXAMPLES</span></span>

### <span data-ttu-id="a0f94-113">Exemplo 1: obter as propriedades de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="a0f94-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a0f94-114">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="a0f94-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="a0f94-115">Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="a0f94-116">Exemplo 2: obter as propriedades do modo de exibição de modelo de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="a0f94-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="a0f94-117">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="a0f94-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="a0f94-118">O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="a0f94-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="a0f94-119">Exemplo 3: obter as propriedades do modo de exibição de instância de uma máquina virtual VMSS</span><span class="sxs-lookup"><span data-stu-id="a0f94-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="a0f94-120">Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="a0f94-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="a0f94-121">Como o comando especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="a0f94-122">O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="a0f94-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="a0f94-123">OS</span><span class="sxs-lookup"><span data-stu-id="a0f94-123">PARAMETERS</span></span>

### <span data-ttu-id="a0f94-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f94-124">-DefaultProfile</span></span>
<span data-ttu-id="a0f94-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f94-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f94-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a0f94-126">-InstanceId</span></span>
<span data-ttu-id="a0f94-127">Especifica a ID da instância para a qual obter o modo de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="a0f94-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f94-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="a0f94-128">-InstanceView</span></span>
<span data-ttu-id="a0f94-129">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0f94-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="a0f94-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f94-130">-ResourceGroupName</span></span>
<span data-ttu-id="a0f94-131">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0f94-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="a0f94-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a0f94-132">-VMScaleSetName</span></span>
<span data-ttu-id="a0f94-133">Especifica o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a0f94-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="a0f94-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f94-134">CommonParameters</span></span>
<span data-ttu-id="a0f94-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f94-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f94-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f94-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f94-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0f94-137">INPUTS</span></span>

### <span data-ttu-id="a0f94-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a0f94-138">None</span></span>
<span data-ttu-id="a0f94-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a0f94-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0f94-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0f94-140">OUTPUTS</span></span>

### <span data-ttu-id="a0f94-141">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a0f94-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a0f94-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0f94-142">NOTES</span></span>

## <span data-ttu-id="a0f94-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0f94-143">RELATED LINKS</span></span>

[<span data-ttu-id="a0f94-144">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a0f94-144">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="a0f94-145">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0f94-145">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


