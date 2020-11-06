---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: e50b9b1a99c770ca8d9bb88c114a4c80f25283da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427255"
---
# <span data-ttu-id="7dedf-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7dedf-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="7dedf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="7dedf-103">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7dedf-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dedf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dedf-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dedf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dedf-105">DESCRIPTION</span></span>
<span data-ttu-id="7dedf-106">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7dedf-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="7dedf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dedf-107">EXAMPLES</span></span>

### <span data-ttu-id="7dedf-108">Exemplo 1: definir a propriedade de perfil do diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="7dedf-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="7dedf-109">Esse comando define a propriedade de perfil de diagnóstico de inicialização para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7dedf-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="7dedf-110">OS</span><span class="sxs-lookup"><span data-stu-id="7dedf-110">PARAMETERS</span></span>

### <span data-ttu-id="7dedf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dedf-111">-DefaultProfile</span></span>
<span data-ttu-id="7dedf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dedf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dedf-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="7dedf-113">-Enabled</span></span>
<span data-ttu-id="7dedf-114">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7dedf-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7dedf-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="7dedf-115">-StorageUri</span></span>
<span data-ttu-id="7dedf-116">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="7dedf-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="7dedf-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7dedf-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7dedf-118">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7dedf-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="7dedf-119">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="7dedf-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="7dedf-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7dedf-120">-Confirm</span></span>
<span data-ttu-id="7dedf-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dedf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dedf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dedf-122">-WhatIf</span></span>
<span data-ttu-id="7dedf-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7dedf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dedf-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dedf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dedf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dedf-125">CommonParameters</span></span>
<span data-ttu-id="7dedf-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dedf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dedf-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dedf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dedf-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dedf-128">INPUTS</span></span>

### <span data-ttu-id="7dedf-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7dedf-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7dedf-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7dedf-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7dedf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7dedf-131">System.String</span></span>

## <span data-ttu-id="7dedf-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dedf-132">OUTPUTS</span></span>

### <span data-ttu-id="7dedf-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7dedf-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7dedf-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dedf-134">NOTES</span></span>

## <span data-ttu-id="7dedf-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dedf-135">RELATED LINKS</span></span>
