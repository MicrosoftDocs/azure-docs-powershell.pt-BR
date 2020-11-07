---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785266"
---
# <span data-ttu-id="25570-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="25570-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="25570-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25570-102">SYNOPSIS</span></span>
<span data-ttu-id="25570-103">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25570-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25570-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25570-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25570-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25570-105">DESCRIPTION</span></span>
<span data-ttu-id="25570-106">Define o perfil de diagnóstico de inicialização do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25570-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="25570-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25570-107">EXAMPLES</span></span>

### <span data-ttu-id="25570-108">Exemplo 1: definir a propriedade de perfil do diagnóstico de inicialização para um VMSS</span><span class="sxs-lookup"><span data-stu-id="25570-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="25570-109">Esse comando define a propriedade de perfil de diagnóstico de inicialização para o VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="25570-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="25570-110">OS</span><span class="sxs-lookup"><span data-stu-id="25570-110">PARAMETERS</span></span>

### <span data-ttu-id="25570-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25570-111">-DefaultProfile</span></span>
<span data-ttu-id="25570-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25570-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25570-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="25570-113">-Enabled</span></span>
<span data-ttu-id="25570-114">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="25570-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="25570-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="25570-115">-StorageUri</span></span>
<span data-ttu-id="25570-116">URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.</span><span class="sxs-lookup"><span data-stu-id="25570-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="25570-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25570-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="25570-118">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="25570-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="25570-119">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="25570-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25570-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25570-120">-Confirm</span></span>
<span data-ttu-id="25570-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25570-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25570-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25570-122">-WhatIf</span></span>
<span data-ttu-id="25570-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25570-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25570-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25570-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25570-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25570-125">CommonParameters</span></span>
<span data-ttu-id="25570-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25570-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25570-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25570-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25570-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25570-128">INPUTS</span></span>

### <span data-ttu-id="25570-129">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25570-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="25570-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="25570-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="25570-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25570-131">OUTPUTS</span></span>

### <span data-ttu-id="25570-132">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25570-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="25570-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25570-133">NOTES</span></span>

## <span data-ttu-id="25570-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25570-134">RELATED LINKS</span></span>

