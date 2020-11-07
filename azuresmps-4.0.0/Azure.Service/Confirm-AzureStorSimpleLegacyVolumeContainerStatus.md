---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945700"
---
# <span data-ttu-id="095b7-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="095b7-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="095b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="095b7-102">SYNOPSIS</span></span>
<span data-ttu-id="095b7-103">Inicia a confirmação ou a reversão dos contêineres de volume que foram migrados.</span><span class="sxs-lookup"><span data-stu-id="095b7-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="095b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="095b7-104">SYNTAX</span></span>

### <span data-ttu-id="095b7-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="095b7-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="095b7-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="095b7-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="095b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="095b7-107">DESCRIPTION</span></span>
<span data-ttu-id="095b7-108">O cmdlet **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** inicia a confirmação ou a reversão dos contêineres de volume que são migrados como parte de uma migração herdada.</span><span class="sxs-lookup"><span data-stu-id="095b7-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="095b7-109">A reversão restaura o aparelho para a propriedade original.</span><span class="sxs-lookup"><span data-stu-id="095b7-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="095b7-110">A confirmação atribui a propriedade ao dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="095b7-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="095b7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="095b7-111">EXAMPLES</span></span>

### <span data-ttu-id="095b7-112">Exemplo 1: iniciar uma operação de confirmação em um contêiner de volume específico</span><span class="sxs-lookup"><span data-stu-id="095b7-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="095b7-113">Esse comando inicia uma operação de confirmação no contêiner de volume especificado para a ID de configuração herdada especificada.</span><span class="sxs-lookup"><span data-stu-id="095b7-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="095b7-114">Para ver o status da operação, use o cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** .</span><span class="sxs-lookup"><span data-stu-id="095b7-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="095b7-115">Exemplo 2: iniciar uma operação de reversão em um contêiner de volume específico</span><span class="sxs-lookup"><span data-stu-id="095b7-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="095b7-116">Esse comando inicia uma operação de reversão no contêiner de volume especificado para a ID de configuração herdada especificada.</span><span class="sxs-lookup"><span data-stu-id="095b7-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="095b7-117">Exemplo 3: iniciar uma operação de confirmação em todos os contêineres de volume</span><span class="sxs-lookup"><span data-stu-id="095b7-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="095b7-118">Esse comando inicia uma operação de confirmação em todo o contêiner de volume para a ID de configuração herdada especificada.</span><span class="sxs-lookup"><span data-stu-id="095b7-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="095b7-119">Exemplo 4: iniciar uma operação de reversão em todos os contêineres de volume</span><span class="sxs-lookup"><span data-stu-id="095b7-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="095b7-120">Esse comando inicia uma operação de reversão em todos os contêineres de volume para a ID de configuração herdada especificada.</span><span class="sxs-lookup"><span data-stu-id="095b7-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="095b7-121">OS</span><span class="sxs-lookup"><span data-stu-id="095b7-121">PARAMETERS</span></span>

### <span data-ttu-id="095b7-122">-Tudo</span><span class="sxs-lookup"><span data-stu-id="095b7-122">-All</span></span>
<span data-ttu-id="095b7-123">Indica que esse cmdlet inicia uma operação de reversão ou confirmação em todos os contêineres de volume no arquivo de configuração importado.</span><span class="sxs-lookup"><span data-stu-id="095b7-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095b7-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="095b7-124">-LegacyConfigId</span></span>
<span data-ttu-id="095b7-125">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="095b7-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="095b7-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="095b7-126">-LegacyContainerNames</span></span>
<span data-ttu-id="095b7-127">Especifica uma matriz de nomes de contêiner de volume para os quais o plano de migração se aplica.</span><span class="sxs-lookup"><span data-stu-id="095b7-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095b7-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="095b7-128">-MigrationOperation</span></span>
<span data-ttu-id="095b7-129">Especifica se esse cmdlet executa uma confirmação ou uma reversão.</span><span class="sxs-lookup"><span data-stu-id="095b7-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="095b7-130">Os valores válidos são: Commit e ROLLBACK.</span><span class="sxs-lookup"><span data-stu-id="095b7-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="095b7-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="095b7-131">-Profile</span></span>
<span data-ttu-id="095b7-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="095b7-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="095b7-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="095b7-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="095b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095b7-134">CommonParameters</span></span>
<span data-ttu-id="095b7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095b7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095b7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095b7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="095b7-137">INPUTS</span></span>

## <span data-ttu-id="095b7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="095b7-138">OUTPUTS</span></span>

## <span data-ttu-id="095b7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="095b7-139">NOTES</span></span>

## <span data-ttu-id="095b7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="095b7-140">RELATED LINKS</span></span>

[<span data-ttu-id="095b7-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="095b7-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="095b7-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="095b7-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="095b7-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="095b7-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


