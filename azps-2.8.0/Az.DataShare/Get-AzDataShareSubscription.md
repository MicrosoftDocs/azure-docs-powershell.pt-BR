---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 23553e939256b9124369afd79db29a50802dc6cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596731"
---
# <span data-ttu-id="baca8-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="baca8-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="baca8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baca8-102">SYNOPSIS</span></span>
<span data-ttu-id="baca8-103">Obtém informações sobre a assinatura de compartilhamento na conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="baca8-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="baca8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baca8-104">SYNTAX</span></span>

### <span data-ttu-id="baca8-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="baca8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baca8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="baca8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baca8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="baca8-107">DESCRIPTION</span></span>
<span data-ttu-id="baca8-108">O cmdlet **Get-AzDataShareSubscription** fornece informações sobre a assinatura de compartilhamento em uma conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="baca8-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="baca8-109">Se o nome do compartilhamento de assinatura for fornecido, o cmdlet fornece informações sobre a assinatura de compartilhamento em particular.</span><span class="sxs-lookup"><span data-stu-id="baca8-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="baca8-110">Caso contrário, o cmdlet fornece uma lista de assinaturas de compartilhamento na conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="baca8-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="baca8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baca8-111">EXAMPLES</span></span>

### <span data-ttu-id="baca8-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="baca8-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="baca8-113">Este comando fornece informações sobre o compartilhamento de assinatura AdsShareSubscription no WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="baca8-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="baca8-114">OS</span><span class="sxs-lookup"><span data-stu-id="baca8-114">PARAMETERS</span></span>

### <span data-ttu-id="baca8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="baca8-115">-AccountName</span></span>
<span data-ttu-id="baca8-116">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="baca8-116">Azure data share account name</span></span>

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

### <span data-ttu-id="baca8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baca8-117">-DefaultProfile</span></span>
<span data-ttu-id="baca8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baca8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baca8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="baca8-119">-Name</span></span>
<span data-ttu-id="baca8-120">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="baca8-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="baca8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baca8-121">-ResourceGroupName</span></span>
<span data-ttu-id="baca8-122">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="baca8-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="baca8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baca8-123">-ResourceId</span></span>
<span data-ttu-id="baca8-124">A ID do recurso da assinatura do Azure data share</span><span class="sxs-lookup"><span data-stu-id="baca8-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="baca8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baca8-125">CommonParameters</span></span>
<span data-ttu-id="baca8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baca8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baca8-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baca8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baca8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="baca8-128">INPUTS</span></span>

### <span data-ttu-id="baca8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="baca8-129">System.String</span></span>

## <span data-ttu-id="baca8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="baca8-130">OUTPUTS</span></span>

### <span data-ttu-id="baca8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="baca8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="baca8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="baca8-132">NOTES</span></span>

## <span data-ttu-id="baca8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baca8-133">RELATED LINKS</span></span>
