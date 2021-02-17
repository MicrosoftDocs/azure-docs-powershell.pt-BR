---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: c72573f467377a4ea16fd487a8cee5f0055a5cee
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401446"
---
# <span data-ttu-id="f1b8c-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f1b8c-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="f1b8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b8c-103">Criar Objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="f1b8c-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f1b8c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1b8c-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b8c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b8c-106">Criar Objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="f1b8c-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="f1b8c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b8c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1b8c-108">Example 1</span></span>
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

<span data-ttu-id="f1b8c-109">Criar um Objeto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f1b8c-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="f1b8c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b8c-111">-DefaultProfile</span></span>
<span data-ttu-id="f1b8c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b8c-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f1b8c-113">-RuleGroupOverride</span></span>
<span data-ttu-id="f1b8c-114">Lista de configuração de substituição do provedor gerenciado do Azure</span><span class="sxs-lookup"><span data-stu-id="f1b8c-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="f1b8c-115">-Tipo</span><span class="sxs-lookup"><span data-stu-id="f1b8c-115">-Type</span></span>
<span data-ttu-id="f1b8c-116">Tipo do ruleset</span><span class="sxs-lookup"><span data-stu-id="f1b8c-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="f1b8c-117">-Versão</span><span class="sxs-lookup"><span data-stu-id="f1b8c-117">-Version</span></span>
<span data-ttu-id="f1b8c-118">Versão do ruleset</span><span class="sxs-lookup"><span data-stu-id="f1b8c-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="f1b8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b8c-119">CommonParameters</span></span>
<span data-ttu-id="f1b8c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b8c-121">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1b8c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b8c-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1b8c-122">INPUTS</span></span>

### <span data-ttu-id="f1b8c-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f1b8c-123">None</span></span>

## <span data-ttu-id="f1b8c-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1b8c-124">OUTPUTS</span></span>

### <span data-ttu-id="f1b8c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="f1b8c-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="f1b8c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f1b8c-126">NOTES</span></span>

## <span data-ttu-id="f1b8c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b8c-127">RELATED LINKS</span></span>

<span data-ttu-id="f1b8c-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="f1b8c-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
