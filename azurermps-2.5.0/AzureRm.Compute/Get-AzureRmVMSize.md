---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
ms.openlocfilehash: 77e4de344e3dd89eac09b1ebefb6ba49071dcbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786573"
---
# <span data-ttu-id="941fc-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="941fc-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="941fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="941fc-102">SYNOPSIS</span></span>
<span data-ttu-id="941fc-103">Obtém tamanhos de máquina virtual disponíveis.</span><span class="sxs-lookup"><span data-stu-id="941fc-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="941fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="941fc-104">SYNTAX</span></span>

### <span data-ttu-id="941fc-105">ListVirtualMachineSizeParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="941fc-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941fc-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="941fc-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941fc-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="941fc-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="941fc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="941fc-108">DESCRIPTION</span></span>
<span data-ttu-id="941fc-109">O cmdlet **Get-AzureRmVMSize** Obtém os tamanhos das máquinas virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="941fc-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="941fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="941fc-110">EXAMPLES</span></span>

### <span data-ttu-id="941fc-111">Exemplo 1: obter tamanhos de máquina virtual para um local</span><span class="sxs-lookup"><span data-stu-id="941fc-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="941fc-112">Esse comando obtém os tamanhos disponíveis para máquinas virtuais no local especificado.</span><span class="sxs-lookup"><span data-stu-id="941fc-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="941fc-113">Exemplo 2: obter tamanhos para um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="941fc-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="941fc-114">Esse comando obtém tamanhos disponíveis para máquinas virtuais que você pode implantar no conjunto de disponibilidade chamado AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="941fc-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="941fc-115">Exemplo 3: obter os tamanhos de uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="941fc-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="941fc-116">Esse comando obtém os tamanhos disponíveis para a máquina virtual existente chamada VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="941fc-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="941fc-117">Você pode redimensionar essa máquina virtual para os tamanhos que esse comando obtém.</span><span class="sxs-lookup"><span data-stu-id="941fc-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="941fc-118">OS</span><span class="sxs-lookup"><span data-stu-id="941fc-118">PARAMETERS</span></span>

### <span data-ttu-id="941fc-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="941fc-119">-AvailabilitySetName</span></span>
<span data-ttu-id="941fc-120">Especifica o nome do conjunto de disponibilidade para o qual este cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="941fc-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="941fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941fc-121">-DefaultProfile</span></span>
<span data-ttu-id="941fc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="941fc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="941fc-123">-Local</span><span class="sxs-lookup"><span data-stu-id="941fc-123">-Location</span></span>
<span data-ttu-id="941fc-124">Especifica o local para o qual esse cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="941fc-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="941fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="941fc-126">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="941fc-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="941fc-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="941fc-127">-VMName</span></span>
<span data-ttu-id="941fc-128">Especifica o nome da máquina virtual em que este cmdlet obtém os tamanhos da máquina virtual disponível para redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="941fc-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="941fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941fc-129">CommonParameters</span></span>
<span data-ttu-id="941fc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941fc-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="941fc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941fc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="941fc-132">INPUTS</span></span>

### <span data-ttu-id="941fc-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="941fc-133">None</span></span>
<span data-ttu-id="941fc-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="941fc-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="941fc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="941fc-135">OUTPUTS</span></span>

### <span data-ttu-id="941fc-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="941fc-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="941fc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="941fc-137">NOTES</span></span>

## <span data-ttu-id="941fc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="941fc-138">RELATED LINKS</span></span>

[<span data-ttu-id="941fc-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="941fc-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


