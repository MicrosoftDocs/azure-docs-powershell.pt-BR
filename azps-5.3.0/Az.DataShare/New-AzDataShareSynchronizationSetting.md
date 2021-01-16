---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271467"
---
# <span data-ttu-id="d9220-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d9220-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d9220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9220-102">SYNOPSIS</span></span>
<span data-ttu-id="d9220-103">Cria uma configuração de sincronização para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d9220-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="d9220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9220-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9220-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9220-105">DESCRIPTION</span></span>
<span data-ttu-id="d9220-106">O **New-AzDataShareSynchronizationSetting** cria uma configuração de sincronização para compartilhamento de conta de compartilhamento para um intervalo de recorrência de diária ou de hora em uma hora específica.</span><span class="sxs-lookup"><span data-stu-id="d9220-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="d9220-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9220-107">EXAMPLES</span></span>

### <span data-ttu-id="d9220-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9220-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="d9220-109">Esses comandos criam uma configuração de sincronização no intervalo de recorrência diária em 9:00 AM para share AdsShare no WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="d9220-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="d9220-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9220-110">PARAMETERS</span></span>

### <span data-ttu-id="d9220-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9220-111">-AccountName</span></span>
<span data-ttu-id="d9220-112">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d9220-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9220-113">-DefaultProfile</span></span>
<span data-ttu-id="d9220-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9220-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9220-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9220-115">-Name</span></span>
<span data-ttu-id="d9220-116">Nome da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="d9220-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="d9220-117">-RecurrenceInterval</span></span>
<span data-ttu-id="d9220-118">O intervalo de recorrência da configuração de sincronização (dia ou hora)</span><span class="sxs-lookup"><span data-stu-id="d9220-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9220-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9220-120">Nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d9220-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d9220-121">-ShareName</span></span>
<span data-ttu-id="d9220-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d9220-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-123">-Synchronizationtime</span><span class="sxs-lookup"><span data-stu-id="d9220-123">-SynchronizationTime</span></span>
<span data-ttu-id="d9220-124">A hora de início da configuração de sincronização agendada</span><span class="sxs-lookup"><span data-stu-id="d9220-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9220-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9220-125">-Confirm</span></span>
<span data-ttu-id="d9220-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9220-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9220-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9220-127">-WhatIf</span></span>
<span data-ttu-id="d9220-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9220-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9220-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9220-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9220-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9220-130">CommonParameters</span></span>
<span data-ttu-id="d9220-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9220-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9220-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9220-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9220-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9220-133">INPUTS</span></span>

### <span data-ttu-id="d9220-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d9220-134">None</span></span>

## <span data-ttu-id="d9220-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9220-135">OUTPUTS</span></span>

### <span data-ttu-id="d9220-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d9220-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d9220-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9220-137">NOTES</span></span>

## <span data-ttu-id="d9220-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9220-138">RELATED LINKS</span></span>
