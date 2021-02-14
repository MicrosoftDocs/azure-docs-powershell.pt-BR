---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116552"
---
# <span data-ttu-id="318cc-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="318cc-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="318cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="318cc-102">SYNOPSIS</span></span>
<span data-ttu-id="318cc-103">Converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="318cc-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="318cc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="318cc-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318cc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="318cc-105">DESCRIPTION</span></span>
<span data-ttu-id="318cc-106">O cmdlet **ConvertTo-AzVMManagedDisk** converte uma máquina virtual com discos baseados em blob em uma máquina virtual com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="318cc-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="318cc-107">A máquina virtual deve ser parada antes de revogar esta operação.</span><span class="sxs-lookup"><span data-stu-id="318cc-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="318cc-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="318cc-108">EXAMPLES</span></span>

### <span data-ttu-id="318cc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="318cc-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="318cc-110">Esse comando converte os discos baseados em blob da máquina virtual chamada 'VM01' no grupo de recursos 'ResourceGroup01' em discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="318cc-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="318cc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="318cc-111">PARAMETERS</span></span>

### <span data-ttu-id="318cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="318cc-112">-AsJob</span></span>
<span data-ttu-id="318cc-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="318cc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="318cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318cc-114">-DefaultProfile</span></span>
<span data-ttu-id="318cc-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="318cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="318cc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318cc-116">-ResourceGroupName</span></span>
<span data-ttu-id="318cc-117">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="318cc-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="318cc-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="318cc-118">-VMName</span></span>
<span data-ttu-id="318cc-119">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="318cc-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="318cc-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="318cc-120">-Confirm</span></span>
<span data-ttu-id="318cc-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318cc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318cc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318cc-122">-WhatIf</span></span>
<span data-ttu-id="318cc-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="318cc-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="318cc-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="318cc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318cc-125">CommonParameters</span></span>
<span data-ttu-id="318cc-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318cc-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="318cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318cc-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="318cc-128">INPUTS</span></span>

### <span data-ttu-id="318cc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="318cc-129">System.String</span></span>

## <span data-ttu-id="318cc-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="318cc-130">OUTPUTS</span></span>

### <span data-ttu-id="318cc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="318cc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="318cc-132">Notas</span><span class="sxs-lookup"><span data-stu-id="318cc-132">NOTES</span></span>

## <span data-ttu-id="318cc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318cc-133">RELATED LINKS</span></span>
