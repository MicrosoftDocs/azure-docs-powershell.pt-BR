---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946290"
---
# <span data-ttu-id="57503-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="57503-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="57503-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57503-102">SYNOPSIS</span></span>
<span data-ttu-id="57503-103">Obtém backups de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57503-103">Gets backups from a device.</span></span>

## <span data-ttu-id="57503-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57503-104">SYNTAX</span></span>

### <span data-ttu-id="57503-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="57503-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57503-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="57503-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57503-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="57503-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57503-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="57503-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57503-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="57503-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57503-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57503-110">DESCRIPTION</span></span>
<span data-ttu-id="57503-111">O cmdlet **Get-AzureStorSimpleDeviceBackup** Obtém backups de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57503-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="57503-112">Você pode especificar a política de backup, o volume e o tempo de criação dos backups.</span><span class="sxs-lookup"><span data-stu-id="57503-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="57503-113">Esse cmdlet pode retornar um máximo de 100 backups na primeira página.</span><span class="sxs-lookup"><span data-stu-id="57503-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="57503-114">Se houver mais de 100 backups, recupere páginas subsequentes usando os parâmetros *First* e *Skip* .</span><span class="sxs-lookup"><span data-stu-id="57503-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="57503-115">Se você especificar um valor de 100 para *Skip* e 50 para *primeiro* , esse cmdlet não retornará os primeiros resultados de 100.</span><span class="sxs-lookup"><span data-stu-id="57503-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="57503-116">Ele retorna os próximos 50 resultados após o 100 que ele ignora.</span><span class="sxs-lookup"><span data-stu-id="57503-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="57503-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57503-117">EXAMPLES</span></span>

### <span data-ttu-id="57503-118">Exemplo 1: obter todos os backups em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="57503-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="57503-119">Esse comando obtém todos os backups que existem no dispositivo chamado Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="57503-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="57503-120">Se houver mais do que o máximo de 100 backups permitidos para a primeira página, use os parâmetros *First* e *Skip* para exibir resultados adicionais.</span><span class="sxs-lookup"><span data-stu-id="57503-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="57503-121">Exemplo 2: obter backups criados entre duas datas</span><span class="sxs-lookup"><span data-stu-id="57503-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="57503-122">Este comando obtém backups no dispositivo nomeado Contoso63-AppVm que foram criados em ou após 10/7/2014 e em ou antes de 10/8/2014.</span><span class="sxs-lookup"><span data-stu-id="57503-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="57503-123">Esse cmdlet ignora o primeiro resultado e retorna os dois primeiros resultados após o primeiro resultado.</span><span class="sxs-lookup"><span data-stu-id="57503-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="57503-124">Modifique os valores do *primeiro* e *pule* para exibir outros resultados.</span><span class="sxs-lookup"><span data-stu-id="57503-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="57503-125">Exemplo 3: obter backups de uma ID de política de backup</span><span class="sxs-lookup"><span data-stu-id="57503-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="57503-126">Esse comando obtém backups no dispositivo chamado Contoso63-AppVm criado em ou antes da data especificada.</span><span class="sxs-lookup"><span data-stu-id="57503-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="57503-127">O comando obtém os backups que foram criados usando a política de backup com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="57503-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="57503-128">Esse comando especifica o *primeiro* parâmetro, portanto, retorna apenas os 10 primeiros resultados.</span><span class="sxs-lookup"><span data-stu-id="57503-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="57503-129">Exemplo 4: obter backups para um objeto de política de backup</span><span class="sxs-lookup"><span data-stu-id="57503-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="57503-130">Esse comando obtém um objeto **BackupPolicyDetails** usando o cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** e, em seguida, passa esse objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="57503-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="57503-131">Esse cmdlet obtém backups para o dispositivo chamado Contoso63-AppVm criado usando a política de backup da primeira parte do comando.</span><span class="sxs-lookup"><span data-stu-id="57503-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="57503-132">O comando obtém os backups criados em ou antes da data especificada, exatamente como no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="57503-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="57503-133">Esse comando retorna apenas os 10 primeiros resultados.</span><span class="sxs-lookup"><span data-stu-id="57503-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="57503-134">Exemplo 5: obter um backup para uma ID de volume</span><span class="sxs-lookup"><span data-stu-id="57503-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="57503-135">Esse comando obtém um backup no dispositivo criado no volume que tem a ID de instância especificada.</span><span class="sxs-lookup"><span data-stu-id="57503-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="57503-136">Esse comando especifica o *primeiro* parâmetro e, portanto, retorna somente o primeiro resultado.</span><span class="sxs-lookup"><span data-stu-id="57503-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="57503-137">Exemplo 6: obter um backup para um nome de volume</span><span class="sxs-lookup"><span data-stu-id="57503-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="57503-138">Esse comando obtém um objeto **VirtualDisk** usando o cmdlet **Get-AzureStorSimpleDeviceVolume** e, em seguida, passa esse objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="57503-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="57503-139">Esse cmdlet obtém backups para o dispositivo chamado Contoso63-AppVm criado no volume da primeira parte do comando.</span><span class="sxs-lookup"><span data-stu-id="57503-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="57503-140">Esse comando retorna apenas o primeiro resultado.</span><span class="sxs-lookup"><span data-stu-id="57503-140">This command returns only the first result.</span></span>

