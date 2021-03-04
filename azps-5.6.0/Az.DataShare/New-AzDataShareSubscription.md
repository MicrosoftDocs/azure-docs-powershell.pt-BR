---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891195"
---
# <span data-ttu-id="90bcd-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="90bcd-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="90bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="90bcd-103">Cria uma nova assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="90bcd-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="90bcd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90bcd-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90bcd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="90bcd-106">O cmdlet **New-AzDataShareSubscription** cria uma assinatura de compartilhamento em conta de compartilhamento de dados especificada e id de convite.</span><span class="sxs-lookup"><span data-stu-id="90bcd-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="90bcd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="90bcd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90bcd-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="90bcd-109">Esses comandos criam uma nova assinatura de compartilhamento AdsShareSubscription para invitaionId em conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="90bcd-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="90bcd-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90bcd-110">PARAMETERS</span></span>

### <span data-ttu-id="90bcd-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90bcd-111">-AccountName</span></span>
<span data-ttu-id="90bcd-112">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="90bcd-112">Azure data share account name</span></span>

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

### <span data-ttu-id="90bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="90bcd-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90bcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90bcd-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="90bcd-115">-InvitationId</span></span>
<span data-ttu-id="90bcd-116">InvitationId de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="90bcd-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="90bcd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90bcd-117">-Name</span></span>
<span data-ttu-id="90bcd-118">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="90bcd-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="90bcd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bcd-119">-ResourceGroupName</span></span>
<span data-ttu-id="90bcd-120">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="90bcd-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="90bcd-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="90bcd-121">-SourceShareLocation</span></span>
<span data-ttu-id="90bcd-122">Local do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="90bcd-122">Azure data share location</span></span>

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

### <span data-ttu-id="90bcd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90bcd-123">-Confirm</span></span>
<span data-ttu-id="90bcd-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90bcd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bcd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90bcd-125">-WhatIf</span></span>
<span data-ttu-id="90bcd-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90bcd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90bcd-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90bcd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bcd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bcd-128">CommonParameters</span></span>
<span data-ttu-id="90bcd-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90bcd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bcd-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90bcd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bcd-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90bcd-131">INPUTS</span></span>

### <span data-ttu-id="90bcd-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="90bcd-132">None</span></span>

## <span data-ttu-id="90bcd-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90bcd-133">OUTPUTS</span></span>

### <span data-ttu-id="90bcd-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="90bcd-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="90bcd-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="90bcd-135">NOTES</span></span>

## <span data-ttu-id="90bcd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90bcd-136">RELATED LINKS</span></span>
