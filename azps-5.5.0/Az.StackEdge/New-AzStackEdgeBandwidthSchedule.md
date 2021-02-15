---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114454"
---
# <span data-ttu-id="05658-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="05658-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="05658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05658-102">SYNOPSIS</span></span>
<span data-ttu-id="05658-103">Cria um novo cronograma de largura de banda</span><span class="sxs-lookup"><span data-stu-id="05658-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="05658-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05658-104">SYNTAX</span></span>

### <span data-ttu-id="05658-105">UnlimitedBandwidthParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05658-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05658-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="05658-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05658-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="05658-107">DESCRIPTION</span></span>
<span data-ttu-id="05658-108">O cmdlet **New-AzSt stackEdgeBandwidthSchedule** cria um novo Cronograma de Largura de Banda para um dispositivo de Borda de Pilha para ajudar a gerenciar o uso de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="05658-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="05658-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="05658-109">EXAMPLES</span></span>

### <span data-ttu-id="05658-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05658-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="05658-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="05658-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="05658-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05658-112">PARAMETERS</span></span>

### <span data-ttu-id="05658-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05658-113">-AsJob</span></span>
<span data-ttu-id="05658-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="05658-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05658-115">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="05658-115">-Bandwidth</span></span>
<span data-ttu-id="05658-116">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="05658-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="05658-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="05658-117">-DaysOfWeek</span></span>
<span data-ttu-id="05658-118">Agendada DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="05658-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="05658-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05658-119">-DefaultProfile</span></span>
<span data-ttu-id="05658-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05658-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05658-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="05658-121">-DeviceName</span></span>
<span data-ttu-id="05658-122">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="05658-122">Device Name</span></span>

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

### <span data-ttu-id="05658-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="05658-123">-Name</span></span>
<span data-ttu-id="05658-124">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="05658-124">Resource Name</span></span>

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

### <span data-ttu-id="05658-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05658-125">-ResourceGroupName</span></span>
<span data-ttu-id="05658-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="05658-126">Resource Group Name</span></span>

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

### <span data-ttu-id="05658-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05658-127">-StartTime</span></span>
<span data-ttu-id="05658-128">Hora de Início agendada</span><span class="sxs-lookup"><span data-stu-id="05658-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="05658-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="05658-129">-StopTime</span></span>
<span data-ttu-id="05658-130">Hora de parada agendada</span><span class="sxs-lookup"><span data-stu-id="05658-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="05658-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="05658-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="05658-132">Definirá largura de banda como ilimitada</span><span class="sxs-lookup"><span data-stu-id="05658-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="05658-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="05658-133">-Confirm</span></span>
<span data-ttu-id="05658-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05658-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05658-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05658-135">-WhatIf</span></span>
<span data-ttu-id="05658-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="05658-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05658-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05658-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05658-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05658-138">CommonParameters</span></span>
<span data-ttu-id="05658-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05658-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05658-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05658-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05658-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="05658-141">INPUTS</span></span>

### <span data-ttu-id="05658-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="05658-142">None</span></span>

## <span data-ttu-id="05658-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="05658-143">OUTPUTS</span></span>

### <span data-ttu-id="05658-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="05658-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="05658-145">Notas</span><span class="sxs-lookup"><span data-stu-id="05658-145">NOTES</span></span>

## <span data-ttu-id="05658-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05658-146">RELATED LINKS</span></span>
