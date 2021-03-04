---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: d0f5d0d71f35df5bb36ea86a1ec20ca009256f67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889284"
---
# <span data-ttu-id="45b8e-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="45b8e-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="45b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="45b8e-103">Atualiza um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="45b8e-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="45b8e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45b8e-104">SYNTAX</span></span>

### <span data-ttu-id="45b8e-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45b8e-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45b8e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b8e-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="45b8e-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b8e-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45b8e-114">DESCRIPTION</span></span>
<span data-ttu-id="45b8e-115">O cmdlet **Set-AzDataBoxEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="45b8e-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="45b8e-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45b8e-116">EXAMPLES</span></span>

### <span data-ttu-id="45b8e-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45b8e-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="45b8e-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45b8e-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="45b8e-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45b8e-119">PARAMETERS</span></span>

### <span data-ttu-id="45b8e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b8e-120">-AsJob</span></span>
<span data-ttu-id="45b8e-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45b8e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45b8e-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="45b8e-122">-Bandwidth</span></span>
<span data-ttu-id="45b8e-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="45b8e-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="45b8e-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="45b8e-124">-DaysOfWeek</span></span>
<span data-ttu-id="45b8e-125">DaysOfWeek Agendado</span><span class="sxs-lookup"><span data-stu-id="45b8e-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="45b8e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b8e-126">-DefaultProfile</span></span>
<span data-ttu-id="45b8e-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45b8e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b8e-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="45b8e-128">-DeviceName</span></span>
<span data-ttu-id="45b8e-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="45b8e-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45b8e-130">-InputObject</span></span>
<span data-ttu-id="45b8e-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b8e-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="45b8e-132">-Name</span></span>
<span data-ttu-id="45b8e-133">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="45b8e-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b8e-134">-ResourceGroupName</span></span>
<span data-ttu-id="45b8e-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="45b8e-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b8e-136">-ResourceId</span></span>
<span data-ttu-id="45b8e-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="45b8e-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="45b8e-138">-StartTime</span></span>
<span data-ttu-id="45b8e-139">Agendar Hora de Início</span><span class="sxs-lookup"><span data-stu-id="45b8e-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="45b8e-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="45b8e-140">-StopTime</span></span>
<span data-ttu-id="45b8e-141">Hora de parada de agendamento</span><span class="sxs-lookup"><span data-stu-id="45b8e-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="45b8e-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="45b8e-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="45b8e-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="45b8e-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b8e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45b8e-144">-Confirm</span></span>
<span data-ttu-id="45b8e-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b8e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b8e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b8e-146">-WhatIf</span></span>
<span data-ttu-id="45b8e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b8e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b8e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b8e-149">CommonParameters</span></span>
<span data-ttu-id="45b8e-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b8e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b8e-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b8e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b8e-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45b8e-152">INPUTS</span></span>

### <span data-ttu-id="45b8e-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="45b8e-153">None</span></span>

## <span data-ttu-id="45b8e-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45b8e-154">OUTPUTS</span></span>

### <span data-ttu-id="45b8e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="45b8e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="45b8e-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="45b8e-156">NOTES</span></span>

## <span data-ttu-id="45b8e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45b8e-157">RELATED LINKS</span></span>
