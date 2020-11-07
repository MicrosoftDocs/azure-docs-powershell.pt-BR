---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 57b5476e9b797179acdc513cc5fe536ccf4eee69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940911"
---
# <span data-ttu-id="98c44-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="98c44-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="98c44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98c44-102">SYNOPSIS</span></span>
<span data-ttu-id="98c44-103">Obtém informações sobre um gatilho na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="98c44-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="98c44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98c44-104">SYNTAX</span></span>

### <span data-ttu-id="98c44-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="98c44-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c44-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c44-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98c44-107">DESCRIPTION</span></span>
<span data-ttu-id="98c44-108">O cmdlet **Get-AzDataShareTrigger** Obtém informações sobre o gatilho para a assinatura de compartilhamento em conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="98c44-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="98c44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98c44-109">EXAMPLES</span></span>

### <span data-ttu-id="98c44-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98c44-110">Example 1</span></span>
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

<span data-ttu-id="98c44-111">Este comando obtém informações sobre o gatilho AdsTrigger para AdsShareSubscription de assinatura de compartilhamento em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="98c44-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="98c44-112">OS</span><span class="sxs-lookup"><span data-stu-id="98c44-112">PARAMETERS</span></span>

### <span data-ttu-id="98c44-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98c44-113">-AccountName</span></span>
<span data-ttu-id="98c44-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="98c44-114">Azure data share account name</span></span>

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

### <span data-ttu-id="98c44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c44-115">-DefaultProfile</span></span>
<span data-ttu-id="98c44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98c44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c44-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="98c44-117">-Name</span></span>
<span data-ttu-id="98c44-118">Nome do gatilho do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="98c44-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="98c44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c44-119">-ResourceGroupName</span></span>
<span data-ttu-id="98c44-120">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="98c44-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="98c44-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c44-121">-ResourceId</span></span>
<span data-ttu-id="98c44-122">A ID do recurso do gatilho</span><span class="sxs-lookup"><span data-stu-id="98c44-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="98c44-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="98c44-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="98c44-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="98c44-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="98c44-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c44-125">CommonParameters</span></span>
<span data-ttu-id="98c44-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c44-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c44-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c44-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c44-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98c44-128">INPUTS</span></span>

### <span data-ttu-id="98c44-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98c44-129">System.String</span></span>

## <span data-ttu-id="98c44-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98c44-130">OUTPUTS</span></span>

### <span data-ttu-id="98c44-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="98c44-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="98c44-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98c44-132">NOTES</span></span>

## <span data-ttu-id="98c44-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98c44-133">RELATED LINKS</span></span>
