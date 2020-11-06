---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4f69866d6301bc4efc0c867d35cdc7777e759ed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426958"
---
# <span data-ttu-id="c6942-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c6942-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="c6942-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6942-102">SYNOPSIS</span></span>
<span data-ttu-id="c6942-103">Remove uma extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6942-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6942-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6942-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6942-105">DESCRIPTION</span></span>
<span data-ttu-id="c6942-106">O cmdlet **Remove-AzureRmVmssDiagnosticsExtension** remove uma extensão de diagnóstico do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c6942-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c6942-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6942-107">EXAMPLES</span></span>

### <span data-ttu-id="c6942-108">Exemplo 1: remover uma extensão de diagnóstico do VMSS</span><span class="sxs-lookup"><span data-stu-id="c6942-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="c6942-109">Esse comando Remove a extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6942-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="c6942-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6942-110">PARAMETERS</span></span>

### <span data-ttu-id="c6942-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6942-111">-DefaultProfile</span></span>
<span data-ttu-id="c6942-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6942-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6942-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6942-113">-Name</span></span>
<span data-ttu-id="c6942-114">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="c6942-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6942-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c6942-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c6942-116">Especifica o VMSS a partir do qual a extensão deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="c6942-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6942-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6942-117">-Confirm</span></span>
<span data-ttu-id="c6942-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6942-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6942-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6942-119">-WhatIf</span></span>
<span data-ttu-id="c6942-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6942-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c6942-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6942-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6942-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6942-122">CommonParameters</span></span>
<span data-ttu-id="c6942-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6942-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6942-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6942-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6942-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6942-125">INPUTS</span></span>

## <span data-ttu-id="c6942-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6942-126">OUTPUTS</span></span>

###  
<span data-ttu-id="c6942-127">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c6942-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c6942-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6942-128">NOTES</span></span>

## <span data-ttu-id="c6942-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6942-129">RELATED LINKS</span></span>

[<span data-ttu-id="c6942-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c6942-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="c6942-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c6942-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="c6942-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c6942-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


