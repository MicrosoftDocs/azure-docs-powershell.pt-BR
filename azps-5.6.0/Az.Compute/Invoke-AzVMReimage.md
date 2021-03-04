---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 96560f393c361996ad906d1207647ba53f53cbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891870"
---
# <span data-ttu-id="aacaa-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="aacaa-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="aacaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aacaa-102">SYNOPSIS</span></span>
<span data-ttu-id="aacaa-103">Reimage uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="aacaa-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="aacaa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aacaa-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aacaa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aacaa-105">DESCRIPTION</span></span>
<span data-ttu-id="aacaa-106">O cmdlet **Invoke-AzVMReimage** reimages an Azure virtual machine.</span><span class="sxs-lookup"><span data-stu-id="aacaa-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="aacaa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aacaa-107">EXAMPLES</span></span>

### <span data-ttu-id="aacaa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aacaa-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="aacaa-109">Este comando reimaja a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="aacaa-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="aacaa-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aacaa-110">PARAMETERS</span></span>

### <span data-ttu-id="aacaa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aacaa-111">-AsJob</span></span>
<span data-ttu-id="aacaa-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aacaa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aacaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacaa-113">-DefaultProfile</span></span>
<span data-ttu-id="aacaa-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aacaa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacaa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aacaa-115">-ResourceGroupName</span></span>
<span data-ttu-id="aacaa-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aacaa-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aacaa-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="aacaa-117">-TempDisk</span></span>
<span data-ttu-id="aacaa-118">Especifica se o disco temporário deve ser reimageado.</span><span class="sxs-lookup"><span data-stu-id="aacaa-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="aacaa-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="aacaa-119">-VMName</span></span>
<span data-ttu-id="aacaa-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aacaa-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="aacaa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aacaa-121">-Confirm</span></span>
<span data-ttu-id="aacaa-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aacaa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aacaa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aacaa-123">-WhatIf</span></span>
<span data-ttu-id="aacaa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aacaa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aacaa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aacaa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aacaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacaa-126">CommonParameters</span></span>
<span data-ttu-id="aacaa-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacaa-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aacaa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacaa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aacaa-129">INPUTS</span></span>

### <span data-ttu-id="aacaa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="aacaa-130">System.String</span></span>

## <span data-ttu-id="aacaa-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aacaa-131">OUTPUTS</span></span>

### <span data-ttu-id="aacaa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="aacaa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="aacaa-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="aacaa-133">NOTES</span></span>

## <span data-ttu-id="aacaa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aacaa-134">RELATED LINKS</span></span>
