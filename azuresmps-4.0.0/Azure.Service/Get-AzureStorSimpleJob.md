---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945558"
---
# <span data-ttu-id="6254d-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6254d-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="6254d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6254d-102">SYNOPSIS</span></span>
<span data-ttu-id="6254d-103">Obtém trabalhos do StorSimple.</span><span class="sxs-lookup"><span data-stu-id="6254d-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="6254d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6254d-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6254d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6254d-105">DESCRIPTION</span></span>
<span data-ttu-id="6254d-106">O cmdlet **Get-AzureStorSimpleJob** Obtém trabalhos do Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="6254d-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="6254d-107">Especifique uma ID de instância para obter um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="6254d-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="6254d-108">Especifique outros parâmetros para limitar os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6254d-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="6254d-109">Este cmdlet retorna um máximo de 200 trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6254d-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="6254d-110">Se houver mais de 200 trabalhos, obtenha os trabalhos restantes usando os parâmetros *First* e *Skip* .</span><span class="sxs-lookup"><span data-stu-id="6254d-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="6254d-111">Se você especificar um valor de 100 para *Skip* e 50 para *primeiro* , esse cmdlet não retornará os primeiros resultados de 100.</span><span class="sxs-lookup"><span data-stu-id="6254d-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="6254d-112">Ele retorna os próximos 50 resultados após o 100 que ele ignora.</span><span class="sxs-lookup"><span data-stu-id="6254d-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="6254d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6254d-113">EXAMPLES</span></span>

### <span data-ttu-id="6254d-114">Exemplo 1: obter um trabalho usando uma ID</span><span class="sxs-lookup"><span data-stu-id="6254d-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="6254d-115">Esse comando obtém informações para o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="6254d-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="6254d-116">Exemplo 2: obter trabalhos usando um nome de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6254d-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="6254d-117">Esse comando obtém informações para os trabalhos do dispositivo chamado 8600-bravo 001.</span><span class="sxs-lookup"><span data-stu-id="6254d-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="6254d-118">O comando obtém os dois primeiros trabalhos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6254d-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="6254d-119">Exemplo 3: obter trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="6254d-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="6254d-120">Este comando obtém trabalhos concluídos.</span><span class="sxs-lookup"><span data-stu-id="6254d-120">This command gets completed jobs.</span></span>
<span data-ttu-id="6254d-121">O comando obtém apenas os dois primeiros trabalhos depois de ignorar os dez primeiros trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6254d-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="6254d-122">Exemplo 4: obter trabalhos de backup manuais</span><span class="sxs-lookup"><span data-stu-id="6254d-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="6254d-123">Esse comando obtém os trabalhos do tipo de backup manual.</span><span class="sxs-lookup"><span data-stu-id="6254d-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="6254d-124">Exemplo 5: obter trabalhos entre horários especificados</span><span class="sxs-lookup"><span data-stu-id="6254d-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="6254d-125">Os dois primeiros comandos criam objetos **DateTime** usando o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="6254d-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="6254d-126">Os comandos armazenam os novos horários nas variáveis $StartTime e $EndTime.</span><span class="sxs-lookup"><span data-stu-id="6254d-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="6254d-127">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6254d-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="6254d-128">O comando final Obtém trabalhos para o dispositivo chamado Device07 entre os horários armazenados em $StartTime e $EndTime.</span><span class="sxs-lookup"><span data-stu-id="6254d-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="6254d-129">OS</span><span class="sxs-lookup"><span data-stu-id="6254d-129">PARAMETERS</span></span>

### <span data-ttu-id="6254d-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6254d-130">-DeviceName</span></span>
<span data-ttu-id="6254d-131">Especifica o nome de um dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="6254d-131">Specifies the name of a StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-132">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="6254d-132">-First</span></span>
<span data-ttu-id="6254d-133">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="6254d-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="6254d-134">Digite o número de objetos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="6254d-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-135">-De</span><span class="sxs-lookup"><span data-stu-id="6254d-135">-From</span></span>
<span data-ttu-id="6254d-136">Especifica a data e a hora de início dos trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6254d-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6254d-137">-InstanceId</span></span>
<span data-ttu-id="6254d-138">Especifica a ID do trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="6254d-138">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6254d-139">-Profile</span></span>
<span data-ttu-id="6254d-140">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6254d-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6254d-141">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6254d-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="6254d-142">-Skip</span></span>
<span data-ttu-id="6254d-143">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="6254d-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="6254d-144">Digite o número de objetos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="6254d-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-145">-Status</span><span class="sxs-lookup"><span data-stu-id="6254d-145">-Status</span></span>
<span data-ttu-id="6254d-146">Especifica o status.</span><span class="sxs-lookup"><span data-stu-id="6254d-146">Specifies the status.</span></span>
<span data-ttu-id="6254d-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6254d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6254d-148">Executando</span><span class="sxs-lookup"><span data-stu-id="6254d-148">Running</span></span>
- <span data-ttu-id="6254d-149">Feito</span><span class="sxs-lookup"><span data-stu-id="6254d-149">Completed</span></span>
- <span data-ttu-id="6254d-150">Cela</span><span class="sxs-lookup"><span data-stu-id="6254d-150">Cancelled</span></span>
- <span data-ttu-id="6254d-151">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="6254d-151">Failed</span></span>
- <span data-ttu-id="6254d-152">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="6254d-152">Canceling</span></span>
- <span data-ttu-id="6254d-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="6254d-153">CompletedWithErrors</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-154">-To</span><span class="sxs-lookup"><span data-stu-id="6254d-154">-To</span></span>
<span data-ttu-id="6254d-155">Especifica a data e a hora de término dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6254d-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-156">-Digite</span><span class="sxs-lookup"><span data-stu-id="6254d-156">-Type</span></span>
<span data-ttu-id="6254d-157">Especifica o tipo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6254d-157">Specifies the job type.</span></span>
<span data-ttu-id="6254d-158">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6254d-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6254d-159">Fazer</span><span class="sxs-lookup"><span data-stu-id="6254d-159">Backup</span></span>
- <span data-ttu-id="6254d-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="6254d-160">ManualBackup</span></span>
- <span data-ttu-id="6254d-161">Restaurar</span><span class="sxs-lookup"><span data-stu-id="6254d-161">Restore</span></span>
- <span data-ttu-id="6254d-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="6254d-162">CloneWorkflow</span></span>
- <span data-ttu-id="6254d-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="6254d-163">DeviceRestore</span></span>
- <span data-ttu-id="6254d-164">Atualização</span><span class="sxs-lookup"><span data-stu-id="6254d-164">Update</span></span>
- <span data-ttu-id="6254d-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="6254d-165">SupportPackage</span></span>
- <span data-ttu-id="6254d-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="6254d-166">VirtualApplianceProvisioning</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6254d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6254d-167">CommonParameters</span></span>
<span data-ttu-id="6254d-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6254d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6254d-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6254d-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6254d-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6254d-170">INPUTS</span></span>

### <span data-ttu-id="6254d-171">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6254d-171">None</span></span>
<span data-ttu-id="6254d-172">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6254d-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="6254d-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6254d-173">OUTPUTS</span></span>

### <span data-ttu-id="6254d-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="6254d-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="6254d-175">Esse cmdlet retorna uma lista de objetos de detalhes do trabalho ou, se você especificar o parâmetro *InstanceId* , ele retornará um único objeto de detalhes do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6254d-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="6254d-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6254d-176">NOTES</span></span>

## <span data-ttu-id="6254d-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6254d-177">RELATED LINKS</span></span>

[<span data-ttu-id="6254d-178">Parar-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6254d-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


