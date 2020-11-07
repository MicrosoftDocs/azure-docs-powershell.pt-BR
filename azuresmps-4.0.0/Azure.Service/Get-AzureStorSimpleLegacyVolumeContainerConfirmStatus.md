---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946553"
---
# <span data-ttu-id="cbe09-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="cbe09-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="cbe09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbe09-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe09-103">Obtém o status de uma operação de confirmação ou reversão.</span><span class="sxs-lookup"><span data-stu-id="cbe09-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="cbe09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbe09-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cbe09-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbe09-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe09-106">O cmdlet **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** Obtém o status da operação de confirmação ou reversão.</span><span class="sxs-lookup"><span data-stu-id="cbe09-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="cbe09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbe09-107">EXAMPLES</span></span>

### <span data-ttu-id="cbe09-108">Exemplo 1: obter o status de uma operação de confirmação completa</span><span class="sxs-lookup"><span data-stu-id="cbe09-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="cbe09-109">Esse comando obtém o status de uma operação de confirmação para o contêiner nomeado.</span><span class="sxs-lookup"><span data-stu-id="cbe09-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="cbe09-110">Esta operação tem um status concluído.</span><span class="sxs-lookup"><span data-stu-id="cbe09-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="cbe09-111">Exemplo 2: obter o status de uma operação de reversão concluída</span><span class="sxs-lookup"><span data-stu-id="cbe09-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="cbe09-112">Esse comando obtém o status de uma operação de reversão para o contêiner nomeado.</span><span class="sxs-lookup"><span data-stu-id="cbe09-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="cbe09-113">Esta operação tem um status concluído.</span><span class="sxs-lookup"><span data-stu-id="cbe09-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="cbe09-114">OS</span><span class="sxs-lookup"><span data-stu-id="cbe09-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe09-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="cbe09-115">-LegacyConfigId</span></span>
<span data-ttu-id="cbe09-116">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="cbe09-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="cbe09-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="cbe09-117">-LegacyContainerNames</span></span>
<span data-ttu-id="cbe09-118">Especifica uma matriz de nomes de contêiner de volume para os quais o plano de migração se aplica.</span><span class="sxs-lookup"><span data-stu-id="cbe09-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="cbe09-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cbe09-119">-Profile</span></span>
<span data-ttu-id="cbe09-120">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe09-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cbe09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe09-121">CommonParameters</span></span>
<span data-ttu-id="cbe09-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe09-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe09-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe09-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbe09-124">INPUTS</span></span>

### <span data-ttu-id="cbe09-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cbe09-125">None</span></span>

## <span data-ttu-id="cbe09-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbe09-126">OUTPUTS</span></span>

### <span data-ttu-id="cbe09-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="cbe09-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="cbe09-128">Esse cmdlet retorna o status da operação de confirmação de migração que é executada.</span><span class="sxs-lookup"><span data-stu-id="cbe09-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="cbe09-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbe09-129">NOTES</span></span>

## <span data-ttu-id="cbe09-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbe09-130">RELATED LINKS</span></span>

[<span data-ttu-id="cbe09-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="cbe09-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="cbe09-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="cbe09-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


