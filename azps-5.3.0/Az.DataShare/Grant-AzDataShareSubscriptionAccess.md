---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271483"
---
# <span data-ttu-id="c666c-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="c666c-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="c666c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c666c-102">SYNOPSIS</span></span>
<span data-ttu-id="c666c-103">Concede o acesso à assinatura de compartilhamento revogado ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="c666c-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="c666c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c666c-104">SYNTAX</span></span>

### <span data-ttu-id="c666c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c666c-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c666c-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c666c-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c666c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c666c-107">DESCRIPTION</span></span>
<span data-ttu-id="c666c-108">O cmdlet **Grant-AzDataShareSubscriptionAccess** concede um acesso de assinatura de compartilhamento ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="c666c-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="c666c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c666c-109">EXAMPLES</span></span>

### <span data-ttu-id="c666c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c666c-110">Example 1</span></span>
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

<span data-ttu-id="c666c-111">Concede acesso à assinatura de compartilhamento identificada pela ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="c666c-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="c666c-112">OS</span><span class="sxs-lookup"><span data-stu-id="c666c-112">PARAMETERS</span></span>

### <span data-ttu-id="c666c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c666c-113">-AccountName</span></span>
<span data-ttu-id="c666c-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="c666c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c666c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c666c-115">-DefaultProfile</span></span>
<span data-ttu-id="c666c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c666c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c666c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c666c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c666c-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="c666c-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c666c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c666c-119">-ResourceId</span></span>
<span data-ttu-id="c666c-120">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="c666c-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="c666c-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c666c-121">-ShareName</span></span>
<span data-ttu-id="c666c-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="c666c-122">Azure data share name</span></span>

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

### <span data-ttu-id="c666c-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c666c-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="c666c-124">A ID da assinatura de compartilhamento da assinatura de compartilhamento do provedor</span><span class="sxs-lookup"><span data-stu-id="c666c-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="c666c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c666c-125">-Confirm</span></span>
<span data-ttu-id="c666c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c666c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c666c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c666c-127">-WhatIf</span></span>
<span data-ttu-id="c666c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c666c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c666c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c666c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c666c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c666c-130">CommonParameters</span></span>
<span data-ttu-id="c666c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c666c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c666c-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c666c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c666c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c666c-133">INPUTS</span></span>

### <span data-ttu-id="c666c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c666c-134">System.String</span></span>

## <span data-ttu-id="c666c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c666c-135">OUTPUTS</span></span>

### <span data-ttu-id="c666c-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c666c-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="c666c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c666c-137">NOTES</span></span>

## <span data-ttu-id="c666c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c666c-138">RELATED LINKS</span></span>
