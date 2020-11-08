---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111272"
---
# <span data-ttu-id="be186-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="be186-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="be186-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be186-102">SYNOPSIS</span></span>
<span data-ttu-id="be186-103">Configura um gatilho no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be186-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="be186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be186-104">SYNTAX</span></span>

### <span data-ttu-id="be186-105">FileEventTriggerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="be186-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be186-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="be186-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be186-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be186-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be186-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be186-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be186-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be186-109">DESCRIPTION</span></span>
<span data-ttu-id="be186-110">O cmdlet **New-AzStackEdgeTrigger** configura um gatilho no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="be186-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="be186-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be186-111">EXAMPLES</span></span>

### <span data-ttu-id="be186-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be186-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="be186-113">OS</span><span class="sxs-lookup"><span data-stu-id="be186-113">PARAMETERS</span></span>

### <span data-ttu-id="be186-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be186-114">-AsJob</span></span>
<span data-ttu-id="be186-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="be186-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be186-116">-DefaultProfile</span></span>
<span data-ttu-id="be186-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be186-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be186-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="be186-118">-DeviceName</span></span>
<span data-ttu-id="be186-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="be186-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be186-120">-Fileevent</span><span class="sxs-lookup"><span data-stu-id="be186-120">-FileEvent</span></span>
<span data-ttu-id="be186-121">Passe esse parâmetro de opção para configurar o gatilho fileevent</span><span class="sxs-lookup"><span data-stu-id="be186-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="be186-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="be186-122">-Name</span></span>
<span data-ttu-id="be186-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="be186-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be186-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="be186-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="be186-125">Passe esse parâmetro de opção para configurar o gatilho PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="be186-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="be186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be186-126">-ResourceGroupName</span></span>
<span data-ttu-id="be186-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="be186-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be186-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="be186-128">-RoleName</span></span>
<span data-ttu-id="be186-129">Calcule a função em relação a quais eventos serão gerados.</span><span class="sxs-lookup"><span data-stu-id="be186-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="be186-130">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="be186-130">-Schedule</span></span>
<span data-ttu-id="be186-131">Frequência periódica em que o evento do temporizador precisa ser gerado.</span><span class="sxs-lookup"><span data-stu-id="be186-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="be186-132">Especifique um cronograma em qualquer um dos dias (entre 1 e 365), horas (entre 1 e 23) ou minutos (entre 1 e 59).</span><span class="sxs-lookup"><span data-stu-id="be186-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="be186-133">-Shareid</span><span class="sxs-lookup"><span data-stu-id="be186-133">-ShareId</span></span>
<span data-ttu-id="be186-134">ID de compartilhamento de arquivos a ser passada no gatilho fileevent</span><span class="sxs-lookup"><span data-stu-id="be186-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="be186-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="be186-135">-ShareName</span></span>
<span data-ttu-id="be186-136">ID de compartilhamento de arquivos a ser passada no gatilho fileevent</span><span class="sxs-lookup"><span data-stu-id="be186-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="be186-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="be186-137">-StartTime</span></span>
<span data-ttu-id="be186-138">A hora do dia que resulta em um gatilho válido.</span><span class="sxs-lookup"><span data-stu-id="be186-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="be186-139">A agenda é calculada com referência ao tempo especificado em até segundos.</span><span class="sxs-lookup"><span data-stu-id="be186-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="be186-140">Se o fuso horário não for especificado, o tempo será considerado no fuso horário do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be186-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="be186-141">O valor sempre será retornado como horário UTC.</span><span class="sxs-lookup"><span data-stu-id="be186-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="be186-142">-Tópico</span><span class="sxs-lookup"><span data-stu-id="be186-142">-Topic</span></span>
<span data-ttu-id="be186-143">Tópico em que os eventos periódicos são publicados no dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="be186-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="be186-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be186-144">-Confirm</span></span>
<span data-ttu-id="be186-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be186-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be186-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be186-146">-WhatIf</span></span>
<span data-ttu-id="be186-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be186-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be186-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be186-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be186-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be186-149">CommonParameters</span></span>
<span data-ttu-id="be186-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be186-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be186-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be186-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be186-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be186-152">INPUTS</span></span>

### <span data-ttu-id="be186-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="be186-153">None</span></span>

## <span data-ttu-id="be186-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be186-154">OUTPUTS</span></span>

### <span data-ttu-id="be186-155">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="be186-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="be186-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be186-156">NOTES</span></span>

## <span data-ttu-id="be186-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be186-157">RELATED LINKS</span></span>
