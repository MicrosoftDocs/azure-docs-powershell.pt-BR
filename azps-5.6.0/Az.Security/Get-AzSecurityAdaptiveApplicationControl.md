---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: ec35083cf4495d0bf262d841563f0dc4100dcdc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888180"
---
# <span data-ttu-id="bb529-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="bb529-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="bb529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb529-102">SYNOPSIS</span></span>
<span data-ttu-id="bb529-103">Obtém uma lista de grupos de VM/servidor de controle de aplicativos para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="bb529-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="bb529-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb529-104">SYNTAX</span></span>

### <span data-ttu-id="bb529-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb529-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb529-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb529-106">DESCRIPTION</span></span>
<span data-ttu-id="bb529-107">Controles de aplicativo adaptáveis são calculados automaticamente pelo Centro de Segurança do Azure, use este cmdlet para obter uma lista de recursos controles de aplicativo adaptáveis no escopo de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="bb529-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="bb529-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb529-108">EXAMPLES</span></span>

### <span data-ttu-id="bb529-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb529-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="bb529-110">Obtém uma lista de grupos de VM/servidor de controle de aplicativos para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="bb529-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="bb529-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb529-111">PARAMETERS</span></span>

### <span data-ttu-id="bb529-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb529-112">-DefaultProfile</span></span>
<span data-ttu-id="bb529-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb529-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb529-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb529-114">-SubscriptionId</span></span>
<span data-ttu-id="bb529-115">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb529-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb529-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="bb529-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="bb529-117">Inclua as regras de política.</span><span class="sxs-lookup"><span data-stu-id="bb529-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb529-118">-Summary</span><span class="sxs-lookup"><span data-stu-id="bb529-118">-Summary</span></span>
<span data-ttu-id="bb529-119">Retornar saída em um formulário resumido.</span><span class="sxs-lookup"><span data-stu-id="bb529-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb529-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb529-120">CommonParameters</span></span>
<span data-ttu-id="bb529-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb529-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb529-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb529-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb529-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb529-123">INPUTS</span></span>

### <span data-ttu-id="bb529-124">System.String</span><span class="sxs-lookup"><span data-stu-id="bb529-124">System.String</span></span>

### <span data-ttu-id="bb529-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb529-125">System.Boolean</span></span>

## <span data-ttu-id="bb529-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb529-126">OUTPUTS</span></span>

### <span data-ttu-id="bb529-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="bb529-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="bb529-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb529-128">NOTES</span></span>

## <span data-ttu-id="bb529-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb529-129">RELATED LINKS</span></span>
