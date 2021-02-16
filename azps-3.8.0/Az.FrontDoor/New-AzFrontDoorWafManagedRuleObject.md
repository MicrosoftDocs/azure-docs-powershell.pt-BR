---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403945"
---
# <span data-ttu-id="48197-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="48197-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="48197-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48197-102">SYNOPSIS</span></span>
<span data-ttu-id="48197-103">Criar Objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="48197-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="48197-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48197-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48197-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="48197-105">DESCRIPTION</span></span>
<span data-ttu-id="48197-106">Criar Objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="48197-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="48197-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48197-107">EXAMPLES</span></span>

### <span data-ttu-id="48197-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48197-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="48197-109">Criar um Objeto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="48197-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="48197-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48197-110">PARAMETERS</span></span>

### <span data-ttu-id="48197-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48197-111">-DefaultProfile</span></span>
<span data-ttu-id="48197-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48197-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48197-113">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="48197-113">-Exclusion</span></span>
<span data-ttu-id="48197-114">Exclusão</span><span class="sxs-lookup"><span data-stu-id="48197-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48197-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="48197-115">-RuleGroupOverride</span></span>
<span data-ttu-id="48197-116">Lista de configuração de substituição do provedor gerenciado do Azure</span><span class="sxs-lookup"><span data-stu-id="48197-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48197-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="48197-117">-Type</span></span>
<span data-ttu-id="48197-118">Tipo do ruleset</span><span class="sxs-lookup"><span data-stu-id="48197-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="48197-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="48197-119">-Version</span></span>
<span data-ttu-id="48197-120">Versão do ruleset</span><span class="sxs-lookup"><span data-stu-id="48197-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="48197-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48197-121">CommonParameters</span></span>
<span data-ttu-id="48197-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48197-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48197-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48197-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48197-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="48197-124">INPUTS</span></span>

### <span data-ttu-id="48197-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="48197-125">None</span></span>

## <span data-ttu-id="48197-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="48197-126">OUTPUTS</span></span>

### <span data-ttu-id="48197-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="48197-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="48197-128">Notas</span><span class="sxs-lookup"><span data-stu-id="48197-128">NOTES</span></span>

## <span data-ttu-id="48197-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48197-129">RELATED LINKS</span></span>

<span data-ttu-id="48197-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="48197-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
