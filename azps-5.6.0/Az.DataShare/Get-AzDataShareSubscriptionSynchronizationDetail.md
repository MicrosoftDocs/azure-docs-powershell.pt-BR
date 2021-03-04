---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: c2f7dc41bc84594d1c9d7e64dc52f27a162b8be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892503"
---
# <span data-ttu-id="ac3bf-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ac3bf-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="ac3bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3bf-103">Obtém informações sobre detalhes de sincronização para assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ac3bf-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="ac3bf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac3bf-104">SYNTAX</span></span>

### <span data-ttu-id="ac3bf-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac3bf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac3bf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac3bf-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac3bf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac3bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ac3bf-108">O cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornece detalhes da sincronização iniciada para uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ac3bf-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="ac3bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-109">EXAMPLES</span></span>

### <span data-ttu-id="ac3bf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac3bf-110">Example 1</span></span>
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

<span data-ttu-id="ac3bf-111">Este comando fornece informações sobre a sincronização iniciada para compartilhar assinatura AdsShareSubscription na conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="ac3bf-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ac3bf-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-112">PARAMETERS</span></span>

### <span data-ttu-id="ac3bf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac3bf-113">-AccountName</span></span>
<span data-ttu-id="ac3bf-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ac3bf-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ac3bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3bf-115">-DefaultProfile</span></span>
<span data-ttu-id="ac3bf-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac3bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac3bf-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="ac3bf-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ac3bf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac3bf-119">-ResourceId</span></span>
<span data-ttu-id="ac3bf-120">ID do recurso de assinatura de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ac3bf-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="ac3bf-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ac3bf-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="ac3bf-122">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ac3bf-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ac3bf-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="ac3bf-123">-SynchronizationId</span></span>
<span data-ttu-id="ac3bf-124">ID de sincronização da sincronização de assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="ac3bf-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="ac3bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3bf-125">CommonParameters</span></span>
<span data-ttu-id="ac3bf-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3bf-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac3bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3bf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-128">INPUTS</span></span>

### <span data-ttu-id="ac3bf-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ac3bf-129">System.String</span></span>

## <span data-ttu-id="ac3bf-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-130">OUTPUTS</span></span>

### <span data-ttu-id="ac3bf-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ac3bf-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="ac3bf-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac3bf-132">NOTES</span></span>

## <span data-ttu-id="ac3bf-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac3bf-133">RELATED LINKS</span></span>
