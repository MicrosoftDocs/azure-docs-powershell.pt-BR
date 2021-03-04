---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891193"
---
# <span data-ttu-id="48034-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="48034-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="48034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48034-102">SYNOPSIS</span></span>
<span data-ttu-id="48034-103">Cria a configuração de sincronização para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="48034-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="48034-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="48034-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48034-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="48034-105">DESCRIPTION</span></span>
<span data-ttu-id="48034-106">O **New-AzDataShareSynchronizationSetting** cria uma configuração de sincronização para compartilhamento na conta de compartilhamento para um intervalo de recorrência diário ou por hora em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="48034-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="48034-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48034-107">EXAMPLES</span></span>

### <span data-ttu-id="48034-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48034-108">Example 1</span></span>
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

<span data-ttu-id="48034-109">Esses comandos criam uma configuração de sincronização no intervalo de recorrência diária às 9:00 para compartilhar AdsShare na conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="48034-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="48034-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="48034-110">PARAMETERS</span></span>

### <span data-ttu-id="48034-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48034-111">-AccountName</span></span>
<span data-ttu-id="48034-112">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="48034-112">Azure data share account name</span></span>

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

### <span data-ttu-id="48034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48034-113">-DefaultProfile</span></span>
<span data-ttu-id="48034-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48034-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48034-115">-Name</span><span class="sxs-lookup"><span data-stu-id="48034-115">-Name</span></span>
<span data-ttu-id="48034-116">Nome da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="48034-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="48034-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="48034-117">-RecurrenceInterval</span></span>
<span data-ttu-id="48034-118">O intervalo de recorrência para a configuração de sincronização (Dia ou Hora)</span><span class="sxs-lookup"><span data-stu-id="48034-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="48034-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48034-119">-ResourceGroupName</span></span>
<span data-ttu-id="48034-120">Nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="48034-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="48034-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="48034-121">-ShareName</span></span>
<span data-ttu-id="48034-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="48034-122">Azure data share name</span></span>

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

### <span data-ttu-id="48034-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="48034-123">-SynchronizationTime</span></span>
<span data-ttu-id="48034-124">A hora de início da configuração de sincronização agendada</span><span class="sxs-lookup"><span data-stu-id="48034-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="48034-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48034-125">-Confirm</span></span>
<span data-ttu-id="48034-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48034-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48034-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48034-127">-WhatIf</span></span>
<span data-ttu-id="48034-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48034-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48034-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48034-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48034-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48034-130">CommonParameters</span></span>
<span data-ttu-id="48034-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48034-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48034-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48034-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48034-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48034-133">INPUTS</span></span>

### <span data-ttu-id="48034-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="48034-134">None</span></span>

## <span data-ttu-id="48034-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="48034-135">OUTPUTS</span></span>

### <span data-ttu-id="48034-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="48034-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="48034-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="48034-137">NOTES</span></span>

## <span data-ttu-id="48034-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48034-138">RELATED LINKS</span></span>
