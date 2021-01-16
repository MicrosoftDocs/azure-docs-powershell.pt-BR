---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263284"
---
# <span data-ttu-id="109ab-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="109ab-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="109ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="109ab-102">SYNOPSIS</span></span>
<span data-ttu-id="109ab-103">Cria uma nova programação de largura de banda</span><span class="sxs-lookup"><span data-stu-id="109ab-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="109ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="109ab-104">SYNTAX</span></span>

### <span data-ttu-id="109ab-105">UnlimitedBandwidthParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="109ab-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="109ab-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="109ab-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="109ab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="109ab-107">DESCRIPTION</span></span>
<span data-ttu-id="109ab-108">O cmdlet **New-AzStackEdgeBandwidthSchedule** cria uma nova programação de largura de banda para um dispositivo de borda de pilha para ajudar a gerenciar o uso de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="109ab-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="109ab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="109ab-109">EXAMPLES</span></span>

### <span data-ttu-id="109ab-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="109ab-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="109ab-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="109ab-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="109ab-112">OS</span><span class="sxs-lookup"><span data-stu-id="109ab-112">PARAMETERS</span></span>

### <span data-ttu-id="109ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="109ab-113">-AsJob</span></span>
<span data-ttu-id="109ab-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="109ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="109ab-115">-Largura de banda</span><span class="sxs-lookup"><span data-stu-id="109ab-115">-Bandwidth</span></span>
<span data-ttu-id="109ab-116">Largura de banda em Mbps</span><span class="sxs-lookup"><span data-stu-id="109ab-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="109ab-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="109ab-117">-DaysOfWeek</span></span>
<span data-ttu-id="109ab-118">DaysOfWeek programado</span><span class="sxs-lookup"><span data-stu-id="109ab-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="109ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109ab-119">-DefaultProfile</span></span>
<span data-ttu-id="109ab-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="109ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109ab-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="109ab-121">-DeviceName</span></span>
<span data-ttu-id="109ab-122">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="109ab-122">Device Name</span></span>

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

### <span data-ttu-id="109ab-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="109ab-123">-Name</span></span>
<span data-ttu-id="109ab-124">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="109ab-124">Resource Name</span></span>

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

### <span data-ttu-id="109ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="109ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="109ab-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="109ab-126">Resource Group Name</span></span>

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

### <span data-ttu-id="109ab-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="109ab-127">-StartTime</span></span>
<span data-ttu-id="109ab-128">Agendar hora de início</span><span class="sxs-lookup"><span data-stu-id="109ab-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="109ab-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="109ab-129">-StopTime</span></span>
<span data-ttu-id="109ab-130">Agendar hora de término</span><span class="sxs-lookup"><span data-stu-id="109ab-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="109ab-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="109ab-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="109ab-132">Definirá a largura de banda como ilimitada</span><span class="sxs-lookup"><span data-stu-id="109ab-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="109ab-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="109ab-133">-Confirm</span></span>
<span data-ttu-id="109ab-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="109ab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="109ab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="109ab-135">-WhatIf</span></span>
<span data-ttu-id="109ab-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="109ab-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="109ab-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="109ab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="109ab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109ab-138">CommonParameters</span></span>
<span data-ttu-id="109ab-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="109ab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109ab-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="109ab-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109ab-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="109ab-141">INPUTS</span></span>

### <span data-ttu-id="109ab-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="109ab-142">None</span></span>

## <span data-ttu-id="109ab-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="109ab-143">OUTPUTS</span></span>

### <span data-ttu-id="109ab-144">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="109ab-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="109ab-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="109ab-145">NOTES</span></span>

## <span data-ttu-id="109ab-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="109ab-146">RELATED LINKS</span></span>
