---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116416"
---
# <span data-ttu-id="516d8-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="516d8-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="516d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="516d8-102">SYNOPSIS</span></span>
<span data-ttu-id="516d8-103">Obtém as configurações da extensão DSC em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="516d8-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="516d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="516d8-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="516d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="516d8-105">DESCRIPTION</span></span>
<span data-ttu-id="516d8-106">O cmdlet **Get-AzVMDscExtension** Obtém as configurações da extensão da configuração de estado desejada (DSC) em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="516d8-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="516d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="516d8-107">EXAMPLES</span></span>

### <span data-ttu-id="516d8-108">Exemplo 1: obter as configurações de uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="516d8-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="516d8-109">Esse comando obtém as configurações de extensão nomeada como DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="516d8-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="516d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="516d8-110">PARAMETERS</span></span>

### <span data-ttu-id="516d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516d8-111">-DefaultProfile</span></span>
<span data-ttu-id="516d8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="516d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="516d8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="516d8-113">-Name</span></span>
<span data-ttu-id="516d8-114">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="516d8-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="516d8-115">O cmdlet Set-AzVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="516d8-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="516d8-116">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzVMDscExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="516d8-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="516d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="516d8-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="516d8-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="516d8-119">-Status</span><span class="sxs-lookup"><span data-stu-id="516d8-119">-Status</span></span>
<span data-ttu-id="516d8-120">Indica que esse cmdlet obtém o modo de exibição de instância da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="516d8-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="516d8-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="516d8-121">-VMName</span></span>
<span data-ttu-id="516d8-122">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="516d8-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="516d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516d8-123">CommonParameters</span></span>
<span data-ttu-id="516d8-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516d8-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="516d8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516d8-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="516d8-126">INPUTS</span></span>

### <span data-ttu-id="516d8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="516d8-127">System.String</span></span>

### <span data-ttu-id="516d8-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="516d8-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="516d8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="516d8-129">OUTPUTS</span></span>

### <span data-ttu-id="516d8-130">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="516d8-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="516d8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="516d8-131">NOTES</span></span>

## <span data-ttu-id="516d8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="516d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="516d8-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="516d8-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="516d8-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="516d8-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


