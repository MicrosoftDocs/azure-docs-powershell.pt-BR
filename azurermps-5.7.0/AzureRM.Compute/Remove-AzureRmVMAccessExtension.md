---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429860"
---
# <span data-ttu-id="f51b6-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f51b6-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="f51b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f51b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f51b6-103">Remove a extensão VMAccess de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f51b6-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f51b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f51b6-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f51b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f51b6-105">DESCRIPTION</span></span>
<span data-ttu-id="f51b6-106">O cmdlet **Remove-AzureRmVMAccessExtension** remove a extensão da máquina virtual do VMAccess (acesso à máquina virtual) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f51b6-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="f51b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f51b6-107">EXAMPLES</span></span>

## <span data-ttu-id="f51b6-108">OS</span><span class="sxs-lookup"><span data-stu-id="f51b6-108">PARAMETERS</span></span>

### <span data-ttu-id="f51b6-109">-Force</span><span class="sxs-lookup"><span data-stu-id="f51b6-109">-Force</span></span>
<span data-ttu-id="f51b6-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f51b6-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51b6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="f51b6-111">-Name</span></span>
<span data-ttu-id="f51b6-112">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f51b6-112">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f51b6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f51b6-113">-ResourceGroupName</span></span>
<span data-ttu-id="f51b6-114">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f51b6-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f51b6-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="f51b6-115">-VMName</span></span>
<span data-ttu-id="f51b6-116">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f51b6-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f51b6-117">Esse cmdlet Remove VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f51b6-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f51b6-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f51b6-118">-Confirm</span></span>
<span data-ttu-id="f51b6-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f51b6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f51b6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f51b6-120">-WhatIf</span></span>
<span data-ttu-id="f51b6-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f51b6-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f51b6-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f51b6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f51b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51b6-123">CommonParameters</span></span>
<span data-ttu-id="f51b6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f51b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51b6-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51b6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f51b6-126">INPUTS</span></span>

### <span data-ttu-id="f51b6-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f51b6-127">None</span></span>
<span data-ttu-id="f51b6-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f51b6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f51b6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f51b6-129">OUTPUTS</span></span>

## <span data-ttu-id="f51b6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f51b6-130">NOTES</span></span>

## <span data-ttu-id="f51b6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f51b6-131">RELATED LINKS</span></span>

[<span data-ttu-id="f51b6-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f51b6-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f51b6-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f51b6-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="f51b6-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f51b6-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
