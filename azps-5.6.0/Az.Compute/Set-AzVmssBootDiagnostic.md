---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 58a45d6f9e3a24ca11c298935fc0d9676617737e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889688"
---
# <span data-ttu-id="bdb4c-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bdb4c-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="bdb4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb4c-103">Define o perfil de diagnóstico de inicialização do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="bdb4c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bdb4c-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb4c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bdb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb4c-106">Define o perfil de diagnóstico de inicialização do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="bdb4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb4c-108">Exemplo 1: definir a propriedade de perfil de diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="bdb4c-109">Este comando define a propriedade de perfil de diagnóstico de inicialização para a VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bdb4c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb4c-111">-DefaultProfile</span></span>
<span data-ttu-id="bdb4c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdb4c-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="bdb4c-113">-Enabled</span></span>
<span data-ttu-id="bdb4c-114">Se os diagnósticos de inicialização devem ser habilitados no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bdb4c-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="bdb4c-115">-StorageUri</span></span>
<span data-ttu-id="bdb4c-116">URI da conta de armazenamento a ser usada para colocar a saída do console e a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="bdb4c-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdb4c-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bdb4c-118">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="bdb4c-119">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bdb4c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdb4c-120">-Confirm</span></span>
<span data-ttu-id="bdb4c-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb4c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb4c-122">-WhatIf</span></span>
<span data-ttu-id="bdb4c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb4c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb4c-125">CommonParameters</span></span>
<span data-ttu-id="bdb4c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb4c-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb4c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb4c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-128">INPUTS</span></span>

### <span data-ttu-id="bdb4c-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdb4c-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bdb4c-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bdb4c-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bdb4c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bdb4c-131">System.String</span></span>

## <span data-ttu-id="bdb4c-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-132">OUTPUTS</span></span>

### <span data-ttu-id="bdb4c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bdb4c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bdb4c-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="bdb4c-134">NOTES</span></span>

## <span data-ttu-id="bdb4c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdb4c-135">RELATED LINKS</span></span>
