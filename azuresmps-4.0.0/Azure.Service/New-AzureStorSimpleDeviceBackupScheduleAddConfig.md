---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945528"
---
# <span data-ttu-id="4b4b9-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="4b4b9-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="4b4b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4b9-103">Cria um objeto de configuração de agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="4b4b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b4b9-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b4b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4b9-106">O cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cria um objeto de configuração **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="4b4b9-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="4b4b9-107">Use este objeto de configuração para criar uma nova política de backup usando o cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="4b4b9-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="4b4b9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b4b9-108">EXAMPLES</span></span>

### <span data-ttu-id="4b4b9-109">Exemplo 1: criar um objeto de configuração de backup</span><span class="sxs-lookup"><span data-stu-id="4b4b9-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="4b4b9-110">Esse comando cria um objeto base de agendamento de backup para backups de instantâneo na nuvem.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="4b4b9-111">O backup ocorre todos os dias, e os backups são mantidos por 100 dias.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="4b4b9-112">Este cronograma está habilitado do tempo padrão, que é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="4b4b9-113">OS</span><span class="sxs-lookup"><span data-stu-id="4b4b9-113">PARAMETERS</span></span>

### <span data-ttu-id="4b4b9-114">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="4b4b9-114">-BackupType</span></span>
<span data-ttu-id="4b4b9-115">Especifica o tipo de backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-115">Specifies the backup type.</span></span>
<span data-ttu-id="4b4b9-116">Os valores válidos são: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="4b4b9-117">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="4b4b9-117">-Enabled</span></span>
<span data-ttu-id="4b4b9-118">Indica se o agendamento de backup deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b4b9-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4b4b9-119">-Profile</span></span>
<span data-ttu-id="4b4b9-120">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4b4b9-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="4b4b9-121">-RecurrenceType</span></span>
<span data-ttu-id="4b4b9-122">Especifica o tipo de recorrência para este agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="4b4b9-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="4b4b9-123">Valid values are:</span></span> 

- <span data-ttu-id="4b4b9-124">Minutos</span><span class="sxs-lookup"><span data-stu-id="4b4b9-124">Minutes</span></span>
- <span data-ttu-id="4b4b9-125">Por hora</span><span class="sxs-lookup"><span data-stu-id="4b4b9-125">Hourly</span></span>
- <span data-ttu-id="4b4b9-126">Daily</span><span class="sxs-lookup"><span data-stu-id="4b4b9-126">Daily</span></span>
- <span data-ttu-id="4b4b9-127">Mensal</span><span class="sxs-lookup"><span data-stu-id="4b4b9-127">Weekly</span></span>

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

### <span data-ttu-id="4b4b9-128">-Recorrência</span><span class="sxs-lookup"><span data-stu-id="4b4b9-128">-RecurrenceValue</span></span>
<span data-ttu-id="4b4b9-129">Especifica com que frequência fazer um backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="4b4b9-130">Esse parâmetro usa a unidade especificada pelo parâmetro *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="4b4b9-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="4b4b9-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="4b4b9-131">-RetentionCount</span></span>
<span data-ttu-id="4b4b9-132">Especifica o número de dias para manter um backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="4b4b9-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="4b4b9-133">-StartFromDateTime</span></span>
<span data-ttu-id="4b4b9-134">Especifica a data a partir da qual começar a fazer backups.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="4b4b9-135">O valor padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="4b4b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4b9-136">CommonParameters</span></span>
<span data-ttu-id="4b4b9-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4b9-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4b9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4b9-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b4b9-139">INPUTS</span></span>

### <span data-ttu-id="4b4b9-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b4b9-140">None</span></span>

## <span data-ttu-id="4b4b9-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b4b9-141">OUTPUTS</span></span>

### <span data-ttu-id="4b4b9-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="4b4b9-142">BackupScheduleBase</span></span>
<span data-ttu-id="4b4b9-143">Esse cmdlet retorna um objeto **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="4b4b9-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="4b4b9-144">Use um **BackupScheduleBase** para construir uma nova política de backup.</span><span class="sxs-lookup"><span data-stu-id="4b4b9-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="4b4b9-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b4b9-145">NOTES</span></span>

## <span data-ttu-id="4b4b9-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b4b9-146">RELATED LINKS</span></span>

[<span data-ttu-id="4b4b9-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4b4b9-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="4b4b9-148">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4b4b9-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


