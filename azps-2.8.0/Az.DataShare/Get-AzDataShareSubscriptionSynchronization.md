---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596726"
---
# <span data-ttu-id="2c029-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="2c029-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="2c029-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c029-102">SYNOPSIS</span></span>
<span data-ttu-id="2c029-103">Obtém informações sobre execuções de sincronização na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2c029-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="2c029-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c029-104">SYNTAX</span></span>

### <span data-ttu-id="2c029-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c029-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c029-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c029-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c029-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c029-107">DESCRIPTION</span></span>
<span data-ttu-id="2c029-108">O cmdlet **Get-AzDataShareSubscriptionSynchronization** fornece informaiton sobre todas as execuções de sincronização em uma assinatura de compartilhamento em uma conta de compartilhamento de dados no consumidor.</span><span class="sxs-lookup"><span data-stu-id="2c029-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="2c029-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c029-109">EXAMPLES</span></span>

### <span data-ttu-id="2c029-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c029-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="2c029-111">Esse comando fornece informações sobre todas as execuções de sincronização para uma assinatura de compartilhamento AdsShareSubscription em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="2c029-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="2c029-112">OS</span><span class="sxs-lookup"><span data-stu-id="2c029-112">PARAMETERS</span></span>

### <span data-ttu-id="2c029-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c029-113">-AccountName</span></span>
<span data-ttu-id="2c029-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2c029-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2c029-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c029-115">-DefaultProfile</span></span>
<span data-ttu-id="2c029-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c029-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c029-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c029-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c029-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="2c029-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2c029-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c029-119">-ResourceId</span></span>
<span data-ttu-id="2c029-120">ID do recurso de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2c029-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="2c029-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2c029-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="2c029-122">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2c029-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2c029-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c029-123">CommonParameters</span></span>
<span data-ttu-id="2c029-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c029-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c029-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c029-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c029-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c029-126">INPUTS</span></span>

### <span data-ttu-id="2c029-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2c029-127">System.String</span></span>

## <span data-ttu-id="2c029-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c029-128">OUTPUTS</span></span>

### <span data-ttu-id="2c029-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="2c029-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="2c029-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c029-130">NOTES</span></span>

## <span data-ttu-id="2c029-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c029-131">RELATED LINKS</span></span>
