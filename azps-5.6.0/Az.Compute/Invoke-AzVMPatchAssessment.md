---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889565"
---
# <span data-ttu-id="d4e0f-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="d4e0f-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="d4e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e0f-103">Avalie o estado de patch de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="d4e0f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4e0f-104">SYNTAX</span></span>

### <span data-ttu-id="d4e0f-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4e0f-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e0f-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e0f-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e0f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4e0f-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e0f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4e0f-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e0f-109">Avalia o status do patch de uma VM e relata todos os patches detectados que estão disponíveis para instalação.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="d4e0f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e0f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4e0f-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="d4e0f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-112">PARAMETERS</span></span>

### <span data-ttu-id="d4e0f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4e0f-113">-AsJob</span></span>
<span data-ttu-id="d4e0f-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d4e0f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4e0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e0f-115">-DefaultProfile</span></span>
<span data-ttu-id="d4e0f-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4e0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4e0f-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4e0f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e0f-119">-ResourceId</span></span>
<span data-ttu-id="d4e0f-120">ID de recurso para sua máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="d4e0f-121">-VM</span><span class="sxs-lookup"><span data-stu-id="d4e0f-121">-VM</span></span>
<span data-ttu-id="d4e0f-122">Objeto da máquina virtual do PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4e0f-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="d4e0f-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4e0f-123">-VMName</span></span>
<span data-ttu-id="d4e0f-124">Nome da Máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="d4e0f-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="d4e0f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4e0f-125">-Confirm</span></span>
<span data-ttu-id="d4e0f-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e0f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e0f-127">-WhatIf</span></span>
<span data-ttu-id="d4e0f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4e0f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e0f-130">CommonParameters</span></span>
<span data-ttu-id="d4e0f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e0f-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4e0f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e0f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-133">INPUTS</span></span>

### <span data-ttu-id="d4e0f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d4e0f-134">System.String</span></span>

## <span data-ttu-id="d4e0f-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-135">OUTPUTS</span></span>

### <span data-ttu-id="d4e0f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="d4e0f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="d4e0f-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4e0f-137">NOTES</span></span>

## <span data-ttu-id="d4e0f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4e0f-138">RELATED LINKS</span></span>