## <span data-ttu-id="57503-141">OS</span><span class="sxs-lookup"><span data-stu-id="57503-141">PARAMETERS</span></span>

### <span data-ttu-id="57503-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="57503-142">-BackupPolicy</span></span>
<span data-ttu-id="57503-143">Especifica um objeto **BackupPolicyDetails** .</span><span class="sxs-lookup"><span data-stu-id="57503-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="57503-144">Esse cmdlet usa a **InstanceId** desse objeto para determinar quais backups obter.</span><span class="sxs-lookup"><span data-stu-id="57503-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="57503-145">Para obter um objeto **BackupPolicyDetails** , use o cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="57503-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57503-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="57503-146">-BackupPolicyId</span></span>
<span data-ttu-id="57503-147">Especifica uma ID de instância de uma política de backup.</span><span class="sxs-lookup"><span data-stu-id="57503-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="57503-148">Este cmdlet obtém backups de dispositivos para a política que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="57503-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57503-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="57503-149">-DeviceName</span></span>
<span data-ttu-id="57503-150">Especifica o nome do dispositivo StorSimple para o qual obter backups.</span><span class="sxs-lookup"><span data-stu-id="57503-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57503-151">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="57503-151">-First</span></span>
<span data-ttu-id="57503-152">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="57503-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="57503-153">Digite o número de objetos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="57503-153">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="57503-154">-De</span><span class="sxs-lookup"><span data-stu-id="57503-154">-From</span></span>
<span data-ttu-id="57503-155">Especifica a data e a hora de início dos backups que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="57503-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57503-156">-Perfil</span><span class="sxs-lookup"><span data-stu-id="57503-156">-Profile</span></span>
<span data-ttu-id="57503-157">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="57503-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="57503-158">-Skip</span><span class="sxs-lookup"><span data-stu-id="57503-158">-Skip</span></span>
<span data-ttu-id="57503-159">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="57503-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="57503-160">Digite o número de objetos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="57503-160">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="57503-161">-To</span><span class="sxs-lookup"><span data-stu-id="57503-161">-To</span></span>
<span data-ttu-id="57503-162">Especifica a data e a hora de término dos backups que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="57503-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57503-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="57503-163">-Volume</span></span>
<span data-ttu-id="57503-164">Especifica um objeto **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="57503-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="57503-165">Esse cmdlet usa a **InstanceId** desse objeto para determinar o volume no qual os backups existem.</span><span class="sxs-lookup"><span data-stu-id="57503-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="57503-166">Para obter um objeto **VirtualDisk** , use o parâmetro **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="57503-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57503-167">-VolumeID</span><span class="sxs-lookup"><span data-stu-id="57503-167">-VolumeId</span></span>
<span data-ttu-id="57503-168">Especifica a ID de instância do volume em que existem backups.</span><span class="sxs-lookup"><span data-stu-id="57503-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57503-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57503-169">CommonParameters</span></span>
<span data-ttu-id="57503-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57503-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57503-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57503-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57503-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57503-172">INPUTS</span></span>

### <span data-ttu-id="57503-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="57503-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="57503-174">Esse cmdlet aceita objetos **BackupPolicyDetails** e **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="57503-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="57503-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57503-175">OUTPUTS</span></span>

### <span data-ttu-id="57503-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="57503-176">IList\<Backup\></span></span>
<span data-ttu-id="57503-177">Esse cmdlet retorna uma lista de objetos de **backup** .</span><span class="sxs-lookup"><span data-stu-id="57503-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="57503-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57503-178">NOTES</span></span>

## <span data-ttu-id="57503-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57503-179">RELATED LINKS</span></span>

[<span data-ttu-id="57503-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="57503-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="57503-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="57503-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="57503-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="57503-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


