---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786129"
---
# <span data-ttu-id="40e08-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="40e08-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="40e08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40e08-102">SYNOPSIS</span></span>
<span data-ttu-id="40e08-103">Remove uma extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="40e08-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40e08-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40e08-105">DESCRIPTION</span></span>
<span data-ttu-id="40e08-106">O cmdlet **Remove-AzureRmVmssDiagnosticsExtension** remove uma extensão de diagnóstico do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="40e08-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="40e08-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40e08-107">EXAMPLES</span></span>

### <span data-ttu-id="40e08-108">Exemplo 1: remover uma extensão de diagnóstico do VMSS</span><span class="sxs-lookup"><span data-stu-id="40e08-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="40e08-109">Esse comando Remove a extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="40e08-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="40e08-110">OS</span><span class="sxs-lookup"><span data-stu-id="40e08-110">PARAMETERS</span></span>

### <span data-ttu-id="40e08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e08-111">-DefaultProfile</span></span>
<span data-ttu-id="40e08-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40e08-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e08-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="40e08-113">-Name</span></span>
<span data-ttu-id="40e08-114">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="40e08-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e08-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40e08-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="40e08-116">Especifica o VMSS a partir do qual a extensão deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="40e08-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="40e08-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40e08-117">-Confirm</span></span>
<span data-ttu-id="40e08-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e08-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e08-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e08-119">-WhatIf</span></span>
<span data-ttu-id="40e08-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40e08-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="40e08-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40e08-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e08-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e08-122">CommonParameters</span></span>
<span data-ttu-id="40e08-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e08-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e08-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e08-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e08-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40e08-125">INPUTS</span></span>

### <span data-ttu-id="40e08-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40e08-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="40e08-127">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="40e08-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="40e08-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40e08-128">OUTPUTS</span></span>

###  
<span data-ttu-id="40e08-129">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="40e08-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="40e08-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40e08-130">NOTES</span></span>

## <span data-ttu-id="40e08-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e08-131">RELATED LINKS</span></span>

[<span data-ttu-id="40e08-132">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="40e08-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="40e08-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="40e08-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="40e08-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="40e08-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


