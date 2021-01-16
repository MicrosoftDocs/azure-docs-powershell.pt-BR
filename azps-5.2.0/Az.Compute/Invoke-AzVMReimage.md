---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263893"
---
# <span data-ttu-id="0da19-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0da19-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="0da19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0da19-102">SYNOPSIS</span></span>
<span data-ttu-id="0da19-103">Reimagem de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0da19-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="0da19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0da19-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0da19-105">DESCRIPTION</span></span>
<span data-ttu-id="0da19-106">O cmdlet **Invoke-AzVMReimage** reimagemia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0da19-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="0da19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0da19-107">EXAMPLES</span></span>

### <span data-ttu-id="0da19-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0da19-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0da19-109">Este comando reimagemia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0da19-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0da19-110">OS</span><span class="sxs-lookup"><span data-stu-id="0da19-110">PARAMETERS</span></span>

### <span data-ttu-id="0da19-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0da19-111">-AsJob</span></span>
<span data-ttu-id="0da19-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0da19-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0da19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da19-113">-DefaultProfile</span></span>
<span data-ttu-id="0da19-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0da19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da19-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da19-115">-ResourceGroupName</span></span>
<span data-ttu-id="0da19-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0da19-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0da19-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="0da19-117">-TempDisk</span></span>
<span data-ttu-id="0da19-118">Especifica se a reimagem do disco temporário será renovada.</span><span class="sxs-lookup"><span data-stu-id="0da19-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="0da19-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="0da19-119">-VMName</span></span>
<span data-ttu-id="0da19-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0da19-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="0da19-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0da19-121">-Confirm</span></span>
<span data-ttu-id="0da19-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da19-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da19-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da19-123">-WhatIf</span></span>
<span data-ttu-id="0da19-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0da19-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da19-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0da19-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da19-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da19-126">CommonParameters</span></span>
<span data-ttu-id="0da19-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da19-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da19-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da19-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da19-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0da19-129">INPUTS</span></span>

### <span data-ttu-id="0da19-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0da19-130">System.String</span></span>

## <span data-ttu-id="0da19-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0da19-131">OUTPUTS</span></span>

### <span data-ttu-id="0da19-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0da19-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0da19-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0da19-133">NOTES</span></span>

## <span data-ttu-id="0da19-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0da19-134">RELATED LINKS</span></span>
