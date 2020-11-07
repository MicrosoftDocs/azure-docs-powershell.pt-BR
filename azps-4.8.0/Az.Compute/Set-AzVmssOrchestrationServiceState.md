---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955949"
---
# <span data-ttu-id="9b7c4-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="9b7c4-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="9b7c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7c4-103">Define o estado do serviço de orquestração para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="9b7c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b7c4-104">SYNTAX</span></span>

### <span data-ttu-id="9b7c4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b7c4-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7c4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9b7c4-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7c4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9b7c4-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b7c4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b7c4-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7c4-109">Define o estado do serviço de orquestração para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="9b7c4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b7c4-110">EXAMPLES</span></span>

### <span data-ttu-id="9b7c4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b7c4-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="9b7c4-112">Esse comando suspende o serviço de reparos automáticos no VMSS "vmss1" no grupo de recursos "RG".</span><span class="sxs-lookup"><span data-stu-id="9b7c4-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="9b7c4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b7c4-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="9b7c4-114">Este comando retoma o serviço de reparos automáticos no VMSS "vmss1" no grupo de recursos "RG".</span><span class="sxs-lookup"><span data-stu-id="9b7c4-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="9b7c4-115">OS</span><span class="sxs-lookup"><span data-stu-id="9b7c4-115">PARAMETERS</span></span>

### <span data-ttu-id="9b7c4-116">-Ação</span><span class="sxs-lookup"><span data-stu-id="9b7c4-116">-Action</span></span>
<span data-ttu-id="9b7c4-117">A ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-117">The action to be performed.</span></span>  <span data-ttu-id="9b7c4-118">Os valores possíveis são: retomar, suspender.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-118">Possible values are: Resume, Suspend.</span></span>

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

### <span data-ttu-id="9b7c4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b7c4-119">-AsJob</span></span>
<span data-ttu-id="9b7c4-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b7c4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b7c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7c4-121">-DefaultProfile</span></span>
<span data-ttu-id="9b7c4-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b7c4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b7c4-123">-InputObject</span></span>
<span data-ttu-id="9b7c4-124">O objeto local do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9b7c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b7c4-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b7c4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b7c4-127">-ResourceId</span></span>
<span data-ttu-id="9b7c4-128">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="9b7c4-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9b7c4-129">-ServiceName</span></span>
<span data-ttu-id="9b7c4-130">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-130">The name of the service.</span></span>

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

### <span data-ttu-id="9b7c4-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9b7c4-131">-VMScaleSetName</span></span>
<span data-ttu-id="9b7c4-132">O nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9b7c4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b7c4-133">-Confirm</span></span>
<span data-ttu-id="9b7c4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7c4-135">-WhatIf</span></span>
<span data-ttu-id="9b7c4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b7c4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7c4-138">CommonParameters</span></span>
<span data-ttu-id="9b7c4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7c4-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b7c4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7c4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b7c4-141">INPUTS</span></span>

### <span data-ttu-id="9b7c4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9b7c4-142">System.String</span></span>

### <span data-ttu-id="9b7c4-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9b7c4-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9b7c4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b7c4-144">OUTPUTS</span></span>

### <span data-ttu-id="9b7c4-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9b7c4-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9b7c4-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b7c4-146">NOTES</span></span>

## <span data-ttu-id="9b7c4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b7c4-147">RELATED LINKS</span></span>
