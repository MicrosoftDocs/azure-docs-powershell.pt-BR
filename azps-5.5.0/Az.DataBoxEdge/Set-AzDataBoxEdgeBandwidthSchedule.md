---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115433"
---
# <span data-ttu-id="d5d70-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d5d70-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="d5d70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5d70-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d70-103">Atualiza um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="d5d70-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="d5d70-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5d70-104">SYNTAX</span></span>

### <span data-ttu-id="d5d70-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d5d70-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5d70-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d70-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d5d70-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d70-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5d70-114">DESCRIPTION</span></span>
<span data-ttu-id="d5d70-115">O cmdlet **Set-AzDataBoxEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="d5d70-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="d5d70-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5d70-116">EXAMPLES</span></span>

### <span data-ttu-id="d5d70-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5d70-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="d5d70-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d5d70-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="d5d70-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5d70-119">PARAMETERS</span></span>

### <span data-ttu-id="d5d70-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5d70-120">-AsJob</span></span>
<span data-ttu-id="d5d70-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d5d70-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5d70-122">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="d5d70-122">-Bandwidth</span></span>
<span data-ttu-id="d5d70-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="d5d70-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="d5d70-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d5d70-124">-DaysOfWeek</span></span>
<span data-ttu-id="d5d70-125">Agendada DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d5d70-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="d5d70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d70-126">-DefaultProfile</span></span>
<span data-ttu-id="d5d70-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d70-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d70-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d5d70-128">-DeviceName</span></span>
<span data-ttu-id="d5d70-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d5d70-129">Device Name</span></span>

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

### <span data-ttu-id="d5d70-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d70-130">-InputObject</span></span>
<span data-ttu-id="d5d70-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d70-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="d5d70-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5d70-132">-Name</span></span>
<span data-ttu-id="d5d70-133">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="d5d70-133">Resource Name</span></span>

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

### <span data-ttu-id="d5d70-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d70-134">-ResourceGroupName</span></span>
<span data-ttu-id="d5d70-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d5d70-135">Resource Group Name</span></span>

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

### <span data-ttu-id="d5d70-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d70-136">-ResourceId</span></span>
<span data-ttu-id="d5d70-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d70-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="d5d70-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d5d70-138">-StartTime</span></span>
<span data-ttu-id="d5d70-139">Hora de Início agendada</span><span class="sxs-lookup"><span data-stu-id="d5d70-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="d5d70-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="d5d70-140">-StopTime</span></span>
<span data-ttu-id="d5d70-141">Hora de parada agendada</span><span class="sxs-lookup"><span data-stu-id="d5d70-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="d5d70-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="d5d70-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="d5d70-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="d5d70-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="d5d70-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d5d70-144">-Confirm</span></span>
<span data-ttu-id="d5d70-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d70-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d70-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d70-146">-WhatIf</span></span>
<span data-ttu-id="d5d70-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d5d70-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5d70-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5d70-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d70-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d70-149">CommonParameters</span></span>
<span data-ttu-id="d5d70-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d70-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d70-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5d70-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d70-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="d5d70-152">INPUTS</span></span>

### <span data-ttu-id="d5d70-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d5d70-153">None</span></span>

## <span data-ttu-id="d5d70-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="d5d70-154">OUTPUTS</span></span>

### <span data-ttu-id="d5d70-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d5d70-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="d5d70-156">Notas</span><span class="sxs-lookup"><span data-stu-id="d5d70-156">NOTES</span></span>

## <span data-ttu-id="d5d70-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5d70-157">RELATED LINKS</span></span>
