---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262436"
---
# <span data-ttu-id="fd13d-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fd13d-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="fd13d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd13d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd13d-103">Atualiza um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="fd13d-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="fd13d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd13d-104">SYNTAX</span></span>

### <span data-ttu-id="fd13d-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd13d-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd13d-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd13d-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="fd13d-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd13d-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd13d-114">DESCRIPTION</span></span>
<span data-ttu-id="fd13d-115">O cmdlet **set-AzStackEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="fd13d-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="fd13d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd13d-116">EXAMPLES</span></span>

### <span data-ttu-id="fd13d-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd13d-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="fd13d-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd13d-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="fd13d-119">OS</span><span class="sxs-lookup"><span data-stu-id="fd13d-119">PARAMETERS</span></span>

### <span data-ttu-id="fd13d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd13d-120">-AsJob</span></span>
<span data-ttu-id="fd13d-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fd13d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd13d-122">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="fd13d-122">-Bandwidth</span></span>
<span data-ttu-id="fd13d-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="fd13d-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="fd13d-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="fd13d-124">-DaysOfWeek</span></span>
<span data-ttu-id="fd13d-125">DaysOfWeek programado</span><span class="sxs-lookup"><span data-stu-id="fd13d-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="fd13d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd13d-126">-DefaultProfile</span></span>
<span data-ttu-id="fd13d-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd13d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd13d-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fd13d-128">-DeviceName</span></span>
<span data-ttu-id="fd13d-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fd13d-129">Device Name</span></span>

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

### <span data-ttu-id="fd13d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd13d-130">-InputObject</span></span>
<span data-ttu-id="fd13d-131">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="fd13d-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="fd13d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd13d-132">-Name</span></span>
<span data-ttu-id="fd13d-133">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="fd13d-133">Resource Name</span></span>

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

### <span data-ttu-id="fd13d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd13d-134">-ResourceGroupName</span></span>
<span data-ttu-id="fd13d-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fd13d-135">Resource Group Name</span></span>

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

### <span data-ttu-id="fd13d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd13d-136">-ResourceId</span></span>
<span data-ttu-id="fd13d-137">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="fd13d-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="fd13d-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fd13d-138">-StartTime</span></span>
<span data-ttu-id="fd13d-139">Agendar hora de início</span><span class="sxs-lookup"><span data-stu-id="fd13d-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="fd13d-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="fd13d-140">-StopTime</span></span>
<span data-ttu-id="fd13d-141">Agendar hora de término</span><span class="sxs-lookup"><span data-stu-id="fd13d-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="fd13d-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="fd13d-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="fd13d-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="fd13d-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="fd13d-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd13d-144">-Confirm</span></span>
<span data-ttu-id="fd13d-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd13d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd13d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd13d-146">-WhatIf</span></span>
<span data-ttu-id="fd13d-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd13d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd13d-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd13d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd13d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd13d-149">CommonParameters</span></span>
<span data-ttu-id="fd13d-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd13d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd13d-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd13d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd13d-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd13d-152">INPUTS</span></span>

### <span data-ttu-id="fd13d-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fd13d-153">None</span></span>

## <span data-ttu-id="fd13d-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd13d-154">OUTPUTS</span></span>

### <span data-ttu-id="fd13d-155">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fd13d-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="fd13d-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd13d-156">NOTES</span></span>

## <span data-ttu-id="fd13d-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd13d-157">RELATED LINKS</span></span>
