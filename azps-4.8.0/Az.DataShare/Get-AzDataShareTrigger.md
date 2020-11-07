---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955620"
---
# <span data-ttu-id="bb135-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bb135-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="bb135-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb135-102">SYNOPSIS</span></span>
<span data-ttu-id="bb135-103">Obtém informações sobre um gatilho na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="bb135-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="bb135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb135-104">SYNTAX</span></span>

### <span data-ttu-id="bb135-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb135-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb135-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb135-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb135-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb135-107">DESCRIPTION</span></span>
<span data-ttu-id="bb135-108">O cmdlet **Get-AzDataShareTrigger** Obtém informações sobre o gatilho para a assinatura de compartilhamento em conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="bb135-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="bb135-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb135-109">EXAMPLES</span></span>

### <span data-ttu-id="bb135-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb135-110">Example 1</span></span>
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

<span data-ttu-id="bb135-111">Este comando obtém informações sobre o gatilho AdsTrigger para AdsShareSubscription de assinatura de compartilhamento em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="bb135-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="bb135-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb135-112">PARAMETERS</span></span>

### <span data-ttu-id="bb135-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bb135-113">-AccountName</span></span>
<span data-ttu-id="bb135-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="bb135-114">Azure data share account name</span></span>

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

### <span data-ttu-id="bb135-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb135-115">-DefaultProfile</span></span>
<span data-ttu-id="bb135-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb135-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb135-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb135-117">-Name</span></span>
<span data-ttu-id="bb135-118">Nome do gatilho do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="bb135-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="bb135-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb135-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb135-120">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="bb135-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bb135-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb135-121">-ResourceId</span></span>
<span data-ttu-id="bb135-122">A ID do recurso do gatilho</span><span class="sxs-lookup"><span data-stu-id="bb135-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="bb135-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bb135-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="bb135-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="bb135-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="bb135-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb135-125">CommonParameters</span></span>
<span data-ttu-id="bb135-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb135-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb135-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb135-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb135-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb135-128">INPUTS</span></span>

### <span data-ttu-id="bb135-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb135-129">System.String</span></span>

## <span data-ttu-id="bb135-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb135-130">OUTPUTS</span></span>

### <span data-ttu-id="bb135-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="bb135-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="bb135-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb135-132">NOTES</span></span>

## <span data-ttu-id="bb135-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb135-133">RELATED LINKS</span></span>
