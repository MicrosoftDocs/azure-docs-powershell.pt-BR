---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426933"
---
# <span data-ttu-id="30881-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="30881-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="30881-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30881-102">SYNOPSIS</span></span>
<span data-ttu-id="30881-103">Obter definições do conjunto de regras de gerenciamento WAF</span><span class="sxs-lookup"><span data-stu-id="30881-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="30881-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30881-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30881-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30881-105">DESCRIPTION</span></span>
<span data-ttu-id="30881-106">Obtém a lista de definições de conjuntos de regras gerenciadas WAF para usar como referência</span><span class="sxs-lookup"><span data-stu-id="30881-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="30881-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30881-107">EXAMPLES</span></span>

### <span data-ttu-id="30881-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30881-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="30881-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="30881-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="30881-110">OS</span><span class="sxs-lookup"><span data-stu-id="30881-110">PARAMETERS</span></span>

### <span data-ttu-id="30881-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30881-111">-DefaultProfile</span></span>
<span data-ttu-id="30881-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30881-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30881-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30881-113">CommonParameters</span></span>
<span data-ttu-id="30881-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30881-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30881-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30881-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30881-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30881-116">INPUTS</span></span>

### <span data-ttu-id="30881-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="30881-117">None</span></span>

## <span data-ttu-id="30881-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30881-118">OUTPUTS</span></span>

### <span data-ttu-id="30881-119">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="30881-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="30881-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30881-120">NOTES</span></span>

## <span data-ttu-id="30881-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30881-121">RELATED LINKS</span></span>

<span data-ttu-id="30881-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="30881-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
