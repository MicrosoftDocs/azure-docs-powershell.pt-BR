---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113653"
---
# <span data-ttu-id="ba7a0-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ba7a0-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="ba7a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7a0-103">Obtém informações sobre os detalhes do portal para a assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ba7a0-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="ba7a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba7a0-104">SYNTAX</span></span>

### <span data-ttu-id="ba7a0-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba7a0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba7a0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba7a0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba7a0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba7a0-107">DESCRIPTION</span></span>
<span data-ttu-id="ba7a0-108">O cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornece detalhes da sincronização iniciada para uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ba7a0-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="ba7a0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba7a0-109">EXAMPLES</span></span>

### <span data-ttu-id="ba7a0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba7a0-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="ba7a0-111">Este comando fornece informações sobre a sincronização iniciada para AdsShareSubscription de assinatura de compartilhamento em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="ba7a0-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ba7a0-112">OS</span><span class="sxs-lookup"><span data-stu-id="ba7a0-112">PARAMETERS</span></span>

### <span data-ttu-id="ba7a0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba7a0-113">-AccountName</span></span>
<span data-ttu-id="ba7a0-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ba7a0-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ba7a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7a0-115">-DefaultProfile</span></span>
<span data-ttu-id="ba7a0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba7a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba7a0-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="ba7a0-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ba7a0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba7a0-119">-ResourceId</span></span>
<span data-ttu-id="ba7a0-120">ID do recurso de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ba7a0-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="ba7a0-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ba7a0-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="ba7a0-122">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ba7a0-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ba7a0-123">-Synchronizationid</span><span class="sxs-lookup"><span data-stu-id="ba7a0-123">-SynchronizationId</span></span>
<span data-ttu-id="ba7a0-124">ID de sincronização da sincronização da assinatura do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="ba7a0-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="ba7a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7a0-125">CommonParameters</span></span>
<span data-ttu-id="ba7a0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7a0-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba7a0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7a0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba7a0-128">INPUTS</span></span>

### <span data-ttu-id="ba7a0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ba7a0-129">System.String</span></span>

## <span data-ttu-id="ba7a0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba7a0-130">OUTPUTS</span></span>

### <span data-ttu-id="ba7a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ba7a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="ba7a0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba7a0-132">NOTES</span></span>

## <span data-ttu-id="ba7a0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba7a0-133">RELATED LINKS</span></span>
