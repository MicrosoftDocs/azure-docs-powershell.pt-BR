---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114450"
---
# <span data-ttu-id="6a1b9-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="6a1b9-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="6a1b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1b9-103">Atualiza um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="6a1b9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a1b9-104">SYNTAX</span></span>

### <span data-ttu-id="6a1b9-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a1b9-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1b9-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="6a1b9-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a1b9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a1b9-114">DESCRIPTION</span></span>
<span data-ttu-id="6a1b9-115">O cmdlet **Set-AzSt stackEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="6a1b9-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a1b9-116">EXAMPLES</span></span>

### <span data-ttu-id="6a1b9-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a1b9-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="6a1b9-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6a1b9-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="6a1b9-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a1b9-119">PARAMETERS</span></span>

### <span data-ttu-id="6a1b9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a1b9-120">-AsJob</span></span>
<span data-ttu-id="6a1b9-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6a1b9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a1b9-122">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="6a1b9-122">-Bandwidth</span></span>
<span data-ttu-id="6a1b9-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="6a1b9-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="6a1b9-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="6a1b9-124">-DaysOfWeek</span></span>
<span data-ttu-id="6a1b9-125">Agendada DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="6a1b9-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="6a1b9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1b9-126">-DefaultProfile</span></span>
<span data-ttu-id="6a1b9-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a1b9-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6a1b9-128">-DeviceName</span></span>
<span data-ttu-id="6a1b9-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6a1b9-129">Device Name</span></span>

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

### <span data-ttu-id="6a1b9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a1b9-130">-InputObject</span></span>
<span data-ttu-id="6a1b9-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1b9-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="6a1b9-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a1b9-132">-Name</span></span>
<span data-ttu-id="6a1b9-133">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="6a1b9-133">Resource Name</span></span>

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

### <span data-ttu-id="6a1b9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a1b9-134">-ResourceGroupName</span></span>
<span data-ttu-id="6a1b9-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6a1b9-135">Resource Group Name</span></span>

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

### <span data-ttu-id="6a1b9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1b9-136">-ResourceId</span></span>
<span data-ttu-id="6a1b9-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1b9-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="6a1b9-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6a1b9-138">-StartTime</span></span>
<span data-ttu-id="6a1b9-139">Hora de Início agendada</span><span class="sxs-lookup"><span data-stu-id="6a1b9-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="6a1b9-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="6a1b9-140">-StopTime</span></span>
<span data-ttu-id="6a1b9-141">Hora de parada agendada</span><span class="sxs-lookup"><span data-stu-id="6a1b9-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="6a1b9-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="6a1b9-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="6a1b9-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="6a1b9-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="6a1b9-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6a1b9-144">-Confirm</span></span>
<span data-ttu-id="6a1b9-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a1b9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a1b9-146">-WhatIf</span></span>
<span data-ttu-id="6a1b9-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a1b9-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a1b9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1b9-149">CommonParameters</span></span>
<span data-ttu-id="6a1b9-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1b9-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a1b9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1b9-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a1b9-152">INPUTS</span></span>

### <span data-ttu-id="6a1b9-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a1b9-153">None</span></span>

## <span data-ttu-id="6a1b9-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a1b9-154">OUTPUTS</span></span>

### <span data-ttu-id="6a1b9-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="6a1b9-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="6a1b9-156">Notas</span><span class="sxs-lookup"><span data-stu-id="6a1b9-156">NOTES</span></span>

## <span data-ttu-id="6a1b9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a1b9-157">RELATED LINKS</span></span>
