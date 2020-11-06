---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/repair-azurermvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Repair-AzureRmVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Repair-AzureRmVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 73dd0ec70f2a39f9d96625e8ac5685301b38176f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427257"
---
# <span data-ttu-id="c0043-101">Repair-AzureRmVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c0043-101">Repair-AzureRmVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="c0043-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0043-102">SYNOPSIS</span></span>
<span data-ttu-id="c0043-103">Guia de atualização de domínio manual para atualizar máquinas virtuais em um conjunto de escala de máquina virtual do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c0043-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0043-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0043-104">SYNTAX</span></span>

### <span data-ttu-id="c0043-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0043-105">DefaultParameter (Default)</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0043-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c0043-106">ResourceIdParameter</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0043-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c0043-107">ObjectParameter</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0043-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0043-108">DESCRIPTION</span></span>
<span data-ttu-id="c0043-109">Forçar atualização manual do domínio de atualização de plataforma para atualizar máquinas virtuais em um conjunto de escala de máquina virtual do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c0043-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="c0043-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0043-110">EXAMPLES</span></span>

### <span data-ttu-id="c0043-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0043-111">Example 1</span></span>
```
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="c0043-112">Esse comando força a movimentação de atualização do Service Fabric em UD 0 para o conjunto de escala de máquina virtual especificado pelo nome do grupo de recursos e pelo nome do conjunto de escala.</span><span class="sxs-lookup"><span data-stu-id="c0043-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="c0043-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0043-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="c0043-114">Esse comando força a movimentação de atualização do Service Fabric em UD 1 para o conjunto de escala da máquina virtual especificado pelo objeto do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="c0043-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="c0043-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c0043-115">Example 3</span></span>
```
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -ResourceId $resoureId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="c0043-116">Esse comando força a movimentação de atualização do Service Fabric no UD 2 para o conjunto de escalas da máquina virtual especificado pela ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0043-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="c0043-117">OS</span><span class="sxs-lookup"><span data-stu-id="c0043-117">PARAMETERS</span></span>

### <span data-ttu-id="c0043-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0043-118">-AsJob</span></span>
<span data-ttu-id="c0043-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c0043-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0043-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0043-120">-DefaultProfile</span></span>
<span data-ttu-id="c0043-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0043-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0043-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c0043-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="c0043-123">O domínio de atualização de plataforma para o qual um passeio de recuperação manual é solicitado.</span><span class="sxs-lookup"><span data-stu-id="c0043-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0043-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0043-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0043-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0043-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0043-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0043-126">-ResourceId</span></span>
<span data-ttu-id="c0043-127">A ID do recurso para o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c0043-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c0043-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c0043-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c0043-129">Objeto do conjunto de escala da máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="c0043-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="c0043-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c0043-130">-VMScaleSetName</span></span>
<span data-ttu-id="c0043-131">O nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c0043-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0043-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0043-132">-Confirm</span></span>
<span data-ttu-id="c0043-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0043-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0043-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0043-134">-WhatIf</span></span>
<span data-ttu-id="c0043-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0043-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0043-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0043-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0043-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0043-137">CommonParameters</span></span>
<span data-ttu-id="c0043-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0043-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0043-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0043-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0043-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0043-140">INPUTS</span></span>

### <span data-ttu-id="c0043-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c0043-141">System.String</span></span>

### <span data-ttu-id="c0043-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c0043-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="c0043-143">Parâmetros: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0043-143">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="c0043-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0043-144">OUTPUTS</span></span>

### <span data-ttu-id="c0043-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="c0043-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="c0043-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0043-146">NOTES</span></span>

## <span data-ttu-id="c0043-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0043-147">RELATED LINKS</span></span>