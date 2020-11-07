---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 6ac4fdbc119c5cd6639e9b688d60e158eea2a62f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944419"
---
# <span data-ttu-id="d233b-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="d233b-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="d233b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d233b-102">SYNOPSIS</span></span>
<span data-ttu-id="d233b-103">Revoga o acesso à assinatura do compartilhamento ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="d233b-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="d233b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d233b-104">SYNTAX</span></span>

### <span data-ttu-id="d233b-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d233b-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d233b-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d233b-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d233b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d233b-107">DESCRIPTION</span></span>
<span data-ttu-id="d233b-108">O cmdlet **REVOKE-AzDataShareSubscriptionAccess** concede um acesso de assinatura de compartilhamento ao compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="d233b-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="d233b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d233b-109">EXAMPLES</span></span>

### <span data-ttu-id="d233b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d233b-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="d233b-111">Revoga o acesso da assinatura de compartilhamento identificada pela ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="d233b-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="d233b-112">OS</span><span class="sxs-lookup"><span data-stu-id="d233b-112">PARAMETERS</span></span>

### <span data-ttu-id="d233b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d233b-113">-AccountName</span></span>
<span data-ttu-id="d233b-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d233b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d233b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d233b-115">-AsJob</span></span>
<span data-ttu-id="d233b-116">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="d233b-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d233b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d233b-117">-DefaultProfile</span></span>
<span data-ttu-id="d233b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d233b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d233b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d233b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d233b-120">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d233b-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d233b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d233b-121">-ResourceId</span></span>
<span data-ttu-id="d233b-122">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d233b-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="d233b-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d233b-123">-ShareName</span></span>
<span data-ttu-id="d233b-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d233b-124">Azure data share name</span></span>

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

### <span data-ttu-id="d233b-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d233b-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="d233b-126">A ID da assinatura de compartilhamento da assinatura de compartilhamento do provedor</span><span class="sxs-lookup"><span data-stu-id="d233b-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="d233b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d233b-127">-Confirm</span></span>
<span data-ttu-id="d233b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d233b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d233b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d233b-129">-WhatIf</span></span>
<span data-ttu-id="d233b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d233b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d233b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d233b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d233b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d233b-132">CommonParameters</span></span>
<span data-ttu-id="d233b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d233b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d233b-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d233b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d233b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d233b-135">INPUTS</span></span>

### <span data-ttu-id="d233b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d233b-136">System.String</span></span>

## <span data-ttu-id="d233b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d233b-137">OUTPUTS</span></span>

### <span data-ttu-id="d233b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d233b-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="d233b-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d233b-139">NOTES</span></span>

## <span data-ttu-id="d233b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d233b-140">RELATED LINKS</span></span>
