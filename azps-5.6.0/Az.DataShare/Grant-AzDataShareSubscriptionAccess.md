---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 00b82731e807aa2351d66744b889f56f440226b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892498"
---
# <span data-ttu-id="db708-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="db708-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="db708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db708-102">SYNOPSIS</span></span>
<span data-ttu-id="db708-103">Concede um acesso de assinatura de compartilhamento revogado ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="db708-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="db708-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db708-104">SYNTAX</span></span>

### <span data-ttu-id="db708-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db708-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db708-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db708-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db708-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db708-107">DESCRIPTION</span></span>
<span data-ttu-id="db708-108">O cmdlet **Grant-AzDataShareSubscriptionAccess** concede acesso de assinatura de compartilhamento ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="db708-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="db708-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db708-109">EXAMPLES</span></span>

### <span data-ttu-id="db708-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db708-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="db708-111">Concede acesso à assinatura de compartilhamento identificada pelo id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="db708-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="db708-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db708-112">PARAMETERS</span></span>

### <span data-ttu-id="db708-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db708-113">-AccountName</span></span>
<span data-ttu-id="db708-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="db708-114">Azure data share account name</span></span>

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

### <span data-ttu-id="db708-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db708-115">-DefaultProfile</span></span>
<span data-ttu-id="db708-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db708-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db708-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db708-117">-ResourceGroupName</span></span>
<span data-ttu-id="db708-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="db708-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="db708-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db708-119">-ResourceId</span></span>
<span data-ttu-id="db708-120">A id de recurso do compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="db708-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="db708-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="db708-121">-ShareName</span></span>
<span data-ttu-id="db708-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="db708-122">Azure data share name</span></span>

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

### <span data-ttu-id="db708-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db708-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="db708-124">A ID de assinatura de compartilhamento da assinatura de compartilhamento do provedor</span><span class="sxs-lookup"><span data-stu-id="db708-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="db708-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db708-125">-Confirm</span></span>
<span data-ttu-id="db708-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db708-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db708-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db708-127">-WhatIf</span></span>
<span data-ttu-id="db708-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db708-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db708-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db708-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db708-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db708-130">CommonParameters</span></span>
<span data-ttu-id="db708-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db708-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db708-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db708-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db708-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db708-133">INPUTS</span></span>

### <span data-ttu-id="db708-134">System.String</span><span class="sxs-lookup"><span data-stu-id="db708-134">System.String</span></span>

## <span data-ttu-id="db708-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db708-135">OUTPUTS</span></span>

### <span data-ttu-id="db708-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="db708-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="db708-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="db708-137">NOTES</span></span>

## <span data-ttu-id="db708-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db708-138">RELATED LINKS</span></span>
