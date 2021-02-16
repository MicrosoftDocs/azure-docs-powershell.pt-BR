---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126960"
---
# <span data-ttu-id="61068-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="61068-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="61068-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61068-102">SYNOPSIS</span></span>
<span data-ttu-id="61068-103">Obter definições de conjunto de regras gerenciados por WAF</span><span class="sxs-lookup"><span data-stu-id="61068-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="61068-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61068-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61068-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="61068-105">DESCRIPTION</span></span>
<span data-ttu-id="61068-106">Obtém a lista de definições de conjunto de regras gerenciados por WAF a ser usada como referência</span><span class="sxs-lookup"><span data-stu-id="61068-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="61068-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61068-107">EXAMPLES</span></span>

### <span data-ttu-id="61068-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61068-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="61068-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="61068-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="61068-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61068-110">PARAMETERS</span></span>

### <span data-ttu-id="61068-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61068-111">-DefaultProfile</span></span>
<span data-ttu-id="61068-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61068-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61068-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61068-113">CommonParameters</span></span>
<span data-ttu-id="61068-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61068-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61068-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61068-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61068-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="61068-116">INPUTS</span></span>

### <span data-ttu-id="61068-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61068-117">None</span></span>

## <span data-ttu-id="61068-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="61068-118">OUTPUTS</span></span>

### <span data-ttu-id="61068-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="61068-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="61068-120">Notas</span><span class="sxs-lookup"><span data-stu-id="61068-120">NOTES</span></span>

## <span data-ttu-id="61068-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61068-121">RELATED LINKS</span></span>

<span data-ttu-id="61068-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="61068-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
