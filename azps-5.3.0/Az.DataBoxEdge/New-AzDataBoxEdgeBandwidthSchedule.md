---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433963"
---
# <span data-ttu-id="9e298-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9e298-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9e298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e298-102">SYNOPSIS</span></span>
<span data-ttu-id="9e298-103">Cria uma nova programação de largura de banda</span><span class="sxs-lookup"><span data-stu-id="9e298-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="9e298-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e298-104">SYNTAX</span></span>

### <span data-ttu-id="9e298-105">BandwidthParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e298-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e298-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e298-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e298-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e298-107">DESCRIPTION</span></span>
<span data-ttu-id="9e298-108">O cmdlet **New-AzDataBoxEdgeBandwidthSchedule** cria uma nova programação de largura de banda para um dispositivo de borda de caixa de dados para ajudar a gerenciar o uso de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="9e298-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="9e298-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e298-109">EXAMPLES</span></span>

### <span data-ttu-id="9e298-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e298-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="9e298-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9e298-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="9e298-112">OS</span><span class="sxs-lookup"><span data-stu-id="9e298-112">PARAMETERS</span></span>

### <span data-ttu-id="9e298-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e298-113">-AsJob</span></span>
<span data-ttu-id="9e298-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9e298-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e298-115">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="9e298-115">-Bandwidth</span></span>
<span data-ttu-id="9e298-116">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="9e298-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="9e298-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="9e298-117">-DaysOfWeek</span></span>
<span data-ttu-id="9e298-118">DaysOfWeek programado</span><span class="sxs-lookup"><span data-stu-id="9e298-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="9e298-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e298-119">-DefaultProfile</span></span>
<span data-ttu-id="9e298-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e298-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e298-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9e298-121">-DeviceName</span></span>
<span data-ttu-id="9e298-122">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9e298-122">Device Name</span></span>

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

### <span data-ttu-id="9e298-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e298-123">-Name</span></span>
<span data-ttu-id="9e298-124">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="9e298-124">Resource Name</span></span>

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

### <span data-ttu-id="9e298-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e298-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e298-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9e298-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9e298-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9e298-127">-StartTime</span></span>
<span data-ttu-id="9e298-128">Agendar hora de início</span><span class="sxs-lookup"><span data-stu-id="9e298-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="9e298-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="9e298-129">-StopTime</span></span>
<span data-ttu-id="9e298-130">Agendar hora de término</span><span class="sxs-lookup"><span data-stu-id="9e298-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="9e298-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="9e298-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="9e298-132">Definirá largura de banda ilimitada, se definido como false irá definir o valor padrão como 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="9e298-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="9e298-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e298-133">-Confirm</span></span>
<span data-ttu-id="9e298-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e298-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e298-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e298-135">-WhatIf</span></span>
<span data-ttu-id="9e298-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e298-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e298-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e298-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e298-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e298-138">CommonParameters</span></span>
<span data-ttu-id="9e298-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e298-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e298-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e298-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e298-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e298-141">INPUTS</span></span>

### <span data-ttu-id="9e298-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9e298-142">None</span></span>

## <span data-ttu-id="9e298-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e298-143">OUTPUTS</span></span>

### <span data-ttu-id="9e298-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9e298-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9e298-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e298-145">NOTES</span></span>

## <span data-ttu-id="9e298-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e298-146">RELATED LINKS</span></span>
