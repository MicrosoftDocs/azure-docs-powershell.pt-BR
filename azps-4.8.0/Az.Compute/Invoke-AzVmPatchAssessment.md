---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111179"
---
# <span data-ttu-id="e0d20-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="e0d20-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="e0d20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0d20-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d20-103">Avaliar o estado do patch de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e0d20-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="e0d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0d20-104">SYNTAX</span></span>

### <span data-ttu-id="e0d20-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0d20-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0d20-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0d20-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0d20-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0d20-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d20-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0d20-108">DESCRIPTION</span></span>
<span data-ttu-id="e0d20-109">Avalia o status do patch de uma VM e relata todos os patches detectados que estão disponíveis para instalação.</span><span class="sxs-lookup"><span data-stu-id="e0d20-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="e0d20-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0d20-110">EXAMPLES</span></span>

### <span data-ttu-id="e0d20-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0d20-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="e0d20-112">OS</span><span class="sxs-lookup"><span data-stu-id="e0d20-112">PARAMETERS</span></span>

### <span data-ttu-id="e0d20-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0d20-113">-AsJob</span></span>
<span data-ttu-id="e0d20-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e0d20-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0d20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d20-115">-DefaultProfile</span></span>
<span data-ttu-id="e0d20-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0d20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d20-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0d20-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0d20-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d20-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0d20-119">-ResourceId</span></span>
<span data-ttu-id="e0d20-120">ID do recurso para sua máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e0d20-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d20-121">-VM</span><span class="sxs-lookup"><span data-stu-id="e0d20-121">-VM</span></span>
<span data-ttu-id="e0d20-122">Objeto da máquina virtual do PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0d20-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d20-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="e0d20-123">-VMName</span></span>
<span data-ttu-id="e0d20-124">Nome da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e0d20-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d20-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0d20-125">-Confirm</span></span>
<span data-ttu-id="e0d20-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0d20-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d20-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d20-127">-WhatIf</span></span>
<span data-ttu-id="e0d20-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0d20-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0d20-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0d20-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d20-130">CommonParameters</span></span>
<span data-ttu-id="e0d20-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d20-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0d20-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d20-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0d20-133">INPUTS</span></span>

### <span data-ttu-id="e0d20-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0d20-134">System.String</span></span>

## <span data-ttu-id="e0d20-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0d20-135">OUTPUTS</span></span>

### <span data-ttu-id="e0d20-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="e0d20-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="e0d20-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0d20-137">NOTES</span></span>

## <span data-ttu-id="e0d20-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0d20-138">RELATED LINKS</span></span>
