---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116852"
---
# <span data-ttu-id="1eee8-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="1eee8-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="1eee8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eee8-102">SYNOPSIS</span></span>
<span data-ttu-id="1eee8-103">Obtém informações sobre um gatilho na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1eee8-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="1eee8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1eee8-104">SYNTAX</span></span>

### <span data-ttu-id="1eee8-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1eee8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eee8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eee8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eee8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1eee8-107">DESCRIPTION</span></span>
<span data-ttu-id="1eee8-108">O **cmdlet Get-AzDataShareTri adobe obtém** informações sobre o gatilho para compartilhar assinatura na conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="1eee8-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="1eee8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1eee8-109">EXAMPLES</span></span>

### <span data-ttu-id="1eee8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1eee8-110">Example 1</span></span>
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

<span data-ttu-id="1eee8-111">Este comando obtém informações sobre acionar AdsTriscription para compartilhar assinatura AdsShareSubscription sob a conta wikiAds do compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="1eee8-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="1eee8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1eee8-112">PARAMETERS</span></span>

### <span data-ttu-id="1eee8-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="1eee8-113">-AccountName</span></span>
<span data-ttu-id="1eee8-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="1eee8-114">Azure data share account name</span></span>

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

### <span data-ttu-id="1eee8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eee8-115">-DefaultProfile</span></span>
<span data-ttu-id="1eee8-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eee8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eee8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eee8-117">-Name</span></span>
<span data-ttu-id="1eee8-118">Nome do gatilho de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="1eee8-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="1eee8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eee8-119">-ResourceGroupName</span></span>
<span data-ttu-id="1eee8-120">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="1eee8-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1eee8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eee8-121">-ResourceId</span></span>
<span data-ttu-id="1eee8-122">A ID do recurso do gatilho</span><span class="sxs-lookup"><span data-stu-id="1eee8-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="1eee8-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1eee8-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="1eee8-124">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="1eee8-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1eee8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eee8-125">CommonParameters</span></span>
<span data-ttu-id="1eee8-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eee8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eee8-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1eee8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eee8-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="1eee8-128">INPUTS</span></span>

### <span data-ttu-id="1eee8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1eee8-129">System.String</span></span>

## <span data-ttu-id="1eee8-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="1eee8-130">OUTPUTS</span></span>

### <span data-ttu-id="1eee8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="1eee8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="1eee8-132">Notas</span><span class="sxs-lookup"><span data-stu-id="1eee8-132">NOTES</span></span>

## <span data-ttu-id="1eee8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eee8-133">RELATED LINKS</span></span>
