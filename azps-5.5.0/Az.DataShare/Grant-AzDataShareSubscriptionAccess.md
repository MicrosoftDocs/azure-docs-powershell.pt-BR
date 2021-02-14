---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115850"
---
# <span data-ttu-id="96098-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="96098-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="96098-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96098-102">SYNOPSIS</span></span>
<span data-ttu-id="96098-103">Concede acesso de compartilhamento revogado de assinatura ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="96098-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="96098-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96098-104">SYNTAX</span></span>

### <span data-ttu-id="96098-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96098-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96098-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96098-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96098-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="96098-107">DESCRIPTION</span></span>
<span data-ttu-id="96098-108">O cmdlet **Grant-AzDataShareSubscriptionAccess** concede a uma assinatura de compartilhamento acesso ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="96098-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="96098-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96098-109">EXAMPLES</span></span>

### <span data-ttu-id="96098-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96098-110">Example 1</span></span>
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

<span data-ttu-id="96098-111">Concede acesso para compartilhar assinatura identificada pelo id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="96098-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="96098-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96098-112">PARAMETERS</span></span>

### <span data-ttu-id="96098-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="96098-113">-AccountName</span></span>
<span data-ttu-id="96098-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="96098-114">Azure data share account name</span></span>

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

### <span data-ttu-id="96098-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96098-115">-DefaultProfile</span></span>
<span data-ttu-id="96098-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96098-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96098-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96098-117">-ResourceGroupName</span></span>
<span data-ttu-id="96098-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="96098-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="96098-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96098-119">-ResourceId</span></span>
<span data-ttu-id="96098-120">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="96098-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="96098-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="96098-121">-ShareName</span></span>
<span data-ttu-id="96098-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="96098-122">Azure data share name</span></span>

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

### <span data-ttu-id="96098-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96098-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="96098-124">A ID de compartilhamento da assinatura de compartilhamento do provedor</span><span class="sxs-lookup"><span data-stu-id="96098-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="96098-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96098-125">-Confirm</span></span>
<span data-ttu-id="96098-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96098-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96098-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96098-127">-WhatIf</span></span>
<span data-ttu-id="96098-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96098-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96098-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96098-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96098-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96098-130">CommonParameters</span></span>
<span data-ttu-id="96098-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96098-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96098-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96098-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96098-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="96098-133">INPUTS</span></span>

### <span data-ttu-id="96098-134">System.String</span><span class="sxs-lookup"><span data-stu-id="96098-134">System.String</span></span>

## <span data-ttu-id="96098-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="96098-135">OUTPUTS</span></span>

### <span data-ttu-id="96098-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="96098-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="96098-137">Notas</span><span class="sxs-lookup"><span data-stu-id="96098-137">NOTES</span></span>

## <span data-ttu-id="96098-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96098-138">RELATED LINKS</span></span>
