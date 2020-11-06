---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 33abc50f4cc336230e1c6f4ef14d12f51b22af83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441578"
---
# <span data-ttu-id="4a665-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="4a665-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="4a665-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a665-102">SYNOPSIS</span></span>
<span data-ttu-id="4a665-103">Obtém tamanhos de máquina virtual disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4a665-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a665-104">SYNTAX</span></span>

### <span data-ttu-id="4a665-105">ListVirtualMachineSizeParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a665-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a665-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a665-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a665-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a665-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a665-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a665-108">DESCRIPTION</span></span>
<span data-ttu-id="4a665-109">O cmdlet **Get-AzureRmVMSize** Obtém os tamanhos das máquinas virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4a665-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="4a665-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a665-110">EXAMPLES</span></span>

### <span data-ttu-id="4a665-111">Exemplo 1: obter tamanhos de máquina virtual para um local</span><span class="sxs-lookup"><span data-stu-id="4a665-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="4a665-112">Esse comando obtém os tamanhos disponíveis para máquinas virtuais no local especificado.</span><span class="sxs-lookup"><span data-stu-id="4a665-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="4a665-113">Exemplo 2: obter tamanhos para um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4a665-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="4a665-114">Esse comando obtém tamanhos disponíveis para máquinas virtuais que você pode implantar no conjunto de disponibilidade chamado AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="4a665-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="4a665-115">Exemplo 3: obter os tamanhos de uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="4a665-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="4a665-116">Esse comando obtém os tamanhos disponíveis para a máquina virtual existente chamada VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="4a665-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="4a665-117">Você pode redimensionar essa máquina virtual para os tamanhos que esse comando obtém.</span><span class="sxs-lookup"><span data-stu-id="4a665-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="4a665-118">OS</span><span class="sxs-lookup"><span data-stu-id="4a665-118">PARAMETERS</span></span>

### <span data-ttu-id="4a665-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="4a665-119">-AvailabilitySetName</span></span>
<span data-ttu-id="4a665-120">Especifica o nome do conjunto de disponibilidade para o qual este cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="4a665-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a665-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a665-121">-DefaultProfile</span></span>
<span data-ttu-id="4a665-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a665-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a665-123">-Local</span><span class="sxs-lookup"><span data-stu-id="4a665-123">-Location</span></span>
<span data-ttu-id="4a665-124">Especifica o local para o qual esse cmdlet obtém os tamanhos da máquina virtual disponível.</span><span class="sxs-lookup"><span data-stu-id="4a665-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a665-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a665-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a665-126">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4a665-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a665-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="4a665-127">-VMName</span></span>
<span data-ttu-id="4a665-128">Especifica o nome da máquina virtual em que este cmdlet obtém os tamanhos da máquina virtual disponível para redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="4a665-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a665-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a665-129">CommonParameters</span></span>
<span data-ttu-id="4a665-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a665-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a665-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a665-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a665-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a665-132">INPUTS</span></span>

## <span data-ttu-id="4a665-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a665-133">OUTPUTS</span></span>

## <span data-ttu-id="4a665-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a665-134">NOTES</span></span>

## <span data-ttu-id="4a665-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a665-135">RELATED LINKS</span></span>

[<span data-ttu-id="4a665-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a665-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


