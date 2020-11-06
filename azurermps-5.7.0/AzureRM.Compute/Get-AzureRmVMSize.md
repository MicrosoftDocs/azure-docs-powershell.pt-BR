---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431061"
---
# <span data-ttu-id="a87ea-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="a87ea-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="a87ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a87ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a87ea-103">Obtém tamanhos de máquina virtual disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a87ea-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a87ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a87ea-104">SYNTAX</span></span>

### <span data-ttu-id="a87ea-105">ListVirtualMachineSizeParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a87ea-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="a87ea-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a87ea-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="a87ea-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a87ea-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="a87ea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a87ea-108">DESCRIPTION</span></span>
<span data-ttu-id="a87ea-109">O cmdlet **Get-AzureRmVMSize** Obtém os tamanhos das máquinas virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a87ea-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="a87ea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a87ea-110">EXAMPLES</span></span>

### <span data-ttu-id="a87ea-111">Exemplo 1: obter tamanhos de máquina virtual para um local</span><span class="sxs-lookup"><span data-stu-id="a87ea-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="a87ea-112">Esse comando obtém os tamanhos disponíveis para máquinas virtuais no local especificado.</span><span class="sxs-lookup"><span data-stu-id="a87ea-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="a87ea-113">Exemplo 2: obter tamanhos para um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a87ea-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="a87ea-114">Esse comando obtém tamanhos disponíveis para máquinas virtuais que você pode implantar no conjunto de disponibilidade chamado AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="a87ea-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="a87ea-115">Exemplo 3: obter os tamanhos de uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="a87ea-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="a87ea-116">Esse comando obtém os tamanhos disponíveis para a máquina virtual existente chamada VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="a87ea-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="a87ea-117">Você pode redimensionar essa máquina virtual para os tamanhos que esse comando obtém.</span><span class="sxs-lookup"><span data-stu-id="a87ea-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="a87ea-118">OS</span><span class="sxs-lookup"><span data-stu-id="a87ea-118">PARAMETERS</span></span>

### <span data-ttu-id="a87ea-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="a87ea-119">-AvailabilitySetName</span></span>
<span data-ttu-id="a87ea-120">Especifica o nome do conjunto de disponibilidade para o qual este cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="a87ea-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87ea-121">-Local</span><span class="sxs-lookup"><span data-stu-id="a87ea-121">-Location</span></span>
<span data-ttu-id="a87ea-122">Especifica o local para o qual esse cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="a87ea-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="a87ea-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a87ea-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87ea-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="a87ea-125">-VMName</span></span>
<span data-ttu-id="a87ea-126">Especifica o nome da máquina virtual em que este cmdlet obtém os tamanhos da máquina virtual disponível para redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a87ea-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87ea-127">CommonParameters</span></span>
<span data-ttu-id="a87ea-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87ea-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87ea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87ea-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a87ea-130">INPUTS</span></span>

### <span data-ttu-id="a87ea-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a87ea-131">None</span></span>
<span data-ttu-id="a87ea-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a87ea-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a87ea-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a87ea-133">OUTPUTS</span></span>

## <span data-ttu-id="a87ea-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a87ea-134">NOTES</span></span>

## <span data-ttu-id="a87ea-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a87ea-135">RELATED LINKS</span></span>

[<span data-ttu-id="a87ea-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a87ea-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


