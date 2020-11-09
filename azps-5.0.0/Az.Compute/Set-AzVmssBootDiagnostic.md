---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280377"
---
# <span data-ttu-id="bac8b-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bac8b-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="bac8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bac8b-102">SYNOPSIS</span></span>
<span data-ttu-id="bac8b-103">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bac8b-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="bac8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bac8b-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bac8b-105">DESCRIPTION</span></span>
<span data-ttu-id="bac8b-106">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bac8b-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="bac8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bac8b-107">EXAMPLES</span></span>

### <span data-ttu-id="bac8b-108">Exemplo 1: definir a propriedade de perfil do diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="bac8b-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="bac8b-109">Esse comando define a propriedade de perfil de diagnóstico de inicialização para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bac8b-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bac8b-110">OS</span><span class="sxs-lookup"><span data-stu-id="bac8b-110">PARAMETERS</span></span>

### <span data-ttu-id="bac8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac8b-111">-DefaultProfile</span></span>
<span data-ttu-id="bac8b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bac8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac8b-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="bac8b-113">-Enabled</span></span>
<span data-ttu-id="bac8b-114">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bac8b-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bac8b-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="bac8b-115">-StorageUri</span></span>
<span data-ttu-id="bac8b-116">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="bac8b-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="bac8b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bac8b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bac8b-118">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bac8b-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="bac8b-119">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="bac8b-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bac8b-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bac8b-120">-Confirm</span></span>
<span data-ttu-id="bac8b-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac8b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac8b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac8b-122">-WhatIf</span></span>
<span data-ttu-id="bac8b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bac8b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac8b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bac8b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac8b-125">CommonParameters</span></span>
<span data-ttu-id="bac8b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac8b-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bac8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac8b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bac8b-128">INPUTS</span></span>

### <span data-ttu-id="bac8b-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bac8b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bac8b-130">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bac8b-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bac8b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bac8b-131">System.String</span></span>

## <span data-ttu-id="bac8b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bac8b-132">OUTPUTS</span></span>

### <span data-ttu-id="bac8b-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bac8b-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bac8b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bac8b-134">NOTES</span></span>

## <span data-ttu-id="bac8b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bac8b-135">RELATED LINKS</span></span>
