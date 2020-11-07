---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948431"
---
# <span data-ttu-id="36a4d-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="36a4d-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="36a4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="36a4d-103">Obtém informações sobre uma extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="36a4d-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="36a4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36a4d-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="36a4d-106">O cmdlet **Get-AzVMCustomScriptExtension** Obtém informações sobre uma extensão de máquina virtual de script personalizado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36a4d-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="36a4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="36a4d-108">Exemplo 1: obter uma extensão de script personalizada</span><span class="sxs-lookup"><span data-stu-id="36a4d-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="36a4d-109">Esse comando obtém a extensão de script personalizada chamada ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="36a4d-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="36a4d-110">Exemplo 2: obter o modo de exibição de instância de uma extensão de script personalizado</span><span class="sxs-lookup"><span data-stu-id="36a4d-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="36a4d-111">Este comando obtém o modo de exibição de instância da extensão de script personalizado chamado ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="36a4d-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="36a4d-112">OS</span><span class="sxs-lookup"><span data-stu-id="36a4d-112">PARAMETERS</span></span>

### <span data-ttu-id="36a4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a4d-113">-DefaultProfile</span></span>
<span data-ttu-id="36a4d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36a4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36a4d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="36a4d-115">-Name</span></span>
<span data-ttu-id="36a4d-116">Especifica o nome da extensão de script personalizada sobre a qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="36a4d-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="36a4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="36a4d-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36a4d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="36a4d-119">-Status</span><span class="sxs-lookup"><span data-stu-id="36a4d-119">-Status</span></span>
<span data-ttu-id="36a4d-120">Indica que esse cmdlet obtém o modo de exibição de instância da extensão de script personalizado.</span><span class="sxs-lookup"><span data-stu-id="36a4d-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="36a4d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="36a4d-121">-VMName</span></span>
<span data-ttu-id="36a4d-122">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="36a4d-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="36a4d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a4d-123">CommonParameters</span></span>
<span data-ttu-id="36a4d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a4d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a4d-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36a4d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a4d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36a4d-126">INPUTS</span></span>

### <span data-ttu-id="36a4d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="36a4d-127">System.String</span></span>

### <span data-ttu-id="36a4d-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36a4d-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36a4d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36a4d-129">OUTPUTS</span></span>

### <span data-ttu-id="36a4d-130">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="36a4d-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="36a4d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36a4d-131">NOTES</span></span>

## <span data-ttu-id="36a4d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36a4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="36a4d-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="36a4d-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="36a4d-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="36a4d-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="36a4d-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="36a4d-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


