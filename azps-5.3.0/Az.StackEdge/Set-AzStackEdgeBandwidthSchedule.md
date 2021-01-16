---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264667"
---
# <span data-ttu-id="fa463-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fa463-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="fa463-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa463-102">SYNOPSIS</span></span>
<span data-ttu-id="fa463-103">Atualiza um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="fa463-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="fa463-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa463-104">SYNTAX</span></span>

### <span data-ttu-id="fa463-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa463-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa463-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa463-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa463-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa463-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fa463-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa463-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa463-114">DESCRIPTION</span></span>
<span data-ttu-id="fa463-115">O cmdlet **set-AzStackEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="fa463-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="fa463-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa463-116">EXAMPLES</span></span>

### <span data-ttu-id="fa463-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa463-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="fa463-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fa463-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="fa463-119">OS</span><span class="sxs-lookup"><span data-stu-id="fa463-119">PARAMETERS</span></span>

### <span data-ttu-id="fa463-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa463-120">-AsJob</span></span>
<span data-ttu-id="fa463-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fa463-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa463-122">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="fa463-122">-Bandwidth</span></span>
<span data-ttu-id="fa463-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="fa463-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="fa463-124">-DaysOfWeek</span></span>
<span data-ttu-id="fa463-125">DaysOfWeek programado</span><span class="sxs-lookup"><span data-stu-id="fa463-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa463-126">-DefaultProfile</span></span>
<span data-ttu-id="fa463-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa463-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa463-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fa463-128">-DeviceName</span></span>
<span data-ttu-id="fa463-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa463-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa463-130">-InputObject</span></span>
<span data-ttu-id="fa463-131">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="fa463-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa463-132">-Name</span></span>
<span data-ttu-id="fa463-133">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="fa463-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa463-134">-ResourceGroupName</span></span>
<span data-ttu-id="fa463-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fa463-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa463-136">-ResourceId</span></span>
<span data-ttu-id="fa463-137">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="fa463-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fa463-138">-StartTime</span></span>
<span data-ttu-id="fa463-139">Agendar hora de início</span><span class="sxs-lookup"><span data-stu-id="fa463-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="fa463-140">-StopTime</span></span>
<span data-ttu-id="fa463-141">Agendar hora de término</span><span class="sxs-lookup"><span data-stu-id="fa463-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="fa463-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="fa463-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="fa463-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa463-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa463-144">-Confirm</span></span>
<span data-ttu-id="fa463-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa463-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa463-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa463-146">-WhatIf</span></span>
<span data-ttu-id="fa463-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa463-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa463-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa463-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa463-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa463-149">CommonParameters</span></span>
<span data-ttu-id="fa463-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa463-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa463-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa463-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa463-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa463-152">INPUTS</span></span>

### <span data-ttu-id="fa463-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fa463-153">None</span></span>

## <span data-ttu-id="fa463-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa463-154">OUTPUTS</span></span>

### <span data-ttu-id="fa463-155">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fa463-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="fa463-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa463-156">NOTES</span></span>

## <span data-ttu-id="fa463-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa463-157">RELATED LINKS</span></span>
