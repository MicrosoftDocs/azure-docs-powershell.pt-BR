---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943837"
---
# <span data-ttu-id="379d4-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="379d4-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="379d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="379d4-102">SYNOPSIS</span></span>
<span data-ttu-id="379d4-103">Criar objeto de substituição de regra gerenciada</span><span class="sxs-lookup"><span data-stu-id="379d4-103">Create managed rule override object</span></span>

## <span data-ttu-id="379d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="379d4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="379d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="379d4-105">DESCRIPTION</span></span>
<span data-ttu-id="379d4-106">Criar objeto PSAzureManagedRuleOverride para grupo de regras gerenciado WAF substituir a criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="379d4-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="379d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="379d4-107">EXAMPLES</span></span>

### <span data-ttu-id="379d4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="379d4-108">Example 1</span></span>
<span data-ttu-id="379d4-109">Crie um objeto de substituição de regra gerenciada para a regra 942250 (que está no grupo SQLI).</span><span class="sxs-lookup"><span data-stu-id="379d4-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="379d4-110">OS</span><span class="sxs-lookup"><span data-stu-id="379d4-110">PARAMETERS</span></span>

### <span data-ttu-id="379d4-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="379d4-111">-Action</span></span>
<span data-ttu-id="379d4-112">Ação de substituição</span><span class="sxs-lookup"><span data-stu-id="379d4-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379d4-113">-DefaultProfile</span></span>
<span data-ttu-id="379d4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="379d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379d4-115">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="379d4-115">-Disabled</span></span>
<span data-ttu-id="379d4-116">Estado desabilitado</span><span class="sxs-lookup"><span data-stu-id="379d4-116">Disabled state</span></span>

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

### <span data-ttu-id="379d4-117">-Exclusão</span><span class="sxs-lookup"><span data-stu-id="379d4-117">-Exclusion</span></span>
<span data-ttu-id="379d4-118">Excluídos</span><span class="sxs-lookup"><span data-stu-id="379d4-118">Exclusion</span></span>

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

### <span data-ttu-id="379d4-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="379d4-119">-RuleId</span></span>
<span data-ttu-id="379d4-120">ID da regra</span><span class="sxs-lookup"><span data-stu-id="379d4-120">Rule ID</span></span>

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

### <span data-ttu-id="379d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379d4-121">CommonParameters</span></span>
<span data-ttu-id="379d4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379d4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="379d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379d4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="379d4-124">INPUTS</span></span>

### <span data-ttu-id="379d4-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="379d4-125">None</span></span>

## <span data-ttu-id="379d4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="379d4-126">OUTPUTS</span></span>

### <span data-ttu-id="379d4-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="379d4-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="379d4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="379d4-128">NOTES</span></span>

## <span data-ttu-id="379d4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="379d4-129">RELATED LINKS</span></span>

[<span data-ttu-id="379d4-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="379d4-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)