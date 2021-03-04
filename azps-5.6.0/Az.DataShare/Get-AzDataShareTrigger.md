---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 430f31a0e44f226584d06a341971ed206a2bf5d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892499"
---
# <span data-ttu-id="115ad-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="115ad-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="115ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="115ad-102">SYNOPSIS</span></span>
<span data-ttu-id="115ad-103">Obtém informações sobre um gatilho na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="115ad-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="115ad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="115ad-104">SYNTAX</span></span>

### <span data-ttu-id="115ad-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="115ad-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="115ad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="115ad-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="115ad-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="115ad-107">DESCRIPTION</span></span>
<span data-ttu-id="115ad-108">O cmdlet **Get-AzDataShareTrigger** obtém informações sobre o gatilho para compartilhamento de assinatura em conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="115ad-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="115ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="115ad-109">EXAMPLES</span></span>

### <span data-ttu-id="115ad-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="115ad-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

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

<span data-ttu-id="115ad-111">Este comando obtém informações sobre disparar AdsTrigger para compartilhar assinatura AdsShareSubscription em conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="115ad-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="115ad-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="115ad-112">PARAMETERS</span></span>

### <span data-ttu-id="115ad-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="115ad-113">-AccountName</span></span>
<span data-ttu-id="115ad-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="115ad-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115ad-115">-DefaultProfile</span></span>
<span data-ttu-id="115ad-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="115ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="115ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="115ad-117">-Name</span></span>
<span data-ttu-id="115ad-118">Nome do gatilho de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="115ad-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="115ad-120">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="115ad-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115ad-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="115ad-121">-ResourceId</span></span>
<span data-ttu-id="115ad-122">A id de recurso do gatilho</span><span class="sxs-lookup"><span data-stu-id="115ad-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115ad-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="115ad-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="115ad-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="115ad-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115ad-125">CommonParameters</span></span>
<span data-ttu-id="115ad-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115ad-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="115ad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115ad-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="115ad-128">INPUTS</span></span>

### <span data-ttu-id="115ad-129">System.String</span><span class="sxs-lookup"><span data-stu-id="115ad-129">System.String</span></span>

## <span data-ttu-id="115ad-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="115ad-130">OUTPUTS</span></span>

### <span data-ttu-id="115ad-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="115ad-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="115ad-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="115ad-132">NOTES</span></span>

## <span data-ttu-id="115ad-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="115ad-133">RELATED LINKS</span></span>
