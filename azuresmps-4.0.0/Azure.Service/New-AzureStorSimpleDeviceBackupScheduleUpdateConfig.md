---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945524"
---
# <span data-ttu-id="3febc-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3febc-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="3febc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3febc-102">SYNOPSIS</span></span>
<span data-ttu-id="3febc-103">Cria um objeto de configuração de atualização de agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="3febc-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="3febc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3febc-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3febc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3febc-105">DESCRIPTION</span></span>
<span data-ttu-id="3febc-106">O cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cria um objeto de configuração **BackupScheduleUpdateRequest** .</span><span class="sxs-lookup"><span data-stu-id="3febc-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="3febc-107">Use este objeto de configuração para atualizar uma política de backup usando o cmdlet **set-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3febc-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="3febc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3febc-108">EXAMPLES</span></span>

### <span data-ttu-id="3febc-109">Exemplo 1: criar uma solicitação de atualização de agendamento</span><span class="sxs-lookup"><span data-stu-id="3febc-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="3febc-110">Esse comando cria uma solicitação de atualização de agendamento de backup para o cronograma que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="3febc-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="3febc-111">A solicitação é fazer o cronograma de um backup de instantâneo na nuvem que se repete a cada hora.</span><span class="sxs-lookup"><span data-stu-id="3febc-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="3febc-112">Os backups são mantidos por 50 dias.</span><span class="sxs-lookup"><span data-stu-id="3febc-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="3febc-113">Este cronograma está habilitado do tempo padrão, que é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="3febc-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="3febc-114">OS</span><span class="sxs-lookup"><span data-stu-id="3febc-114">PARAMETERS</span></span>

### <span data-ttu-id="3febc-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="3febc-115">-BackupType</span></span>
<span data-ttu-id="3febc-116">Especifica o tipo de backup.</span><span class="sxs-lookup"><span data-stu-id="3febc-116">Specifies the backup type.</span></span>
<span data-ttu-id="3febc-117">Os valores válidos são: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="3febc-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="3febc-118">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="3febc-118">-Enabled</span></span>
<span data-ttu-id="3febc-119">Indica se o agendamento de backup deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="3febc-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3febc-120">-ID</span><span class="sxs-lookup"><span data-stu-id="3febc-120">-Id</span></span>
<span data-ttu-id="3febc-121">Especifica a ID da instância do agendamento de backup a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3febc-121">Specifies the instance ID of the backup schedule to update.</span></span>

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

### <span data-ttu-id="3febc-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3febc-122">-Profile</span></span>
<span data-ttu-id="3febc-123">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="3febc-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3febc-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="3febc-124">-RecurrenceType</span></span>
<span data-ttu-id="3febc-125">Especifica o tipo de recorrência para este agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="3febc-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="3febc-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3febc-126">Valid values are:</span></span> 

- <span data-ttu-id="3febc-127">Minutos</span><span class="sxs-lookup"><span data-stu-id="3febc-127">Minutes</span></span>
- <span data-ttu-id="3febc-128">Por hora</span><span class="sxs-lookup"><span data-stu-id="3febc-128">Hourly</span></span>
- <span data-ttu-id="3febc-129">Daily</span><span class="sxs-lookup"><span data-stu-id="3febc-129">Daily</span></span>
- <span data-ttu-id="3febc-130">Mensal</span><span class="sxs-lookup"><span data-stu-id="3febc-130">Weekly</span></span>

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

### <span data-ttu-id="3febc-131">-Recorrência</span><span class="sxs-lookup"><span data-stu-id="3febc-131">-RecurrenceValue</span></span>
<span data-ttu-id="3febc-132">Especifica com que frequência fazer um backup.</span><span class="sxs-lookup"><span data-stu-id="3febc-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="3febc-133">Esse parâmetro usa a unidade especificada pelo parâmetro *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="3febc-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3febc-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="3febc-134">-RetentionCount</span></span>
<span data-ttu-id="3febc-135">Especifica o número de dias para manter um backup.</span><span class="sxs-lookup"><span data-stu-id="3febc-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3febc-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="3febc-136">-StartFromDateTime</span></span>
<span data-ttu-id="3febc-137">Especifica a data a partir da qual começar a fazer backups.</span><span class="sxs-lookup"><span data-stu-id="3febc-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="3febc-138">O valor padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="3febc-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="3febc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3febc-139">CommonParameters</span></span>
<span data-ttu-id="3febc-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3febc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3febc-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3febc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3febc-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3febc-142">INPUTS</span></span>

### <span data-ttu-id="3febc-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3febc-143">None</span></span>

## <span data-ttu-id="3febc-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3febc-144">OUTPUTS</span></span>

### <span data-ttu-id="3febc-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="3febc-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="3febc-146">Esse cmdlet retorna um objeto **BackupScheduleUpdateRequest** que contém informações sobre agendas de backup atualizadas.</span><span class="sxs-lookup"><span data-stu-id="3febc-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="3febc-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3febc-147">NOTES</span></span>

## <span data-ttu-id="3febc-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3febc-148">RELATED LINKS</span></span>

[<span data-ttu-id="3febc-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="3febc-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="3febc-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3febc-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


