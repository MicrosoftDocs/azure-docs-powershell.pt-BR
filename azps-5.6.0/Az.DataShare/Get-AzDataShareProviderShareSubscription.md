---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893180"
---
# <span data-ttu-id="7a048-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="7a048-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="7a048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a048-102">SYNOPSIS</span></span>
<span data-ttu-id="7a048-103">Obtém informações sobre assinaturas de compartilhamento de consumidor no lado do provedor.</span><span class="sxs-lookup"><span data-stu-id="7a048-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="7a048-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a048-104">SYNTAX</span></span>

### <span data-ttu-id="7a048-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a048-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a048-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a048-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a048-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a048-107">DESCRIPTION</span></span>
<span data-ttu-id="7a048-108">O cmdlet **Get-AzDataShareProviderSubscription** obtém informações sobre assinaturas de compartilhamento de consumidor no lado do provedor.</span><span class="sxs-lookup"><span data-stu-id="7a048-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="7a048-109">Se você especificar a id de subscrption do compartilhamento, este cmdlet obtém informações sobre a assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7a048-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="7a048-110">Se você não especificar a id de assinatura de compartilhamento, este cmdlet obterá informações sobre todas as assinaturas de compartilhamento de consumidor associadas ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7a048-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="7a048-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a048-111">EXAMPLES</span></span>

### <span data-ttu-id="7a048-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a048-112">Example 1</span></span>
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

<span data-ttu-id="7a048-113">Esses comandos fornece informações sobre a assinatura de compartilhamento de consumidor associada ao compartilhamento AdsShare na conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="7a048-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="7a048-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a048-114">PARAMETERS</span></span>

### <span data-ttu-id="7a048-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a048-115">-AccountName</span></span>
<span data-ttu-id="7a048-116">Nome da conta do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="7a048-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="7a048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a048-117">-DefaultProfile</span></span>
<span data-ttu-id="7a048-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a048-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a048-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a048-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a048-120">O grupo de recursos da Conta do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="7a048-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="7a048-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a048-121">-ResourceId</span></span>
<span data-ttu-id="7a048-122">A id de recurso do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="7a048-122">The resource id of the share</span></span>

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

### <span data-ttu-id="7a048-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7a048-123">-ShareName</span></span>
<span data-ttu-id="7a048-124">Nome do Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="7a048-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="7a048-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a048-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="7a048-126">A id da assinatura de compartilhamento de consumidor</span><span class="sxs-lookup"><span data-stu-id="7a048-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="7a048-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a048-127">CommonParameters</span></span>
<span data-ttu-id="7a048-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a048-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a048-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a048-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a048-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a048-130">INPUTS</span></span>

### <span data-ttu-id="7a048-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7a048-131">System.String</span></span>

## <span data-ttu-id="7a048-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a048-132">OUTPUTS</span></span>

### <span data-ttu-id="7a048-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="7a048-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="7a048-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a048-134">NOTES</span></span>

## <span data-ttu-id="7a048-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a048-135">RELATED LINKS</span></span>
