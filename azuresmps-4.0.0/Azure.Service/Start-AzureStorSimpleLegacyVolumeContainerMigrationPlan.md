---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945773"
---
# <span data-ttu-id="e8f09-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="e8f09-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="e8f09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8f09-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f09-103">Inicia a criação de um plano de migração.</span><span class="sxs-lookup"><span data-stu-id="e8f09-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="e8f09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8f09-104">SYNTAX</span></span>

### <span data-ttu-id="e8f09-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="e8f09-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8f09-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="e8f09-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8f09-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8f09-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f09-108">O cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** inicia a criação de um plano de migração.</span><span class="sxs-lookup"><span data-stu-id="e8f09-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="e8f09-109">A criação de um plano de migração é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e8f09-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="e8f09-110">Para ver o status do plano de migração, use o cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .</span><span class="sxs-lookup"><span data-stu-id="e8f09-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="e8f09-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8f09-111">EXAMPLES</span></span>

### <span data-ttu-id="e8f09-112">Exemplo 1: iniciar um plano de migração</span><span class="sxs-lookup"><span data-stu-id="e8f09-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="e8f09-113">Esse comando inicia a criação de um plano de migração para o contêiner herdado chamado OneSDKAzureCloud.</span><span class="sxs-lookup"><span data-stu-id="e8f09-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="e8f09-114">O comando retorna uma mensagem sobre o status do plano e usar o cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** para obter informações atualizadas sobre a data.</span><span class="sxs-lookup"><span data-stu-id="e8f09-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="e8f09-115">Exemplo 2: iniciar o plano de migração para todos os contêineres de volume</span><span class="sxs-lookup"><span data-stu-id="e8f09-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="e8f09-116">Esse comando inicia a criação do plano de migração para todos os contêineres de volume herdados no arquivo de configuração que é importado.</span><span class="sxs-lookup"><span data-stu-id="e8f09-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="e8f09-117">OS</span><span class="sxs-lookup"><span data-stu-id="e8f09-117">PARAMETERS</span></span>

### <span data-ttu-id="e8f09-118">-Tudo</span><span class="sxs-lookup"><span data-stu-id="e8f09-118">-All</span></span>
<span data-ttu-id="e8f09-119">Indica que esse cmdlet inicia estimativas do tempo de migração para todos os contêineres de volume no arquivo de configuração importado.</span><span class="sxs-lookup"><span data-stu-id="e8f09-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="e8f09-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="e8f09-120">-LegacyConfigId</span></span>
<span data-ttu-id="e8f09-121">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="e8f09-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="e8f09-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="e8f09-122">-LegacyContainerNames</span></span>
<span data-ttu-id="e8f09-123">Especifica uma matriz de nomes de contêineres de volume para os quais criar um plano de migração.</span><span class="sxs-lookup"><span data-stu-id="e8f09-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="e8f09-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e8f09-124">-Profile</span></span>
<span data-ttu-id="e8f09-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e8f09-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8f09-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e8f09-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8f09-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f09-127">CommonParameters</span></span>
<span data-ttu-id="e8f09-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f09-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f09-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f09-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f09-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8f09-130">INPUTS</span></span>

### <span data-ttu-id="e8f09-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e8f09-131">None</span></span>

## <span data-ttu-id="e8f09-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8f09-132">OUTPUTS</span></span>

### <span data-ttu-id="e8f09-133">String</span><span class="sxs-lookup"><span data-stu-id="e8f09-133">String</span></span>
<span data-ttu-id="e8f09-134">Esse cmdlet retornará o status do trabalho do plano de migração se ele tiver sido iniciado com êxito no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8f09-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="e8f09-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8f09-135">NOTES</span></span>

## <span data-ttu-id="e8f09-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8f09-136">RELATED LINKS</span></span>

[<span data-ttu-id="e8f09-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="e8f09-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


