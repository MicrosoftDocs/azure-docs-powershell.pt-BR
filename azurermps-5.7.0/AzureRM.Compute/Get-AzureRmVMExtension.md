---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427630"
---
# <span data-ttu-id="8ff96-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ff96-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="8ff96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ff96-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff96-103">Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ff96-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ff96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ff96-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ff96-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff96-106">O cmdlet **Get-AzureRmVMExtension** Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ff96-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="8ff96-107">Especifique o nome de uma extensão para a qual obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="8ff96-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="8ff96-108">Para obter apenas o modo de exibição de instância de uma extensão, especifique o parâmetro status.</span><span class="sxs-lookup"><span data-stu-id="8ff96-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="8ff96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ff96-109">EXAMPLES</span></span>

### <span data-ttu-id="8ff96-110">Exemplo 1: obter propriedades de uma extensão</span><span class="sxs-lookup"><span data-stu-id="8ff96-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="8ff96-111">Este comando obtém as propriedades da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8ff96-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="8ff96-112">Exemplo 2: obter o modo de exibição de instância de uma extensão</span><span class="sxs-lookup"><span data-stu-id="8ff96-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="8ff96-113">Esse comando obtém o modo de exibição de instância da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8ff96-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8ff96-114">OS</span><span class="sxs-lookup"><span data-stu-id="8ff96-114">PARAMETERS</span></span>

### <span data-ttu-id="8ff96-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ff96-115">-Name</span></span>
<span data-ttu-id="8ff96-116">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="8ff96-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="8ff96-117">Esse cmdlet obtém as propriedades da extensão que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8ff96-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ff96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff96-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ff96-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ff96-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8ff96-120">-Status</span><span class="sxs-lookup"><span data-stu-id="8ff96-120">-Status</span></span>
<span data-ttu-id="8ff96-121">Indica que esse cmdlet obtém apenas o modo de exibição de instância de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="8ff96-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="8ff96-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="8ff96-122">-VMName</span></span>
<span data-ttu-id="8ff96-123">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ff96-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8ff96-124">Esse cmdlet obtém as propriedades de uma extensão da máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8ff96-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ff96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff96-125">CommonParameters</span></span>
<span data-ttu-id="8ff96-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff96-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ff96-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff96-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ff96-128">INPUTS</span></span>

### <span data-ttu-id="8ff96-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ff96-129">None</span></span>
<span data-ttu-id="8ff96-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8ff96-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ff96-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ff96-131">OUTPUTS</span></span>

## <span data-ttu-id="8ff96-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ff96-132">NOTES</span></span>

## <span data-ttu-id="8ff96-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ff96-133">RELATED LINKS</span></span>

[<span data-ttu-id="8ff96-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ff96-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="8ff96-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ff96-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


