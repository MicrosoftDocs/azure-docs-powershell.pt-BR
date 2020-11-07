---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945556"
---
# <span data-ttu-id="f07dd-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="f07dd-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="f07dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f07dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f07dd-103">Obtém planos de migração para contêineres herdados.</span><span class="sxs-lookup"><span data-stu-id="f07dd-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="f07dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f07dd-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f07dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f07dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f07dd-106">O cmdlet **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** Obtém planos de migração para contêineres herdados.</span><span class="sxs-lookup"><span data-stu-id="f07dd-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="f07dd-107">Especifique um plano de migração por sua ID de configuração herdada.</span><span class="sxs-lookup"><span data-stu-id="f07dd-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="f07dd-108">Se a criação do plano de migração ainda estiver em andamento, esse cmdlet obtém o status do plano de migração.</span><span class="sxs-lookup"><span data-stu-id="f07dd-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="f07dd-109">Se o plano de migração estiver concluído, esse cmdlet retornará o plano de migração real para o conjunto de contêineres herdados.</span><span class="sxs-lookup"><span data-stu-id="f07dd-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="f07dd-110">Se você não especificar o parâmetro *LegacyConfigId* , esse cmdlet retornará uma lista de IDs de configuração.</span><span class="sxs-lookup"><span data-stu-id="f07dd-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="f07dd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f07dd-111">EXAMPLES</span></span>

### <span data-ttu-id="f07dd-112">Exemplo 1: obter o status de um plano</span><span class="sxs-lookup"><span data-stu-id="f07dd-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="f07dd-113">Esse comando obtém o status do plano de migração.</span><span class="sxs-lookup"><span data-stu-id="f07dd-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="f07dd-114">O status inclui a largura de banda presumida, o tempo estimado e as informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f07dd-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="f07dd-115">Exemplo 2: obter as IDs dos planos existentes</span><span class="sxs-lookup"><span data-stu-id="f07dd-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="f07dd-116">Esse comando obtém todas as IDs de configuração dos planos de migração.</span><span class="sxs-lookup"><span data-stu-id="f07dd-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="f07dd-117">OS</span><span class="sxs-lookup"><span data-stu-id="f07dd-117">PARAMETERS</span></span>

### <span data-ttu-id="f07dd-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="f07dd-118">-LegacyConfigId</span></span>
<span data-ttu-id="f07dd-119">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="f07dd-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="f07dd-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="f07dd-120">-LegacyContainerNames</span></span>
<span data-ttu-id="f07dd-121">Especifica uma matriz de nomes de contêiner de volume para os quais este cmdlet obtém um plano de migração.</span><span class="sxs-lookup"><span data-stu-id="f07dd-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="f07dd-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f07dd-122">-Profile</span></span>
<span data-ttu-id="f07dd-123">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="f07dd-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f07dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07dd-124">CommonParameters</span></span>
<span data-ttu-id="f07dd-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07dd-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07dd-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f07dd-127">INPUTS</span></span>

### <span data-ttu-id="f07dd-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f07dd-128">None</span></span>

## <span data-ttu-id="f07dd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f07dd-129">OUTPUTS</span></span>

### <span data-ttu-id="f07dd-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="f07dd-130">MigrationPlanMsg</span></span>
<span data-ttu-id="f07dd-131">Esse cmdlet retorna um objeto **MigrationPlanMsg** que contém o status do trabalho do plano de migração, a largura de banda presumida em megabits por segundo e o tempo estimado em minutos.</span><span class="sxs-lookup"><span data-stu-id="f07dd-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="f07dd-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f07dd-132">NOTES</span></span>

## <span data-ttu-id="f07dd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f07dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="f07dd-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="f07dd-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


