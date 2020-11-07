---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955621"
---
# <span data-ttu-id="217af-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="217af-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="217af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="217af-102">SYNOPSIS</span></span>
<span data-ttu-id="217af-103">Obtém informações sobre as assinaturas de compartilhamento do consumidor no lado do provedor.</span><span class="sxs-lookup"><span data-stu-id="217af-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="217af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="217af-104">SYNTAX</span></span>

### <span data-ttu-id="217af-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="217af-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217af-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="217af-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="217af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="217af-107">DESCRIPTION</span></span>
<span data-ttu-id="217af-108">O cmdlet **Get-AzDataShareProviderSubscription** Obtém informações sobre as assinaturas de compartilhamento do consumidor no lado do provedor.</span><span class="sxs-lookup"><span data-stu-id="217af-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="217af-109">Se você especificar a ID do compartilhamento de subscrption, esse cmdlet obterá informações sobre a assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="217af-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="217af-110">Se você não especificar a ID da assinatura de compartilhamento, esse cmdlet obterá informações sobre todas as assinaturas de compartilhamento do consumidor em associadas ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="217af-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="217af-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="217af-111">EXAMPLES</span></span>

### <span data-ttu-id="217af-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="217af-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="217af-113">Esses comandos fornecem informações sobre a assinatura de compartilhamento do consumidor associada ao share AdsShare no WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="217af-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="217af-114">OS</span><span class="sxs-lookup"><span data-stu-id="217af-114">PARAMETERS</span></span>

### <span data-ttu-id="217af-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="217af-115">-AccountName</span></span>
<span data-ttu-id="217af-116">Nome da conta do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="217af-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="217af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217af-117">-DefaultProfile</span></span>
<span data-ttu-id="217af-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="217af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="217af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217af-119">-ResourceGroupName</span></span>
<span data-ttu-id="217af-120">O grupo de recursos da conta do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="217af-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="217af-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="217af-121">-ResourceId</span></span>
<span data-ttu-id="217af-122">A ID do recurso do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="217af-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217af-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="217af-123">-ShareName</span></span>
<span data-ttu-id="217af-124">Nome do compartilhamento de DataShare.</span><span class="sxs-lookup"><span data-stu-id="217af-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="217af-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="217af-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="217af-126">A ID da assinatura de compartilhamento do consumidor</span><span class="sxs-lookup"><span data-stu-id="217af-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="217af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217af-127">CommonParameters</span></span>
<span data-ttu-id="217af-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217af-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="217af-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217af-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="217af-130">INPUTS</span></span>

### <span data-ttu-id="217af-131">System. String</span><span class="sxs-lookup"><span data-stu-id="217af-131">System.String</span></span>

## <span data-ttu-id="217af-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="217af-132">OUTPUTS</span></span>

### <span data-ttu-id="217af-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="217af-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="217af-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="217af-134">NOTES</span></span>

## <span data-ttu-id="217af-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="217af-135">RELATED LINKS</span></span>
