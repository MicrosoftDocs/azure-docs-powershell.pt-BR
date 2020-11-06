---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429877"
---
# <span data-ttu-id="9d573-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9d573-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="9d573-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d573-102">SYNOPSIS</span></span>
<span data-ttu-id="9d573-103">Obtém informações sobre uma extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="9d573-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d573-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d573-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="9d573-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d573-105">DESCRIPTION</span></span>
<span data-ttu-id="9d573-106">O cmdlet **Get-AzureRmVMCustomScriptExtension** Obtém informações sobre uma extensão de máquina virtual de script personalizado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d573-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="9d573-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d573-107">EXAMPLES</span></span>

### <span data-ttu-id="9d573-108">Exemplo 1: obter uma extensão de script personalizada</span><span class="sxs-lookup"><span data-stu-id="9d573-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="9d573-109">Esse comando obtém a extensão de script personalizada chamada ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="9d573-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="9d573-110">Exemplo 2: obter o modo de exibição de instância de uma extensão de script personalizado</span><span class="sxs-lookup"><span data-stu-id="9d573-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="9d573-111">Este comando obtém o modo de exibição de instância da extensão de script personalizado chamado ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="9d573-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="9d573-112">OS</span><span class="sxs-lookup"><span data-stu-id="9d573-112">PARAMETERS</span></span>

### <span data-ttu-id="9d573-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d573-113">-Name</span></span>
<span data-ttu-id="9d573-114">Especifica o nome da extensão de script personalizada sobre a qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="9d573-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="9d573-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d573-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d573-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d573-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9d573-117">-Status</span><span class="sxs-lookup"><span data-stu-id="9d573-117">-Status</span></span>
<span data-ttu-id="9d573-118">Indica que esse cmdlet obtém o modo de exibição de instância da extensão de script personalizado.</span><span class="sxs-lookup"><span data-stu-id="9d573-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="9d573-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="9d573-119">-VMName</span></span>
<span data-ttu-id="9d573-120">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="9d573-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="9d573-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d573-121">CommonParameters</span></span>
<span data-ttu-id="9d573-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d573-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d573-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d573-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d573-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d573-124">INPUTS</span></span>

### <span data-ttu-id="9d573-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d573-125">None</span></span>
<span data-ttu-id="9d573-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9d573-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d573-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d573-127">OUTPUTS</span></span>

## <span data-ttu-id="9d573-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d573-128">NOTES</span></span>

## <span data-ttu-id="9d573-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d573-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d573-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9d573-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="9d573-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9d573-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="9d573-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9d573-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


