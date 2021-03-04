---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: fe082dc38f8a16dcca897623c4817d728fdaf3c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886978"
---
# <span data-ttu-id="71e4e-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="71e4e-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="71e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="71e4e-103">Cria um gatilho para a assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="71e4e-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="71e4e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71e4e-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e4e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="71e4e-106">O cmdlet **New-AzDataShareTrigger** cria um gatilho para a assinatura de compartilhamento para o intervalo de recorrência especificado e o tempo de sincronização na conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="71e4e-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="71e4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71e4e-107">EXAMPLES</span></span>

### <span data-ttu-id="71e4e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71e4e-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="71e4e-109">Este comando cria um novo gatilho AdsTrigger para a assinatura de compartilhamento AdsShareSubscription com um intervalo de recorrência diário de 9 horas.</span><span class="sxs-lookup"><span data-stu-id="71e4e-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="71e4e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71e4e-110">PARAMETERS</span></span>

### <span data-ttu-id="71e4e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71e4e-111">-AccountName</span></span>
<span data-ttu-id="71e4e-112">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="71e4e-112">Azure data share account name</span></span>

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

### <span data-ttu-id="71e4e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71e4e-113">-AsJob</span></span>
<span data-ttu-id="71e4e-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="71e4e-114">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e4e-115">-DefaultProfile</span></span>
<span data-ttu-id="71e4e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71e4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e4e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71e4e-117">-Name</span></span>
<span data-ttu-id="71e4e-118">Nome do gatilho de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="71e4e-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="71e4e-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="71e4e-119">-RecurrenceInterval</span></span>
<span data-ttu-id="71e4e-120">O intervalo de recorrência para o gatilho (Dia ou Hora)</span><span class="sxs-lookup"><span data-stu-id="71e4e-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="71e4e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e4e-121">-ResourceGroupName</span></span>
<span data-ttu-id="71e4e-122">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="71e4e-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="71e4e-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="71e4e-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="71e4e-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="71e4e-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e4e-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="71e4e-125">-SynchronizationTime</span></span>
<span data-ttu-id="71e4e-126">A hora de início da sincronização agendada para o gatilho</span><span class="sxs-lookup"><span data-stu-id="71e4e-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="71e4e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71e4e-127">-Confirm</span></span>
<span data-ttu-id="71e4e-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e4e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e4e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e4e-129">-WhatIf</span></span>
<span data-ttu-id="71e4e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71e4e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e4e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71e4e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e4e-132">CommonParameters</span></span>
<span data-ttu-id="71e4e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e4e-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e4e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e4e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71e4e-135">INPUTS</span></span>

### <span data-ttu-id="71e4e-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71e4e-136">None</span></span>

## <span data-ttu-id="71e4e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71e4e-137">OUTPUTS</span></span>

### <span data-ttu-id="71e4e-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="71e4e-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="71e4e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="71e4e-139">NOTES</span></span>

## <span data-ttu-id="71e4e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71e4e-140">RELATED LINKS</span></span>
