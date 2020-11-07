---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 407119856fa670bc4561e06adae32ee806437b1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771112"
---
# <span data-ttu-id="1f362-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1f362-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="1f362-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f362-102">SYNOPSIS</span></span>
<span data-ttu-id="1f362-103">Modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f362-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1f362-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f362-104">SYNTAX</span></span>

### <span data-ttu-id="1f362-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1f362-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f362-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1f362-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f362-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f362-107">DESCRIPTION</span></span>
<span data-ttu-id="1f362-108">O cmdlet **set-AzVMBootDiagnostic** modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f362-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="1f362-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f362-109">EXAMPLES</span></span>

### <span data-ttu-id="1f362-110">Exemplo 1: habilitar o diagnóstico de inicialização</span><span class="sxs-lookup"><span data-stu-id="1f362-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="1f362-111">O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="1f362-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="1f362-112">O comando o armazena na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="1f362-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="1f362-113">O segundo comando habilita o diagnóstico de inicialização para a máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="1f362-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="1f362-114">Os dados de diagnóstico são armazenados na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="1f362-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="1f362-115">OS</span><span class="sxs-lookup"><span data-stu-id="1f362-115">PARAMETERS</span></span>

### <span data-ttu-id="1f362-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f362-116">-DefaultProfile</span></span>
<span data-ttu-id="1f362-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f362-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f362-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="1f362-118">-Disable</span></span>
<span data-ttu-id="1f362-119">Indica que esse cmdlet desabilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f362-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="1f362-120">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="1f362-120">-Enable</span></span>
<span data-ttu-id="1f362-121">Indica que esse cmdlet habilita o diagnóstico de inicialização para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f362-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="1f362-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f362-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f362-123">Especifica o nome do grupo de recursos da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1f362-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="1f362-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f362-124">-StorageAccountName</span></span>
<span data-ttu-id="1f362-125">Especifica o nome da conta de armazenamento na qual os dados de diagnóstico de inicialização são salvos.</span><span class="sxs-lookup"><span data-stu-id="1f362-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="1f362-126">-VM</span><span class="sxs-lookup"><span data-stu-id="1f362-126">-VM</span></span>
<span data-ttu-id="1f362-127">Especifica a máquina virtual para a qual esse cmdlet altera o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="1f362-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="1f362-128">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1f362-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1f362-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f362-129">CommonParameters</span></span>
<span data-ttu-id="1f362-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f362-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f362-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f362-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f362-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f362-132">INPUTS</span></span>

### <span data-ttu-id="1f362-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1f362-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1f362-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f362-134">System.String</span></span>

## <span data-ttu-id="1f362-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f362-135">OUTPUTS</span></span>

### <span data-ttu-id="1f362-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1f362-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1f362-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f362-137">NOTES</span></span>

## <span data-ttu-id="1f362-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f362-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f362-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1f362-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1f362-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1f362-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


