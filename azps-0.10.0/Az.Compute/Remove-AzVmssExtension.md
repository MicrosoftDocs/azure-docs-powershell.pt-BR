---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776886"
---
# <span data-ttu-id="d97ad-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d97ad-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="d97ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d97ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d97ad-103">Remove uma extensão da VMSS.</span><span class="sxs-lookup"><span data-stu-id="d97ad-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="d97ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d97ad-104">SYNTAX</span></span>

### <span data-ttu-id="d97ad-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d97ad-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d97ad-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d97ad-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d97ad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d97ad-107">DESCRIPTION</span></span>
<span data-ttu-id="d97ad-108">O cmdlet **Remove-AzVmssExtension** remove uma extensão do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="d97ad-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d97ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d97ad-109">EXAMPLES</span></span>

### <span data-ttu-id="d97ad-110">Exemplo 1: remover a extensão da VMSS</span><span class="sxs-lookup"><span data-stu-id="d97ad-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="d97ad-111">OS</span><span class="sxs-lookup"><span data-stu-id="d97ad-111">PARAMETERS</span></span>

### <span data-ttu-id="d97ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97ad-112">-DefaultProfile</span></span>
<span data-ttu-id="d97ad-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d97ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97ad-114">-ID</span><span class="sxs-lookup"><span data-stu-id="d97ad-114">-Id</span></span>
<span data-ttu-id="d97ad-115">Especifica a ID da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="d97ad-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ad-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d97ad-116">-Name</span></span>
<span data-ttu-id="d97ad-117">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="d97ad-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97ad-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d97ad-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d97ad-119">Especifica o VMSS do qual a extensão será removida.</span><span class="sxs-lookup"><span data-stu-id="d97ad-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="d97ad-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d97ad-120">-Confirm</span></span>
<span data-ttu-id="d97ad-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d97ad-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97ad-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97ad-122">-WhatIf</span></span>
<span data-ttu-id="d97ad-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d97ad-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d97ad-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d97ad-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97ad-125">CommonParameters</span></span>
<span data-ttu-id="d97ad-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97ad-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97ad-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97ad-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d97ad-128">INPUTS</span></span>

### <span data-ttu-id="d97ad-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d97ad-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d97ad-130">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d97ad-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d97ad-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d97ad-131">OUTPUTS</span></span>

### <span data-ttu-id="d97ad-132">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d97ad-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d97ad-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d97ad-133">NOTES</span></span>

## <span data-ttu-id="d97ad-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d97ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="d97ad-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d97ad-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
