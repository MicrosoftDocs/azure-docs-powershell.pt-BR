---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440512"
---
# <span data-ttu-id="e91c2-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e91c2-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="e91c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e91c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e91c2-103">Converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e91c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e91c2-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e91c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e91c2-105">DESCRIPTION</span></span>
<span data-ttu-id="e91c2-106">O cmdlet **ConvertTo-AzureRmVMManagedDisk** converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="e91c2-107">A máquina virtual deve ser interrompida-desalocada antes de invocar essa operação.</span><span class="sxs-lookup"><span data-stu-id="e91c2-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="e91c2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e91c2-108">EXAMPLES</span></span>

### <span data-ttu-id="e91c2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e91c2-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="e91c2-110">Esse comando converte os discos baseados em BLOB da máquina virtual chamada "VM01" no grupo de recursos "ResourceGroup01" para discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e91c2-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="e91c2-111">OS</span><span class="sxs-lookup"><span data-stu-id="e91c2-111">PARAMETERS</span></span>

### <span data-ttu-id="e91c2-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e91c2-112">-ResourceGroupName</span></span>
<span data-ttu-id="e91c2-113">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e91c2-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91c2-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="e91c2-114">-VMName</span></span>
<span data-ttu-id="e91c2-115">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e91c2-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91c2-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e91c2-116">-Confirm</span></span>
<span data-ttu-id="e91c2-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91c2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91c2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91c2-118">-WhatIf</span></span>
<span data-ttu-id="e91c2-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e91c2-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e91c2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e91c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91c2-121">CommonParameters</span></span>
<span data-ttu-id="e91c2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91c2-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91c2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91c2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e91c2-124">INPUTS</span></span>

### <span data-ttu-id="e91c2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e91c2-125">System.String</span></span>

## <span data-ttu-id="e91c2-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e91c2-126">OUTPUTS</span></span>

### <span data-ttu-id="e91c2-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="e91c2-127">System.Object</span></span>

## <span data-ttu-id="e91c2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e91c2-128">NOTES</span></span>

## <span data-ttu-id="e91c2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e91c2-129">RELATED LINKS</span></span>

