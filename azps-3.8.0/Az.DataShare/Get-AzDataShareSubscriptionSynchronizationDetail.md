---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: ffa9de86a7ebbb70361752b8c7733129eb024845
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777870"
---
# <span data-ttu-id="78052-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="78052-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="78052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78052-102">SYNOPSIS</span></span>
<span data-ttu-id="78052-103">Obtém informações sobre os detalhes do portal para a assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="78052-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="78052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78052-104">SYNTAX</span></span>

### <span data-ttu-id="78052-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="78052-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78052-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78052-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78052-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78052-107">DESCRIPTION</span></span>
<span data-ttu-id="78052-108">O cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornece detalhes da sincronização iniciada para uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="78052-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="78052-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78052-109">EXAMPLES</span></span>

### <span data-ttu-id="78052-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78052-110">Example 1</span></span>
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

<span data-ttu-id="78052-111">Este comando fornece informações sobre a sincronização iniciada para AdsShareSubscription de assinatura de compartilhamento em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="78052-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="78052-112">OS</span><span class="sxs-lookup"><span data-stu-id="78052-112">PARAMETERS</span></span>

### <span data-ttu-id="78052-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78052-113">-AccountName</span></span>
<span data-ttu-id="78052-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="78052-114">Azure data share account name</span></span>

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

### <span data-ttu-id="78052-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78052-115">-DefaultProfile</span></span>
<span data-ttu-id="78052-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78052-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78052-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78052-117">-ResourceGroupName</span></span>
<span data-ttu-id="78052-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="78052-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="78052-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78052-119">-ResourceId</span></span>
<span data-ttu-id="78052-120">ID do recurso de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="78052-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="78052-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="78052-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="78052-122">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="78052-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="78052-123">-Synchronizationid</span><span class="sxs-lookup"><span data-stu-id="78052-123">-SynchronizationId</span></span>
<span data-ttu-id="78052-124">ID de sincronização da sincronização da assinatura do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="78052-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="78052-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78052-125">CommonParameters</span></span>
<span data-ttu-id="78052-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78052-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78052-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78052-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78052-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78052-128">INPUTS</span></span>

### <span data-ttu-id="78052-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78052-129">System.String</span></span>

## <span data-ttu-id="78052-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78052-130">OUTPUTS</span></span>

### <span data-ttu-id="78052-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="78052-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="78052-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78052-132">NOTES</span></span>

## <span data-ttu-id="78052-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78052-133">RELATED LINKS</span></span>
