---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: b6035e991b585ba296a9fdc591ccbdb44dd1b089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770852"
---
# <span data-ttu-id="4bc1d-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4bc1d-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="4bc1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc1d-103">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="4bc1d-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4bc1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bc1d-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bc1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bc1d-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc1d-106">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="4bc1d-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4bc1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bc1d-107">EXAMPLES</span></span>

### <span data-ttu-id="4bc1d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bc1d-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="4bc1d-109">Criar um objeto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="4bc1d-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="4bc1d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4bc1d-110">PARAMETERS</span></span>

### <span data-ttu-id="4bc1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc1d-111">-DefaultProfile</span></span>
<span data-ttu-id="4bc1d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc1d-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4bc1d-113">-RuleGroupOverride</span></span>
<span data-ttu-id="4bc1d-114">Lista de configurações de substituição do provedor gerenciado do Azure</span><span class="sxs-lookup"><span data-stu-id="4bc1d-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="4bc1d-115">-Digite</span><span class="sxs-lookup"><span data-stu-id="4bc1d-115">-Type</span></span>
<span data-ttu-id="4bc1d-116">Tipo de RuleSet</span><span class="sxs-lookup"><span data-stu-id="4bc1d-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="4bc1d-117">-Versão</span><span class="sxs-lookup"><span data-stu-id="4bc1d-117">-Version</span></span>
<span data-ttu-id="4bc1d-118">Versão do RuleSet</span><span class="sxs-lookup"><span data-stu-id="4bc1d-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="4bc1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc1d-119">CommonParameters</span></span>
<span data-ttu-id="4bc1d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc1d-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bc1d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc1d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bc1d-122">INPUTS</span></span>

### <span data-ttu-id="4bc1d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4bc1d-123">None</span></span>

## <span data-ttu-id="4bc1d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bc1d-124">OUTPUTS</span></span>

### <span data-ttu-id="4bc1d-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="4bc1d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="4bc1d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bc1d-126">NOTES</span></span>

## <span data-ttu-id="4bc1d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bc1d-127">RELATED LINKS</span></span>

<span data-ttu-id="4bc1d-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="4bc1d-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
