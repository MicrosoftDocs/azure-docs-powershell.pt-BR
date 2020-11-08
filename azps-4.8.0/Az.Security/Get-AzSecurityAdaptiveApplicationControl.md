---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110298"
---
# <span data-ttu-id="52599-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="52599-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="52599-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52599-102">SYNOPSIS</span></span>
<span data-ttu-id="52599-103">Obtém uma lista de grupos de servidores/VM de controle do aplicativo para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="52599-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="52599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52599-104">SYNTAX</span></span>

### <span data-ttu-id="52599-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="52599-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52599-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52599-106">DESCRIPTION</span></span>
<span data-ttu-id="52599-107">Os controles de aplicativos adaptáveis são calculados automaticamente pela central de segurança do Azure, use esse cmdlet para obter uma lista de recursos de controles de aplicativos adaptáveis no escopo de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="52599-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="52599-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52599-108">EXAMPLES</span></span>

### <span data-ttu-id="52599-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52599-109">Example 1</span></span>
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
<span data-ttu-id="52599-110">Obtém uma lista de grupos de servidores/VM de controle do aplicativo para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="52599-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="52599-111">OS</span><span class="sxs-lookup"><span data-stu-id="52599-111">PARAMETERS</span></span>

### <span data-ttu-id="52599-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52599-112">-DefaultProfile</span></span>
<span data-ttu-id="52599-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52599-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52599-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52599-114">-SubscriptionId</span></span>
<span data-ttu-id="52599-115">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="52599-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="52599-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="52599-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="52599-117">Inclua as regras de política.</span><span class="sxs-lookup"><span data-stu-id="52599-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="52599-118">-Resumo</span><span class="sxs-lookup"><span data-stu-id="52599-118">-Summary</span></span>
<span data-ttu-id="52599-119">Retornar a saída em um formato resumido.</span><span class="sxs-lookup"><span data-stu-id="52599-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="52599-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52599-120">CommonParameters</span></span>
<span data-ttu-id="52599-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52599-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52599-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52599-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52599-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52599-123">INPUTS</span></span>

### <span data-ttu-id="52599-124">System. String</span><span class="sxs-lookup"><span data-stu-id="52599-124">System.String</span></span>

### <span data-ttu-id="52599-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52599-125">System.Boolean</span></span>

## <span data-ttu-id="52599-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52599-126">OUTPUTS</span></span>

### <span data-ttu-id="52599-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="52599-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="52599-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52599-128">NOTES</span></span>

## <span data-ttu-id="52599-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52599-129">RELATED LINKS</span></span>
