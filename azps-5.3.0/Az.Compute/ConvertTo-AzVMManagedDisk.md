---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430261"
---
# <span data-ttu-id="b54f2-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b54f2-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="b54f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b54f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b54f2-103">Converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="b54f2-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="b54f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b54f2-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b54f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b54f2-105">DESCRIPTION</span></span>
<span data-ttu-id="b54f2-106">O cmdlet **ConvertTo-AzVMManagedDisk** converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="b54f2-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="b54f2-107">A máquina virtual deve ser interrompida-desalocada antes de invocar essa operação.</span><span class="sxs-lookup"><span data-stu-id="b54f2-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="b54f2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b54f2-108">EXAMPLES</span></span>

### <span data-ttu-id="b54f2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b54f2-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="b54f2-110">Esse comando converte os discos baseados em BLOB da máquina virtual chamada "VM01" no grupo de recursos "ResourceGroup01" para discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="b54f2-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="b54f2-111">OS</span><span class="sxs-lookup"><span data-stu-id="b54f2-111">PARAMETERS</span></span>

### <span data-ttu-id="b54f2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b54f2-112">-AsJob</span></span>
<span data-ttu-id="b54f2-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b54f2-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b54f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54f2-114">-DefaultProfile</span></span>
<span data-ttu-id="b54f2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b54f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54f2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54f2-116">-ResourceGroupName</span></span>
<span data-ttu-id="b54f2-117">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b54f2-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54f2-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="b54f2-118">-VMName</span></span>
<span data-ttu-id="b54f2-119">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b54f2-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54f2-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b54f2-120">-Confirm</span></span>
<span data-ttu-id="b54f2-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b54f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b54f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b54f2-122">-WhatIf</span></span>
<span data-ttu-id="b54f2-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b54f2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b54f2-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b54f2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b54f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54f2-125">CommonParameters</span></span>
<span data-ttu-id="b54f2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54f2-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b54f2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54f2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b54f2-128">INPUTS</span></span>

### <span data-ttu-id="b54f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b54f2-129">System.String</span></span>

## <span data-ttu-id="b54f2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b54f2-130">OUTPUTS</span></span>

### <span data-ttu-id="b54f2-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b54f2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b54f2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b54f2-132">NOTES</span></span>

## <span data-ttu-id="b54f2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b54f2-133">RELATED LINKS</span></span>
