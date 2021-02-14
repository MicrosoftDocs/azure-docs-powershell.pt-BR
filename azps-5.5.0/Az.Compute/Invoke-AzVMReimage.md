---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111144"
---
# <span data-ttu-id="4be12-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4be12-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="4be12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4be12-102">SYNOPSIS</span></span>
<span data-ttu-id="4be12-103">Reimage uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4be12-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="4be12-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4be12-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be12-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4be12-105">DESCRIPTION</span></span>
<span data-ttu-id="4be12-106">O cmdlet **Invoke-AzVMReimage** reimaima uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4be12-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="4be12-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4be12-107">EXAMPLES</span></span>

### <span data-ttu-id="4be12-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4be12-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4be12-109">Esse comando reimaja a máquina virtual chamada VirtualMachine07 no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4be12-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="4be12-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4be12-110">PARAMETERS</span></span>

### <span data-ttu-id="4be12-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4be12-111">-AsJob</span></span>
<span data-ttu-id="4be12-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4be12-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4be12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be12-113">-DefaultProfile</span></span>
<span data-ttu-id="4be12-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4be12-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be12-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be12-115">-ResourceGroupName</span></span>
<span data-ttu-id="4be12-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4be12-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4be12-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="4be12-117">-TempDisk</span></span>
<span data-ttu-id="4be12-118">Especifica se o disco temp deve ser reimado.</span><span class="sxs-lookup"><span data-stu-id="4be12-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="4be12-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="4be12-119">-VMName</span></span>
<span data-ttu-id="4be12-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4be12-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="4be12-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4be12-121">-Confirm</span></span>
<span data-ttu-id="4be12-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4be12-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be12-123">-WhatIf</span></span>
<span data-ttu-id="4be12-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4be12-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be12-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4be12-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be12-126">CommonParameters</span></span>
<span data-ttu-id="4be12-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be12-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4be12-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be12-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="4be12-129">INPUTS</span></span>

### <span data-ttu-id="4be12-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4be12-130">System.String</span></span>

## <span data-ttu-id="4be12-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="4be12-131">OUTPUTS</span></span>

### <span data-ttu-id="4be12-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4be12-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4be12-133">Notas</span><span class="sxs-lookup"><span data-stu-id="4be12-133">NOTES</span></span>

## <span data-ttu-id="4be12-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4be12-134">RELATED LINKS</span></span>
