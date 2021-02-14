---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116511"
---
# <span data-ttu-id="1c01d-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c01d-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="1c01d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c01d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c01d-103">Modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c01d-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1c01d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c01d-104">SYNTAX</span></span>

### <span data-ttu-id="1c01d-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1c01d-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c01d-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1c01d-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c01d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c01d-107">DESCRIPTION</span></span>
<span data-ttu-id="1c01d-108">O cmdlet **Set-AzVMBootDiagnostic** modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c01d-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1c01d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c01d-109">EXAMPLES</span></span>

### <span data-ttu-id="1c01d-110">Exemplo 1: Habilitar diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="1c01d-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="1c01d-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="1c01d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="1c01d-112">O comando o armazena na variável $VM dados.</span><span class="sxs-lookup"><span data-stu-id="1c01d-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="1c01d-113">O segundo comando habilita o diagnóstico de inicialização para a máquina virtual $VM.</span><span class="sxs-lookup"><span data-stu-id="1c01d-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="1c01d-114">Os dados de diagnóstico são armazenados na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="1c01d-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="1c01d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c01d-115">PARAMETERS</span></span>

### <span data-ttu-id="1c01d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c01d-116">-DefaultProfile</span></span>
<span data-ttu-id="1c01d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1c01d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c01d-118">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="1c01d-118">-Disable</span></span>
<span data-ttu-id="1c01d-119">Indica que esse cmdlet desabilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c01d-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c01d-120">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="1c01d-120">-Enable</span></span>
<span data-ttu-id="1c01d-121">Indica que esse cmdlet habilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c01d-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c01d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c01d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c01d-123">Especifica o nome do grupo de recursos da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1c01d-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c01d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c01d-124">-StorageAccountName</span></span>
<span data-ttu-id="1c01d-125">Especifica o nome da conta de armazenamento na qual você pode salvar dados de diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1c01d-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c01d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="1c01d-126">-VM</span></span>
<span data-ttu-id="1c01d-127">Especifica a máquina virtual para a qual este cmdlet altera o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1c01d-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="1c01d-128">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="1c01d-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c01d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c01d-129">CommonParameters</span></span>
<span data-ttu-id="1c01d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c01d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c01d-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c01d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c01d-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="1c01d-132">INPUTS</span></span>

### <span data-ttu-id="1c01d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1c01d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1c01d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1c01d-134">System.String</span></span>

## <span data-ttu-id="1c01d-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="1c01d-135">OUTPUTS</span></span>

### <span data-ttu-id="1c01d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1c01d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1c01d-137">Notas</span><span class="sxs-lookup"><span data-stu-id="1c01d-137">NOTES</span></span>

## <span data-ttu-id="1c01d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c01d-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c01d-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1c01d-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1c01d-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1c01d-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


