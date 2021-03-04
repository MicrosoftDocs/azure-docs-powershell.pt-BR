---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 195be7fb51e947888c7c22911f4fb5177454731e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888529"
---
# <span data-ttu-id="2e5d6-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2e5d6-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2e5d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5d6-103">Configura um gatilho no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="2e5d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e5d6-104">SYNTAX</span></span>

### <span data-ttu-id="2e5d6-105">FileEventTriggerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e5d6-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5d6-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5d6-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5d6-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5d6-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5d6-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5d6-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5d6-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e5d6-109">DESCRIPTION</span></span>
<span data-ttu-id="2e5d6-110">O cmdlet **New-AzDataBoxEdgeTrigger** configura um gatilho no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="2e5d6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-111">EXAMPLES</span></span>

### <span data-ttu-id="2e5d6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e5d6-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="2e5d6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-113">PARAMETERS</span></span>

### <span data-ttu-id="2e5d6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e5d6-114">-AsJob</span></span>
<span data-ttu-id="2e5d6-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2e5d6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e5d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5d6-116">-DefaultProfile</span></span>
<span data-ttu-id="2e5d6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5d6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2e5d6-118">-DeviceName</span></span>
<span data-ttu-id="2e5d6-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="2e5d6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-120">-FileEvent</span></span>
<span data-ttu-id="2e5d6-121">Passe esse parâmetro de opção para configurar o Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2e5d6-122">-Name</span></span>
<span data-ttu-id="2e5d6-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="2e5d6-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="2e5d6-125">Passe esse parâmetro de opção para configurar o Gatilho PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e5d6-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2e5d6-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="2e5d6-128">-RoleName</span></span>
<span data-ttu-id="2e5d6-129">Calcular função em relação a quais eventos serão gerados.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="2e5d6-130">-Schedule</span></span>
<span data-ttu-id="2e5d6-131">Frequência periódica na qual o evento de timer precisa ser gerado.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="2e5d6-132">Especifique um cronograma em ambos os dias (entre 1 e 365) , horas (entre 1 e 23) ou minutos (entre 1 e 59).</span><span class="sxs-lookup"><span data-stu-id="2e5d6-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="2e5d6-133">-ShareId</span></span>
<span data-ttu-id="2e5d6-134">ID do compartilhamento de arquivos a ser passada no Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2e5d6-135">-ShareName</span></span>
<span data-ttu-id="2e5d6-136">ID do compartilhamento de arquivos a ser passada no Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="2e5d6-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e5d6-137">-StartTime</span></span>
<span data-ttu-id="2e5d6-138">A hora do dia que resulta em um gatilho válido.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="2e5d6-139">O agendamento é calculado com referência ao tempo especificado até segundos.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="2e5d6-140">Se o timezone não for especificado, o tempo será considerado como no timezone do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="2e5d6-141">O valor sempre será retornado como hora UTC.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="2e5d6-142">-Topic</span></span>
<span data-ttu-id="2e5d6-143">Tópico em que eventos periódicos são publicados no dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d6-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e5d6-144">-Confirm</span></span>
<span data-ttu-id="2e5d6-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5d6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5d6-146">-WhatIf</span></span>
<span data-ttu-id="2e5d6-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e5d6-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5d6-149">CommonParameters</span></span>
<span data-ttu-id="2e5d6-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5d6-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e5d6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5d6-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-152">INPUTS</span></span>

### <span data-ttu-id="2e5d6-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e5d6-153">None</span></span>

## <span data-ttu-id="2e5d6-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-154">OUTPUTS</span></span>

### <span data-ttu-id="2e5d6-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2e5d6-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2e5d6-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e5d6-156">NOTES</span></span>

## <span data-ttu-id="2e5d6-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-157">RELATED LINKS</span></span>
