---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115475"
---
# <span data-ttu-id="fa2bd-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="fa2bd-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="fa2bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2bd-103">Avaliar o estado de patch de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="fa2bd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa2bd-104">SYNTAX</span></span>

### <span data-ttu-id="fa2bd-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa2bd-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2bd-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2bd-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa2bd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2bd-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2bd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa2bd-108">DESCRIPTION</span></span>
<span data-ttu-id="fa2bd-109">Avalia o status de patch de um VM e relata todos os patches detectados que estão disponíveis para instalação.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="fa2bd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa2bd-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2bd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa2bd-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="fa2bd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa2bd-112">PARAMETERS</span></span>

### <span data-ttu-id="fa2bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa2bd-113">-AsJob</span></span>
<span data-ttu-id="fa2bd-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fa2bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa2bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2bd-115">-DefaultProfile</span></span>
<span data-ttu-id="fa2bd-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa2bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa2bd-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fa2bd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa2bd-119">-ResourceId</span></span>
<span data-ttu-id="fa2bd-120">ID do recurso para sua máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="fa2bd-121">-VM</span><span class="sxs-lookup"><span data-stu-id="fa2bd-121">-VM</span></span>
<span data-ttu-id="fa2bd-122">Objeto de máquina virtual do PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa2bd-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="fa2bd-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="fa2bd-123">-VMName</span></span>
<span data-ttu-id="fa2bd-124">Nome da Máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="fa2bd-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="fa2bd-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fa2bd-125">-Confirm</span></span>
<span data-ttu-id="fa2bd-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2bd-127">-WhatIf</span></span>
<span data-ttu-id="fa2bd-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa2bd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2bd-130">CommonParameters</span></span>
<span data-ttu-id="fa2bd-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2bd-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa2bd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2bd-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="fa2bd-133">INPUTS</span></span>

### <span data-ttu-id="fa2bd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fa2bd-134">System.String</span></span>

## <span data-ttu-id="fa2bd-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="fa2bd-135">OUTPUTS</span></span>

### <span data-ttu-id="fa2bd-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="fa2bd-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="fa2bd-137">Notas</span><span class="sxs-lookup"><span data-stu-id="fa2bd-137">NOTES</span></span>

## <span data-ttu-id="fa2bd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa2bd-138">RELATED LINKS</span></span>
