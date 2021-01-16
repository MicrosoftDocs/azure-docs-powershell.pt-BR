---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256894"
---
# <span data-ttu-id="5263a-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="5263a-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="5263a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5263a-102">SYNOPSIS</span></span>
<span data-ttu-id="5263a-103">Cria um gatilho para a assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5263a-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="5263a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5263a-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5263a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5263a-105">DESCRIPTION</span></span>
<span data-ttu-id="5263a-106">O cmdlet **New-AzDataShareTrigger** cria um gatilho para a assinatura de compartilhamento do intervalo de recorrência especificado e do tempo de sincronização na conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="5263a-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="5263a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5263a-107">EXAMPLES</span></span>

### <span data-ttu-id="5263a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5263a-108">Example 1</span></span>
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

<span data-ttu-id="5263a-109">Esse comando cria um novo gatilho AdsTrigger para a assinatura de compartilhamento AdsShareSubscription com um intervalo de recorrência diário de 9 AM.</span><span class="sxs-lookup"><span data-stu-id="5263a-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="5263a-110">OS</span><span class="sxs-lookup"><span data-stu-id="5263a-110">PARAMETERS</span></span>

### <span data-ttu-id="5263a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5263a-111">-AccountName</span></span>
<span data-ttu-id="5263a-112">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="5263a-112">Azure data share account name</span></span>

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

### <span data-ttu-id="5263a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5263a-113">-AsJob</span></span>
<span data-ttu-id="5263a-114">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="5263a-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="5263a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5263a-115">-DefaultProfile</span></span>
<span data-ttu-id="5263a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5263a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5263a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5263a-117">-Name</span></span>
<span data-ttu-id="5263a-118">Nome do gatilho do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="5263a-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="5263a-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="5263a-119">-RecurrenceInterval</span></span>
<span data-ttu-id="5263a-120">O intervalo de recorrência do gatilho (dia ou hora)</span><span class="sxs-lookup"><span data-stu-id="5263a-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="5263a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5263a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5263a-122">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="5263a-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5263a-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5263a-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="5263a-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="5263a-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="5263a-125">-Synchronizationtime</span><span class="sxs-lookup"><span data-stu-id="5263a-125">-SynchronizationTime</span></span>
<span data-ttu-id="5263a-126">A hora de início da sincronização agendada para o gatilho</span><span class="sxs-lookup"><span data-stu-id="5263a-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="5263a-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5263a-127">-Confirm</span></span>
<span data-ttu-id="5263a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5263a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5263a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5263a-129">-WhatIf</span></span>
<span data-ttu-id="5263a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5263a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5263a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5263a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5263a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5263a-132">CommonParameters</span></span>
<span data-ttu-id="5263a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5263a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5263a-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5263a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5263a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5263a-135">INPUTS</span></span>

### <span data-ttu-id="5263a-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5263a-136">None</span></span>

## <span data-ttu-id="5263a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5263a-137">OUTPUTS</span></span>

### <span data-ttu-id="5263a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="5263a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="5263a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5263a-139">NOTES</span></span>

## <span data-ttu-id="5263a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5263a-140">RELATED LINKS</span></span>
