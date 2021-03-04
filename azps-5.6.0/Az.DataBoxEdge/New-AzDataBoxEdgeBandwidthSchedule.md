---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 2c83773ba08c2fefe9404fa69861518d00d4d936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891387"
---
# <span data-ttu-id="965af-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="965af-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="965af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="965af-102">SYNOPSIS</span></span>
<span data-ttu-id="965af-103">Cria um novo cronograma de largura de banda</span><span class="sxs-lookup"><span data-stu-id="965af-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="965af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="965af-104">SYNTAX</span></span>

### <span data-ttu-id="965af-105">BandwidthParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="965af-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965af-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="965af-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="965af-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="965af-107">DESCRIPTION</span></span>
<span data-ttu-id="965af-108">O cmdlet **New-AzDataBoxEdgeBandwidthSchedule** cria um novo Cronograma de Largura de Banda para um dispositivo de Borda de Caixa de Dados para ajudar a gerenciar o uso da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="965af-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="965af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="965af-109">EXAMPLES</span></span>

### <span data-ttu-id="965af-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="965af-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="965af-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="965af-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="965af-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="965af-112">PARAMETERS</span></span>

### <span data-ttu-id="965af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="965af-113">-AsJob</span></span>
<span data-ttu-id="965af-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="965af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="965af-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="965af-115">-Bandwidth</span></span>
<span data-ttu-id="965af-116">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="965af-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="965af-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="965af-117">-DaysOfWeek</span></span>
<span data-ttu-id="965af-118">DaysOfWeek Agendado</span><span class="sxs-lookup"><span data-stu-id="965af-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="965af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965af-119">-DefaultProfile</span></span>
<span data-ttu-id="965af-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="965af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965af-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="965af-121">-DeviceName</span></span>
<span data-ttu-id="965af-122">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="965af-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965af-123">-Name</span><span class="sxs-lookup"><span data-stu-id="965af-123">-Name</span></span>
<span data-ttu-id="965af-124">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="965af-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965af-125">-ResourceGroupName</span></span>
<span data-ttu-id="965af-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="965af-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965af-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="965af-127">-StartTime</span></span>
<span data-ttu-id="965af-128">Agendar Hora de Início</span><span class="sxs-lookup"><span data-stu-id="965af-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="965af-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="965af-129">-StopTime</span></span>
<span data-ttu-id="965af-130">Hora de parada de agendamento</span><span class="sxs-lookup"><span data-stu-id="965af-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="965af-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="965af-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="965af-132">Definirá Largura de Banda Ilimitada, se definido como false definirá o valor padrão como 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="965af-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965af-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="965af-133">-Confirm</span></span>
<span data-ttu-id="965af-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="965af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="965af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="965af-135">-WhatIf</span></span>
<span data-ttu-id="965af-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="965af-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="965af-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="965af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="965af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965af-138">CommonParameters</span></span>
<span data-ttu-id="965af-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965af-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="965af-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965af-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="965af-141">INPUTS</span></span>

### <span data-ttu-id="965af-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="965af-142">None</span></span>

## <span data-ttu-id="965af-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="965af-143">OUTPUTS</span></span>

### <span data-ttu-id="965af-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="965af-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="965af-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="965af-145">NOTES</span></span>

## <span data-ttu-id="965af-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="965af-146">RELATED LINKS</span></span>
