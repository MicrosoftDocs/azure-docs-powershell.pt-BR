---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: a9a49f89301da627fcafa285915d0331240f75b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889136"
---
# <span data-ttu-id="4c091-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4c091-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="4c091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c091-102">SYNOPSIS</span></span>
<span data-ttu-id="4c091-103">Cria um novo cronograma de largura de banda</span><span class="sxs-lookup"><span data-stu-id="4c091-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="4c091-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c091-104">SYNTAX</span></span>

### <span data-ttu-id="4c091-105">UnlimitedBandwidthParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c091-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c091-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c091-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c091-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c091-107">DESCRIPTION</span></span>
<span data-ttu-id="4c091-108">O cmdlet **New-AzStackEdgeBandwidthSchedule** cria um novo Cronograma de Largura de Banda para um dispositivo de Borda de Pilha para ajudar a gerenciar o uso da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="4c091-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="4c091-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c091-109">EXAMPLES</span></span>

### <span data-ttu-id="4c091-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c091-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="4c091-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c091-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="4c091-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c091-112">PARAMETERS</span></span>

### <span data-ttu-id="4c091-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c091-113">-AsJob</span></span>
<span data-ttu-id="4c091-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4c091-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c091-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="4c091-115">-Bandwidth</span></span>
<span data-ttu-id="4c091-116">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="4c091-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="4c091-117">-DaysOfWeek</span></span>
<span data-ttu-id="4c091-118">DaysOfWeek Agendado</span><span class="sxs-lookup"><span data-stu-id="4c091-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c091-119">-DefaultProfile</span></span>
<span data-ttu-id="4c091-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c091-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c091-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4c091-121">-DeviceName</span></span>
<span data-ttu-id="4c091-122">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4c091-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4c091-123">-Name</span></span>
<span data-ttu-id="4c091-124">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="4c091-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c091-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c091-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4c091-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4c091-127">-StartTime</span></span>
<span data-ttu-id="4c091-128">Agendar Hora de Início</span><span class="sxs-lookup"><span data-stu-id="4c091-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="4c091-129">-StopTime</span></span>
<span data-ttu-id="4c091-130">Hora de parada de agendamento</span><span class="sxs-lookup"><span data-stu-id="4c091-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="4c091-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="4c091-132">Definirá a largura de banda como ilimitada</span><span class="sxs-lookup"><span data-stu-id="4c091-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c091-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c091-133">-Confirm</span></span>
<span data-ttu-id="4c091-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c091-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c091-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c091-135">-WhatIf</span></span>
<span data-ttu-id="4c091-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c091-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c091-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c091-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c091-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c091-138">CommonParameters</span></span>
<span data-ttu-id="4c091-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c091-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c091-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c091-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c091-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c091-141">INPUTS</span></span>

### <span data-ttu-id="4c091-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4c091-142">None</span></span>

## <span data-ttu-id="4c091-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c091-143">OUTPUTS</span></span>

### <span data-ttu-id="4c091-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4c091-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="4c091-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c091-145">NOTES</span></span>

## <span data-ttu-id="4c091-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c091-146">RELATED LINKS</span></span>
