---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430229"
---
# <span data-ttu-id="21fbe-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="21fbe-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="21fbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="21fbe-103">Obtém as configurações da extensão DSC em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21fbe-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="21fbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21fbe-104">SYNTAX</span></span>

### <span data-ttu-id="21fbe-105">GetDscExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="21fbe-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21fbe-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="21fbe-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21fbe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="21fbe-108">O cmdlet **Get-AzVMDscExtension** Obtém as configurações da extensão da configuração de estado desejada (DSC) em uma determinada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21fbe-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="21fbe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="21fbe-110">Exemplo 1: obter as configurações de uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="21fbe-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="21fbe-111">Esse comando obtém as configurações de extensão nomeada como DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="21fbe-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="21fbe-112">OS</span><span class="sxs-lookup"><span data-stu-id="21fbe-112">PARAMETERS</span></span>

### <span data-ttu-id="21fbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fbe-113">-DefaultProfile</span></span>
<span data-ttu-id="21fbe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21fbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21fbe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="21fbe-115">-Name</span></span>
<span data-ttu-id="21fbe-116">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="21fbe-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="21fbe-117">O cmdlet Set-AzVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o mesmo valor que é usado pelo **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="21fbe-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="21fbe-118">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzVMDscExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="21fbe-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21fbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="21fbe-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="21fbe-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21fbe-121">-Status</span><span class="sxs-lookup"><span data-stu-id="21fbe-121">-Status</span></span>
<span data-ttu-id="21fbe-122">Indica que esse cmdlet obtém o modo de exibição de instância da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="21fbe-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="21fbe-123">-VM</span><span class="sxs-lookup"><span data-stu-id="21fbe-123">-VM</span></span>
<span data-ttu-id="21fbe-124">Especifica o objeto da máquina virtual na qual a extensão está.</span><span class="sxs-lookup"><span data-stu-id="21fbe-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21fbe-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="21fbe-125">-VMName</span></span>
<span data-ttu-id="21fbe-126">Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="21fbe-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21fbe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fbe-127">CommonParameters</span></span>
<span data-ttu-id="21fbe-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21fbe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fbe-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21fbe-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fbe-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21fbe-130">INPUTS</span></span>

### <span data-ttu-id="21fbe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="21fbe-131">System.String</span></span>

### <span data-ttu-id="21fbe-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="21fbe-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="21fbe-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21fbe-133">OUTPUTS</span></span>

### <span data-ttu-id="21fbe-134">Microsoft. Azure. Commands. COMPUTE. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="21fbe-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="21fbe-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21fbe-135">NOTES</span></span>

## <span data-ttu-id="21fbe-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21fbe-136">RELATED LINKS</span></span>

[<span data-ttu-id="21fbe-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="21fbe-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="21fbe-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="21fbe-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


