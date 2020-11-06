---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431048"
---
# <span data-ttu-id="3a80a-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3a80a-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="3a80a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a80a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a80a-103">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a80a-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a80a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a80a-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a80a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a80a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a80a-106">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a80a-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="3a80a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a80a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a80a-108">Exemplo 1: definir a propriedade de perfil do diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="3a80a-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="3a80a-109">Esse comando define a propriedade de perfil de diagnóstico de inicialização para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3a80a-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="3a80a-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a80a-110">PARAMETERS</span></span>

### <span data-ttu-id="3a80a-111">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="3a80a-111">-Enabled</span></span>
<span data-ttu-id="3a80a-112">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a80a-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3a80a-113">-StorageUri</span></span>
<span data-ttu-id="3a80a-114">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="3a80a-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a80a-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3a80a-116">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3a80a-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="3a80a-117">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3a80a-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a80a-118">-Confirm</span></span>
<span data-ttu-id="3a80a-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a80a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a80a-120">-WhatIf</span></span>
<span data-ttu-id="3a80a-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a80a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a80a-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a80a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a80a-123">CommonParameters</span></span>
<span data-ttu-id="3a80a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a80a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a80a-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a80a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a80a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a80a-126">INPUTS</span></span>

### <span data-ttu-id="3a80a-127">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a80a-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="3a80a-128">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="3a80a-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="3a80a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a80a-129">OUTPUTS</span></span>

### <span data-ttu-id="3a80a-130">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3a80a-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="3a80a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a80a-131">NOTES</span></span>

## <span data-ttu-id="3a80a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a80a-132">RELATED LINKS</span></span>

