---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111088"
---
# <span data-ttu-id="4bd1c-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="4bd1c-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="4bd1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd1c-103">Passo a passo manual de atualização de plataforma para atualizar máquinas virtuais em um conjunto de escala de máquina virtual de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="4bd1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bd1c-104">SYNTAX</span></span>

### <span data-ttu-id="4bd1c-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bd1c-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bd1c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4bd1c-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bd1c-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="4bd1c-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd1c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bd1c-108">DESCRIPTION</span></span>
<span data-ttu-id="4bd1c-109">Forçar a atualização manual do domínio da plataforma para atualizar máquinas virtuais em um conjunto de escala de máquina virtual de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="4bd1c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4bd1c-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bd1c-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="4bd1c-112">Esse comando força a atualização de malha de serviço no UD 0 para o conjunto de escala de máquina virtual especificado pelo nome do grupo de recursos e pelo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="4bd1c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bd1c-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="4bd1c-114">Esse comando força a atualização de malha de serviço no UD 1 para o conjunto de escala de máquina virtual especificado pelo objeto de conjunto de escala VM.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="4bd1c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4bd1c-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="4bd1c-116">Esse comando força a atualização de malha de serviço no UD 2 para o conjunto de escala de máquina virtual especificada pela ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="4bd1c-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bd1c-117">PARAMETERS</span></span>

### <span data-ttu-id="4bd1c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bd1c-118">-AsJob</span></span>
<span data-ttu-id="4bd1c-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4bd1c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bd1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd1c-120">-DefaultProfile</span></span>
<span data-ttu-id="4bd1c-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd1c-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="4bd1c-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="4bd1c-123">O domínio de atualização da plataforma para o qual uma recuperação manual é solicitada.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="4bd1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bd1c-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bd1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd1c-126">-ResourceId</span></span>
<span data-ttu-id="4bd1c-127">A ID do recurso para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4bd1c-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4bd1c-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4bd1c-129">Objeto de conjunto de escala de máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="4bd1c-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="4bd1c-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bd1c-130">-VMScaleSetName</span></span>
<span data-ttu-id="4bd1c-131">O nome do conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="4bd1c-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4bd1c-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4bd1c-132">-Confirm</span></span>
<span data-ttu-id="4bd1c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd1c-134">-WhatIf</span></span>
<span data-ttu-id="4bd1c-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd1c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bd1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd1c-137">CommonParameters</span></span>
<span data-ttu-id="4bd1c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd1c-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bd1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd1c-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="4bd1c-140">INPUTS</span></span>

### <span data-ttu-id="4bd1c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4bd1c-141">System.String</span></span>

### <span data-ttu-id="4bd1c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4bd1c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4bd1c-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="4bd1c-143">OUTPUTS</span></span>

### <span data-ttu-id="4bd1c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecovery AutomationResponse</span><span class="sxs-lookup"><span data-stu-id="4bd1c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="4bd1c-145">Notas</span><span class="sxs-lookup"><span data-stu-id="4bd1c-145">NOTES</span></span>

## <span data-ttu-id="4bd1c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bd1c-146">RELATED LINKS</span></span>
