---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111170"
---
# <span data-ttu-id="d74b3-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d74b3-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="d74b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d74b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d74b3-103">Guia de atualização de domínio manual para atualizar máquinas virtuais em um conjunto de escala de máquina virtual do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d74b3-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d74b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d74b3-104">SYNTAX</span></span>

### <span data-ttu-id="d74b3-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="d74b3-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d74b3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d74b3-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74b3-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d74b3-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74b3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d74b3-108">DESCRIPTION</span></span>
<span data-ttu-id="d74b3-109">Forçar atualização manual do domínio de atualização de plataforma para atualizar máquinas virtuais em um conjunto de escala de máquina virtual do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d74b3-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d74b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d74b3-110">EXAMPLES</span></span>

### <span data-ttu-id="d74b3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d74b3-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="d74b3-112">Esse comando força a movimentação de atualização do Service Fabric em UD 0 para o conjunto de escala de máquina virtual especificado pelo nome do grupo de recursos e pelo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="d74b3-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="d74b3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d74b3-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="d74b3-114">Esse comando força a movimentação de atualização do Service Fabric em UD 1 para o conjunto de escala da máquina virtual especificado pelo objeto do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="d74b3-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="d74b3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d74b3-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="d74b3-116">Esse comando força a movimentação de atualização do Service Fabric no UD 2 para o conjunto de escalas da máquina virtual especificado pela ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d74b3-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="d74b3-117">OS</span><span class="sxs-lookup"><span data-stu-id="d74b3-117">PARAMETERS</span></span>

### <span data-ttu-id="d74b3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74b3-118">-AsJob</span></span>
<span data-ttu-id="d74b3-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d74b3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74b3-120">-DefaultProfile</span></span>
<span data-ttu-id="d74b3-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d74b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74b3-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d74b3-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="d74b3-123">O domínio de atualização de plataforma para o qual um passeio de recuperação manual é solicitado.</span><span class="sxs-lookup"><span data-stu-id="d74b3-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="d74b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="d74b3-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d74b3-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d74b3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74b3-126">-ResourceId</span></span>
<span data-ttu-id="d74b3-127">A ID do recurso para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d74b3-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d74b3-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d74b3-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d74b3-129">Objeto do conjunto de escala da máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="d74b3-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="d74b3-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d74b3-130">-VMScaleSetName</span></span>
<span data-ttu-id="d74b3-131">O nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d74b3-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="d74b3-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d74b3-132">-Confirm</span></span>
<span data-ttu-id="d74b3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74b3-134">-WhatIf</span></span>
<span data-ttu-id="d74b3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d74b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74b3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d74b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74b3-137">CommonParameters</span></span>
<span data-ttu-id="d74b3-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74b3-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d74b3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74b3-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d74b3-140">INPUTS</span></span>

### <span data-ttu-id="d74b3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d74b3-141">System.String</span></span>

### <span data-ttu-id="d74b3-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d74b3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d74b3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d74b3-143">OUTPUTS</span></span>

### <span data-ttu-id="d74b3-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="d74b3-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="d74b3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d74b3-145">NOTES</span></span>

## <span data-ttu-id="d74b3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d74b3-146">RELATED LINKS</span></span>
