---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: 28c4278f86600b53b64d3a0ea2d0b4896f8227bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885723"
---
# <span data-ttu-id="97a00-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="97a00-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="97a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a00-102">SYNOPSIS</span></span>
<span data-ttu-id="97a00-103">Obter definições de conjunto de regras gerenciadas waf</span><span class="sxs-lookup"><span data-stu-id="97a00-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="97a00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="97a00-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a00-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="97a00-105">DESCRIPTION</span></span>
<span data-ttu-id="97a00-106">Obtém a lista de definições de conjunto de regras gerenciadas waf a ser usada como referência</span><span class="sxs-lookup"><span data-stu-id="97a00-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="97a00-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97a00-107">EXAMPLES</span></span>

### <span data-ttu-id="97a00-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97a00-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="97a00-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="97a00-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="97a00-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="97a00-110">PARAMETERS</span></span>

### <span data-ttu-id="97a00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a00-111">-DefaultProfile</span></span>
<span data-ttu-id="97a00-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97a00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a00-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a00-113">CommonParameters</span></span>
<span data-ttu-id="97a00-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a00-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a00-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97a00-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a00-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97a00-116">INPUTS</span></span>

### <span data-ttu-id="97a00-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="97a00-117">None</span></span>

## <span data-ttu-id="97a00-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="97a00-118">OUTPUTS</span></span>

### <span data-ttu-id="97a00-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="97a00-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="97a00-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="97a00-120">NOTES</span></span>

## <span data-ttu-id="97a00-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97a00-121">RELATED LINKS</span></span>

<span data-ttu-id="97a00-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="97a00-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
