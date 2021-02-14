---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116537"
---
# <span data-ttu-id="a7081-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="a7081-101">Get-AzVMSize</span></span>

## <span data-ttu-id="a7081-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7081-102">SYNOPSIS</span></span>
<span data-ttu-id="a7081-103">Obtém tamanhos de máquina virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7081-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="a7081-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7081-104">SYNTAX</span></span>

### <span data-ttu-id="a7081-105">ListVirtualMachineSizeParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7081-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7081-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7081-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7081-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a7081-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7081-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7081-108">DESCRIPTION</span></span>
<span data-ttu-id="a7081-109">O **cmdlet Get-AzVMSize** obtém tamanhos de máquina virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7081-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="a7081-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7081-110">EXAMPLES</span></span>

### <span data-ttu-id="a7081-111">Exemplo 1: Obter tamanhos de máquina virtuais para um local</span><span class="sxs-lookup"><span data-stu-id="a7081-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="a7081-112">Esse comando obtém os tamanhos disponíveis para máquinas virtuais no local especificado.</span><span class="sxs-lookup"><span data-stu-id="a7081-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="a7081-113">Exemplo 2: Obter tamanhos para um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a7081-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="a7081-114">Esse comando obtém tamanhos disponíveis para máquinas virtuais que você pode implantar no conjunto de disponibilidade chamado AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="a7081-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="a7081-115">Exemplo 3: Obter tamanhos para uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="a7081-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="a7081-116">Esse comando obtém tamanhos disponíveis para a máquina virtual existente chamada VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="a7081-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="a7081-117">Você pode reorganizar essa máquina virtual para os tamanhos que esse comando obtém.</span><span class="sxs-lookup"><span data-stu-id="a7081-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="a7081-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7081-118">PARAMETERS</span></span>

### <span data-ttu-id="a7081-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="a7081-119">-AvailabilitySetName</span></span>
<span data-ttu-id="a7081-120">Especifica o nome do Conjunto de Disponibilidade para o qual este cmdlet obtém os tamanhos de máquina virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7081-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="a7081-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7081-121">-DefaultProfile</span></span>
<span data-ttu-id="a7081-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7081-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7081-123">-Local</span><span class="sxs-lookup"><span data-stu-id="a7081-123">-Location</span></span>
<span data-ttu-id="a7081-124">Especifica o local para o qual este cmdlet obtém os tamanhos de máquina virtuais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7081-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="a7081-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7081-125">-ResourceGroupName</span></span>
<span data-ttu-id="a7081-126">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a7081-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a7081-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="a7081-127">-VMName</span></span>
<span data-ttu-id="a7081-128">Especifica o nome da máquina virtual em que este cmdlet obtém os tamanhos de máquina virtuais disponíveis para reizing.</span><span class="sxs-lookup"><span data-stu-id="a7081-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="a7081-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7081-129">CommonParameters</span></span>
<span data-ttu-id="a7081-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7081-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7081-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7081-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7081-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7081-132">INPUTS</span></span>

### <span data-ttu-id="a7081-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a7081-133">System.String</span></span>

## <span data-ttu-id="a7081-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7081-134">OUTPUTS</span></span>

### <span data-ttu-id="a7081-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="a7081-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="a7081-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a7081-136">NOTES</span></span>

## <span data-ttu-id="a7081-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7081-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7081-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7081-138">Get-AzVM</span></span>](./Get-AzVM.md)


