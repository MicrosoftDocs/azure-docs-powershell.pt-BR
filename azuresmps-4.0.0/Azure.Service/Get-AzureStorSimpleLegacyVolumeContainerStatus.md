---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946550"
---
# <span data-ttu-id="00419-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="00419-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="00419-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00419-102">SYNOPSIS</span></span>
<span data-ttu-id="00419-103">Obtém o status de migração dos contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="00419-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="00419-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00419-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00419-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00419-105">DESCRIPTION</span></span>
<span data-ttu-id="00419-106">O cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** Obtém o status de migração dos contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="00419-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="00419-107">Esse cmdlet retorna informações de status que incluem se a migração do contêiner de volume ainda está em andamento, concluída ou falha.</span><span class="sxs-lookup"><span data-stu-id="00419-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="00419-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00419-108">EXAMPLES</span></span>

### <span data-ttu-id="00419-109">Exemplo 1: obter o status de uma migração com falha</span><span class="sxs-lookup"><span data-stu-id="00419-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="00419-110">Esse comando obtém o status de migração para o contêiner herdado nomeado.</span><span class="sxs-lookup"><span data-stu-id="00419-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="00419-111">Os resultados mostram que houve falha na migração.</span><span class="sxs-lookup"><span data-stu-id="00419-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="00419-112">Exemplo 2: obter status para uma migração em andamento</span><span class="sxs-lookup"><span data-stu-id="00419-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="00419-113">Esse comando obtém o status de migração para o contêiner herdado nomeado.</span><span class="sxs-lookup"><span data-stu-id="00419-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="00419-114">Os resultados mostram que a migração está em andamento.</span><span class="sxs-lookup"><span data-stu-id="00419-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="00419-115">Exemplo 3: obter o status de uma migração concluída</span><span class="sxs-lookup"><span data-stu-id="00419-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="00419-116">Esse comando obtém o status de migração para o contêiner herdado nomeado.</span><span class="sxs-lookup"><span data-stu-id="00419-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="00419-117">Os resultados mostram que a migração foi concluída.</span><span class="sxs-lookup"><span data-stu-id="00419-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="00419-118">OS</span><span class="sxs-lookup"><span data-stu-id="00419-118">PARAMETERS</span></span>

### <span data-ttu-id="00419-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="00419-119">-LegacyConfigId</span></span>
<span data-ttu-id="00419-120">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="00419-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="00419-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="00419-121">-LegacyContainerNames</span></span>
<span data-ttu-id="00419-122">Especifica uma matriz de nomes de contêiner de volume para os quais o plano de migração se aplica.</span><span class="sxs-lookup"><span data-stu-id="00419-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00419-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="00419-123">-Profile</span></span>
<span data-ttu-id="00419-124">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="00419-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="00419-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00419-125">CommonParameters</span></span>
<span data-ttu-id="00419-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00419-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00419-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00419-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00419-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00419-128">INPUTS</span></span>

## <span data-ttu-id="00419-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00419-129">OUTPUTS</span></span>

## <span data-ttu-id="00419-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00419-130">NOTES</span></span>

## <span data-ttu-id="00419-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00419-131">RELATED LINKS</span></span>

[<span data-ttu-id="00419-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="00419-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="00419-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="00419-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


