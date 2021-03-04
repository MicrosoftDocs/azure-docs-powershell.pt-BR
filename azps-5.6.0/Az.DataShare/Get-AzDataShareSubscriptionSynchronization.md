---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886671"
---
# <span data-ttu-id="ad3b6-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="ad3b6-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="ad3b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3b6-103">Obtém informações sobre sincronização executados na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="ad3b6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad3b6-104">SYNTAX</span></span>

### <span data-ttu-id="ad3b6-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad3b6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad3b6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad3b6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad3b6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad3b6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad3b6-108">O cmdlet **Get-AzDataShareSubscriptionSynchronization** fornece informações sobre todas as sincronizações executados em uma assinatura de compartilhamento em uma conta de compartilhamento de dados no consumidor.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="ad3b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-109">EXAMPLES</span></span>

### <span data-ttu-id="ad3b6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ad3b6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="ad3b6-111">Este comando fornece informações sobre todas as executações de sincronização para uma assinatura de compartilhamento AdsShareSubscription em conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ad3b6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-112">PARAMETERS</span></span>

### <span data-ttu-id="ad3b6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad3b6-113">-AccountName</span></span>
<span data-ttu-id="ad3b6-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ad3b6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ad3b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3b6-115">-DefaultProfile</span></span>
<span data-ttu-id="ad3b6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad3b6-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="ad3b6-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ad3b6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad3b6-119">-ResourceId</span></span>
<span data-ttu-id="ad3b6-120">ID do recurso de assinatura de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ad3b6-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="ad3b6-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ad3b6-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="ad3b6-122">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ad3b6-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ad3b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3b6-123">CommonParameters</span></span>
<span data-ttu-id="ad3b6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3b6-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad3b6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3b6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-126">INPUTS</span></span>

### <span data-ttu-id="ad3b6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ad3b6-127">System.String</span></span>

## <span data-ttu-id="ad3b6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-128">OUTPUTS</span></span>

### <span data-ttu-id="ad3b6-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="ad3b6-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="ad3b6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad3b6-130">NOTES</span></span>

## <span data-ttu-id="ad3b6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad3b6-131">RELATED LINKS</span></span>
