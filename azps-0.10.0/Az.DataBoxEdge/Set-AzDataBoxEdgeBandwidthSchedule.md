---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: f761a84fe994f0da68b4d3a86b513ba333b06573
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775927"
---
# <span data-ttu-id="38fa1-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="38fa1-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="38fa1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="38fa1-103">Atualiza um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="38fa1-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="38fa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38fa1-104">SYNTAX</span></span>

### <span data-ttu-id="38fa1-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="38fa1-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38fa1-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fa1-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="38fa1-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38fa1-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38fa1-114">DESCRIPTION</span></span>
<span data-ttu-id="38fa1-115">O cmdlet **set-AzDataBoxEdgeBandwidthSchedule** atualiza um cronograma de largura de banda para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="38fa1-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="38fa1-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38fa1-116">EXAMPLES</span></span>

### <span data-ttu-id="38fa1-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38fa1-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="38fa1-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38fa1-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="38fa1-119">OS</span><span class="sxs-lookup"><span data-stu-id="38fa1-119">PARAMETERS</span></span>

### <span data-ttu-id="38fa1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38fa1-120">-AsJob</span></span>
<span data-ttu-id="38fa1-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38fa1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38fa1-122">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="38fa1-122">-Bandwidth</span></span>
<span data-ttu-id="38fa1-123">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="38fa1-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="38fa1-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="38fa1-124">-DaysOfWeek</span></span>
<span data-ttu-id="38fa1-125">DaysOfWeek programado</span><span class="sxs-lookup"><span data-stu-id="38fa1-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="38fa1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fa1-126">-DefaultProfile</span></span>
<span data-ttu-id="38fa1-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38fa1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38fa1-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="38fa1-128">-DeviceName</span></span>
<span data-ttu-id="38fa1-129">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="38fa1-129">Device Name</span></span>

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

### <span data-ttu-id="38fa1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38fa1-130">-InputObject</span></span>
<span data-ttu-id="38fa1-131">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="38fa1-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="38fa1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="38fa1-132">-Name</span></span>
<span data-ttu-id="38fa1-133">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="38fa1-133">Resource Name</span></span>

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

### <span data-ttu-id="38fa1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fa1-134">-ResourceGroupName</span></span>
<span data-ttu-id="38fa1-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="38fa1-135">Resource Group Name</span></span>

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

### <span data-ttu-id="38fa1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38fa1-136">-ResourceId</span></span>
<span data-ttu-id="38fa1-137">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="38fa1-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="38fa1-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="38fa1-138">-StartTime</span></span>
<span data-ttu-id="38fa1-139">Agendar hora de início</span><span class="sxs-lookup"><span data-stu-id="38fa1-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="38fa1-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="38fa1-140">-StopTime</span></span>
<span data-ttu-id="38fa1-141">Agendar hora de término</span><span class="sxs-lookup"><span data-stu-id="38fa1-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="38fa1-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="38fa1-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="38fa1-143">Definirá largura de banda ilimitada</span><span class="sxs-lookup"><span data-stu-id="38fa1-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="38fa1-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38fa1-144">-Confirm</span></span>
<span data-ttu-id="38fa1-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38fa1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38fa1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38fa1-146">-WhatIf</span></span>
<span data-ttu-id="38fa1-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38fa1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38fa1-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38fa1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38fa1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fa1-149">CommonParameters</span></span>
<span data-ttu-id="38fa1-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fa1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fa1-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38fa1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fa1-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38fa1-152">INPUTS</span></span>

### <span data-ttu-id="38fa1-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="38fa1-153">None</span></span>

## <span data-ttu-id="38fa1-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38fa1-154">OUTPUTS</span></span>

### <span data-ttu-id="38fa1-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="38fa1-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="38fa1-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38fa1-156">NOTES</span></span>

## <span data-ttu-id="38fa1-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38fa1-157">RELATED LINKS</span></span>