---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428982"
---
# <span data-ttu-id="cebb3-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cebb3-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="cebb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cebb3-102">SYNOPSIS</span></span>
<span data-ttu-id="cebb3-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="cebb3-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cebb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cebb3-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="cebb3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cebb3-105">DESCRIPTION</span></span>
<span data-ttu-id="cebb3-106">O cmdlet **Get-AzureRmVMAccessExtension** Obtém informações sobre a extensão da máquina virtual do VMAccess (acesso à máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="cebb3-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="cebb3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cebb3-107">EXAMPLES</span></span>

### <span data-ttu-id="cebb3-108">Exemplo 1: obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="cebb3-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="cebb3-109">Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="cebb3-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="cebb3-110">Exemplo 2: obter o modo de exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="cebb3-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="cebb3-111">Esse comando obtém o modo de exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="cebb3-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="cebb3-112">OS</span><span class="sxs-lookup"><span data-stu-id="cebb3-112">PARAMETERS</span></span>

### <span data-ttu-id="cebb3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cebb3-113">-Name</span></span>
<span data-ttu-id="cebb3-114">Especifica o nome da extensão obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebb3-114">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebb3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebb3-115">-ResourceGroupName</span></span>
<span data-ttu-id="cebb3-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cebb3-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebb3-117">-Status</span><span class="sxs-lookup"><span data-stu-id="cebb3-117">-Status</span></span>
<span data-ttu-id="cebb3-118">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="cebb3-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebb3-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="cebb3-119">-VMName</span></span>
<span data-ttu-id="cebb3-120">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cebb3-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cebb3-121">Este cmdlet obtém informações sobre VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cebb3-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cebb3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebb3-122">CommonParameters</span></span>
<span data-ttu-id="cebb3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebb3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebb3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cebb3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebb3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cebb3-125">INPUTS</span></span>

### <span data-ttu-id="cebb3-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cebb3-126">None</span></span>
<span data-ttu-id="cebb3-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cebb3-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cebb3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cebb3-128">OUTPUTS</span></span>

## <span data-ttu-id="cebb3-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cebb3-129">NOTES</span></span>

## <span data-ttu-id="cebb3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cebb3-130">RELATED LINKS</span></span>

[<span data-ttu-id="cebb3-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cebb3-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cebb3-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cebb3-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cebb3-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="cebb3-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


