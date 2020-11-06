---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 4aaee403007561797614b2534e29c5918dad3643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432780"
---
# <span data-ttu-id="dd852-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dd852-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="dd852-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd852-102">SYNOPSIS</span></span>
<span data-ttu-id="dd852-103">Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd852-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd852-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd852-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd852-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd852-105">DESCRIPTION</span></span>
<span data-ttu-id="dd852-106">O cmdlet **Get-AzureRmVMExtension** Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd852-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="dd852-107">Especifique o nome de uma extensão para a qual obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd852-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="dd852-108">Para obter apenas o modo de exibição de instância de uma extensão, especifique o parâmetro status.</span><span class="sxs-lookup"><span data-stu-id="dd852-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="dd852-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd852-109">EXAMPLES</span></span>

### <span data-ttu-id="dd852-110">Exemplo 1: obter propriedades de uma extensão</span><span class="sxs-lookup"><span data-stu-id="dd852-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="dd852-111">Este comando obtém as propriedades da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd852-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="dd852-112">Exemplo 2: obter o modo de exibição de instância de uma extensão</span><span class="sxs-lookup"><span data-stu-id="dd852-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="dd852-113">Esse comando obtém o modo de exibição de instância da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd852-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="dd852-114">OS</span><span class="sxs-lookup"><span data-stu-id="dd852-114">PARAMETERS</span></span>

### <span data-ttu-id="dd852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd852-115">-DefaultProfile</span></span>
<span data-ttu-id="dd852-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd852-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd852-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd852-117">-Name</span></span>
<span data-ttu-id="dd852-118">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="dd852-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="dd852-119">Esse cmdlet obtém as propriedades da extensão que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dd852-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd852-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd852-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd852-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd852-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd852-122">-Status</span><span class="sxs-lookup"><span data-stu-id="dd852-122">-Status</span></span>
<span data-ttu-id="dd852-123">Indica que esse cmdlet obtém apenas o modo de exibição de instância de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="dd852-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd852-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="dd852-124">-VMName</span></span>
<span data-ttu-id="dd852-125">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd852-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dd852-126">Esse cmdlet obtém as propriedades de uma extensão da máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dd852-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd852-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd852-127">CommonParameters</span></span>
<span data-ttu-id="dd852-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd852-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd852-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd852-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd852-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd852-130">INPUTS</span></span>

### <span data-ttu-id="dd852-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dd852-131">System.String</span></span>

### <span data-ttu-id="dd852-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd852-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd852-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd852-133">OUTPUTS</span></span>

### <span data-ttu-id="dd852-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="dd852-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="dd852-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd852-135">NOTES</span></span>

## <span data-ttu-id="dd852-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd852-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd852-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dd852-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="dd852-138">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dd852-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


