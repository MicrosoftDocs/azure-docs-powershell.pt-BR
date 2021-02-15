---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111988"
---
# <span data-ttu-id="6c6a3-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6c6a3-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="6c6a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6a3-103">Configura um gatilho no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="6c6a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c6a3-104">SYNTAX</span></span>

### <span data-ttu-id="6c6a3-105">FileEventTrimeterParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6c6a3-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c6a3-106">PeriodicTimerTrimeterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6a3-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c6a3-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6a3-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c6a3-108">PeriodicTimerTriourceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6a3-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c6a3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c6a3-109">DESCRIPTION</span></span>
<span data-ttu-id="6c6a3-110">O **cmdlet New-AzDataBoxEdgeTrigger** configura um gatilho no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="6c6a3-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c6a3-111">EXAMPLES</span></span>

### <span data-ttu-id="6c6a3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c6a3-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="6c6a3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c6a3-113">PARAMETERS</span></span>

### <span data-ttu-id="6c6a3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c6a3-114">-AsJob</span></span>
<span data-ttu-id="6c6a3-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6c6a3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c6a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6a3-116">-DefaultProfile</span></span>
<span data-ttu-id="6c6a3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c6a3-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c6a3-118">-DeviceName</span></span>
<span data-ttu-id="6c6a3-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6c6a3-119">Device Name</span></span>

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

### <span data-ttu-id="6c6a3-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-120">-FileEvent</span></span>
<span data-ttu-id="6c6a3-121">Passe este parâmetro de opção para configurar o Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="6c6a3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c6a3-122">-Name</span></span>
<span data-ttu-id="6c6a3-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="6c6a3-123">Resource Name</span></span>

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

### <span data-ttu-id="6c6a3-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="6c6a3-125">Passe este parâmetro de opção para configurar o Gatilho PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="6c6a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c6a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c6a3-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6c6a3-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6c6a3-128">-NomedaEminidade</span><span class="sxs-lookup"><span data-stu-id="6c6a3-128">-RoleName</span></span>
<span data-ttu-id="6c6a3-129">Calcule a função em relação a quais eventos serão elevados.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="6c6a3-130">-Agendar</span><span class="sxs-lookup"><span data-stu-id="6c6a3-130">-Schedule</span></span>
<span data-ttu-id="6c6a3-131">Frequência periódica na qual o evento de temporizador precisa ser elevado.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="6c6a3-132">Especifique um cronograma em dias (entre 1 e 365), horas (entre 1 e 23) ou minutos (entre 1 e 59).</span><span class="sxs-lookup"><span data-stu-id="6c6a3-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="6c6a3-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="6c6a3-133">-ShareId</span></span>
<span data-ttu-id="6c6a3-134">ID de compartilhamento de arquivos a ser passada no Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="6c6a3-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6c6a3-135">-ShareName</span></span>
<span data-ttu-id="6c6a3-136">ID de compartilhamento de arquivos a ser passada no Gatilho FileEvent</span><span class="sxs-lookup"><span data-stu-id="6c6a3-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="6c6a3-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6c6a3-137">-StartTime</span></span>
<span data-ttu-id="6c6a3-138">A hora do dia que resulta em um gatilho válido.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="6c6a3-139">O cronograma é calculado com referência à hora especificada em até segundos.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="6c6a3-140">Se o timezone não for especificado, o tempo será considerado como no zona de tempo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="6c6a3-141">O valor sempre será retornado como horário UTC.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="6c6a3-142">-Tópico</span><span class="sxs-lookup"><span data-stu-id="6c6a3-142">-Topic</span></span>
<span data-ttu-id="6c6a3-143">Tópico em que os eventos periódicos são publicados no dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="6c6a3-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6c6a3-144">-Confirm</span></span>
<span data-ttu-id="6c6a3-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c6a3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c6a3-146">-WhatIf</span></span>
<span data-ttu-id="6c6a3-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c6a3-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c6a3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6a3-149">CommonParameters</span></span>
<span data-ttu-id="6c6a3-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c6a3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6a3-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c6a3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6a3-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="6c6a3-152">INPUTS</span></span>

### <span data-ttu-id="6c6a3-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6c6a3-153">None</span></span>

## <span data-ttu-id="6c6a3-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="6c6a3-154">OUTPUTS</span></span>

### <span data-ttu-id="6c6a3-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6c6a3-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="6c6a3-156">Notas</span><span class="sxs-lookup"><span data-stu-id="6c6a3-156">NOTES</span></span>

## <span data-ttu-id="6c6a3-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c6a3-157">RELATED LINKS</span></span>
