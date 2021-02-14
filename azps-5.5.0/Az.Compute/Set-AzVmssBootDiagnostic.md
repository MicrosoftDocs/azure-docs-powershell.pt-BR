---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115955"
---
# <span data-ttu-id="25f0a-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="25f0a-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="25f0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="25f0a-103">Define o perfil de diagnóstico de inicialização de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25f0a-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="25f0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f0a-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f0a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="25f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="25f0a-106">Define o perfil de diagnóstico de inicialização de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25f0a-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="25f0a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25f0a-107">EXAMPLES</span></span>

### <span data-ttu-id="25f0a-108">Exemplo 1: Definir a propriedade de perfil de diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="25f0a-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="25f0a-109">Esse comando define a propriedade de perfil de diagnóstico de inicialização para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="25f0a-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="25f0a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25f0a-110">PARAMETERS</span></span>

### <span data-ttu-id="25f0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f0a-111">-DefaultProfile</span></span>
<span data-ttu-id="25f0a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="25f0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f0a-113">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="25f0a-113">-Enabled</span></span>
<span data-ttu-id="25f0a-114">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25f0a-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f0a-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="25f0a-115">-StorageUri</span></span>
<span data-ttu-id="25f0a-116">URI da conta de armazenamento a ser usada para colocar a saída do console e a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="25f0a-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="25f0a-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25f0a-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="25f0a-118">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="25f0a-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="25f0a-119">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="25f0a-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25f0a-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="25f0a-120">-Confirm</span></span>
<span data-ttu-id="25f0a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25f0a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f0a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f0a-122">-WhatIf</span></span>
<span data-ttu-id="25f0a-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="25f0a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f0a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25f0a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f0a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f0a-125">CommonParameters</span></span>
<span data-ttu-id="25f0a-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f0a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f0a-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25f0a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f0a-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="25f0a-128">INPUTS</span></span>

### <span data-ttu-id="25f0a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25f0a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="25f0a-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="25f0a-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="25f0a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="25f0a-131">System.String</span></span>

## <span data-ttu-id="25f0a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="25f0a-132">OUTPUTS</span></span>

### <span data-ttu-id="25f0a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25f0a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="25f0a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="25f0a-134">NOTES</span></span>

## <span data-ttu-id="25f0a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25f0a-135">RELATED LINKS</span></span>
