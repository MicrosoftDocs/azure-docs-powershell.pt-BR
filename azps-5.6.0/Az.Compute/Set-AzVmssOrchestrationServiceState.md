---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889354"
---
# <span data-ttu-id="b8582-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="b8582-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="b8582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8582-102">SYNOPSIS</span></span>
<span data-ttu-id="b8582-103">Define o estado do serviço de orquestração para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="b8582-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="b8582-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8582-104">SYNTAX</span></span>

### <span data-ttu-id="b8582-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8582-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8582-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b8582-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8582-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b8582-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8582-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8582-108">DESCRIPTION</span></span>
<span data-ttu-id="b8582-109">Define o estado do serviço de orquestração para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="b8582-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="b8582-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8582-110">EXAMPLES</span></span>

### <span data-ttu-id="b8582-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8582-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="b8582-112">Este comando suspende o serviço reparos automáticos no VMSS "vmss1" no grupo de recursos "rg".</span><span class="sxs-lookup"><span data-stu-id="b8582-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="b8582-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8582-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="b8582-114">Este comando retoma o serviço reparos automáticos no VMSS "vmss1" no grupo de recursos "rg".</span><span class="sxs-lookup"><span data-stu-id="b8582-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="b8582-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8582-115">PARAMETERS</span></span>

### <span data-ttu-id="b8582-116">-Action</span><span class="sxs-lookup"><span data-stu-id="b8582-116">-Action</span></span>
<span data-ttu-id="b8582-117">A ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="b8582-117">The action to be performed.</span></span>  <span data-ttu-id="b8582-118">Os valores possíveis são: Resume, Suspend.</span><span class="sxs-lookup"><span data-stu-id="b8582-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8582-119">-AsJob</span></span>
<span data-ttu-id="b8582-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8582-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8582-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8582-121">-DefaultProfile</span></span>
<span data-ttu-id="b8582-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8582-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8582-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8582-123">-InputObject</span></span>
<span data-ttu-id="b8582-124">O objeto local do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8582-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8582-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8582-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8582-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8582-127">-ResourceId</span></span>
<span data-ttu-id="b8582-128">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8582-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8582-129">-ServiceName</span></span>
<span data-ttu-id="b8582-130">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="b8582-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b8582-131">-VMScaleSetName</span></span>
<span data-ttu-id="b8582-132">O nome do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8582-132">The name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8582-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8582-133">-Confirm</span></span>
<span data-ttu-id="b8582-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8582-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8582-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8582-135">-WhatIf</span></span>
<span data-ttu-id="b8582-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8582-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8582-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8582-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8582-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8582-138">CommonParameters</span></span>
<span data-ttu-id="b8582-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8582-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8582-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8582-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8582-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8582-141">INPUTS</span></span>

### <span data-ttu-id="b8582-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b8582-142">System.String</span></span>

### <span data-ttu-id="b8582-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b8582-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b8582-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8582-144">OUTPUTS</span></span>

### <span data-ttu-id="b8582-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b8582-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b8582-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8582-146">NOTES</span></span>

## <span data-ttu-id="b8582-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8582-147">RELATED LINKS</span></span>
