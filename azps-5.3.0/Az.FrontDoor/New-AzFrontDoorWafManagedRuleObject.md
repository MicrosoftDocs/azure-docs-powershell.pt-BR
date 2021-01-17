---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 266d553f70cb5c128df1d266f95ee93cb1eb013c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429352"
---
# <span data-ttu-id="32082-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="32082-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="32082-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32082-102">SYNOPSIS</span></span>
<span data-ttu-id="32082-103">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="32082-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="32082-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32082-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32082-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32082-105">DESCRIPTION</span></span>
<span data-ttu-id="32082-106">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="32082-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="32082-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32082-107">EXAMPLES</span></span>

### <span data-ttu-id="32082-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32082-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="32082-109">Criar um objeto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="32082-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="32082-110">OS</span><span class="sxs-lookup"><span data-stu-id="32082-110">PARAMETERS</span></span>

### <span data-ttu-id="32082-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32082-111">-DefaultProfile</span></span>
<span data-ttu-id="32082-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32082-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32082-113">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="32082-113">-Exclusion</span></span>
<span data-ttu-id="32082-114">Excluídos</span><span class="sxs-lookup"><span data-stu-id="32082-114">Exclusion</span></span>

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

### <span data-ttu-id="32082-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="32082-115">-RuleGroupOverride</span></span>
<span data-ttu-id="32082-116">Lista de configurações de substituição do provedor gerenciado do Azure</span><span class="sxs-lookup"><span data-stu-id="32082-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="32082-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="32082-117">-Type</span></span>
<span data-ttu-id="32082-118">Tipo de RuleSet</span><span class="sxs-lookup"><span data-stu-id="32082-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="32082-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="32082-119">-Version</span></span>
<span data-ttu-id="32082-120">Versão do RuleSet</span><span class="sxs-lookup"><span data-stu-id="32082-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="32082-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32082-121">CommonParameters</span></span>
<span data-ttu-id="32082-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32082-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32082-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32082-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32082-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32082-124">INPUTS</span></span>

### <span data-ttu-id="32082-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="32082-125">None</span></span>

## <span data-ttu-id="32082-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32082-126">OUTPUTS</span></span>

### <span data-ttu-id="32082-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="32082-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="32082-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32082-128">NOTES</span></span>

## <span data-ttu-id="32082-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32082-129">RELATED LINKS</span></span>

<span data-ttu-id="32082-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="32082-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
