---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: e0edd9ad095f6f7887e0e3f4951828844d2521c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885884"
---
# <span data-ttu-id="367f5-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="367f5-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="367f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="367f5-102">SYNOPSIS</span></span>
<span data-ttu-id="367f5-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span><span class="sxs-lookup"><span data-stu-id="367f5-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="367f5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="367f5-104">SYNTAX</span></span>

### <span data-ttu-id="367f5-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="367f5-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="367f5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="367f5-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367f5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="367f5-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367f5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="367f5-108">DESCRIPTION</span></span>
<span data-ttu-id="367f5-109">Force o domínio de atualização manual da plataforma para atualizar máquinas virtuais em um conjunto de escala de máquina virtual de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="367f5-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="367f5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="367f5-110">EXAMPLES</span></span>

### <span data-ttu-id="367f5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="367f5-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="367f5-112">Este comando força a atualização de malha de serviço a andar na UD 0 para o conjunto de escala de máquina virtual especificado pelo nome do grupo de recursos e o nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="367f5-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="367f5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="367f5-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="367f5-114">Este comando força a atualização de malha de serviço a andar na UD 1 para o conjunto de escala de máquina virtual especificado pelo objeto de conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="367f5-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="367f5-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="367f5-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="367f5-116">Este comando força a atualização de malha de serviço a andar na UD 2 para o conjunto de escala de máquina virtual especificado pela id de recurso.</span><span class="sxs-lookup"><span data-stu-id="367f5-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="367f5-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="367f5-117">PARAMETERS</span></span>

### <span data-ttu-id="367f5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="367f5-118">-AsJob</span></span>
<span data-ttu-id="367f5-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="367f5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="367f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367f5-120">-DefaultProfile</span></span>
<span data-ttu-id="367f5-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="367f5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="367f5-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="367f5-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="367f5-123">O domínio de atualização da plataforma para o qual uma caminhada de recuperação manual é solicitada.</span><span class="sxs-lookup"><span data-stu-id="367f5-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="367f5-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="367f5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="367f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="367f5-126">-ResourceId</span></span>
<span data-ttu-id="367f5-127">A ID do recurso para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="367f5-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="367f5-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="367f5-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="367f5-129">Objeto de conjunto de escala de máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="367f5-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="367f5-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="367f5-130">-VMScaleSetName</span></span>
<span data-ttu-id="367f5-131">O nome do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="367f5-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="367f5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="367f5-132">-Confirm</span></span>
<span data-ttu-id="367f5-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367f5-134">-WhatIf</span></span>
<span data-ttu-id="367f5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="367f5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367f5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="367f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367f5-137">CommonParameters</span></span>
<span data-ttu-id="367f5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367f5-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="367f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367f5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="367f5-140">INPUTS</span></span>

### <span data-ttu-id="367f5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="367f5-141">System.String</span></span>

### <span data-ttu-id="367f5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="367f5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="367f5-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="367f5-143">OUTPUTS</span></span>

### <span data-ttu-id="367f5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="367f5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="367f5-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="367f5-145">NOTES</span></span>

## <span data-ttu-id="367f5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="367f5-146">RELATED LINKS</span></span>
