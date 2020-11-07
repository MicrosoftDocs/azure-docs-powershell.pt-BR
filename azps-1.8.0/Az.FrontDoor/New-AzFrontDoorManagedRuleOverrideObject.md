---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770850"
---
# <span data-ttu-id="35232-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="35232-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="35232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35232-102">SYNOPSIS</span></span>
<span data-ttu-id="35232-103">Criar objeto de substituição de regra gerenciada</span><span class="sxs-lookup"><span data-stu-id="35232-103">Create managed rule override object</span></span>

## <span data-ttu-id="35232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35232-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35232-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35232-105">DESCRIPTION</span></span>
<span data-ttu-id="35232-106">Criar objeto PSAzureManagedRuleOverride para grupo de regras gerenciado WAF substituir a criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="35232-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="35232-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35232-107">EXAMPLES</span></span>

### <span data-ttu-id="35232-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35232-108">Example 1</span></span>
<span data-ttu-id="35232-109">Crie um objeto de substituição de regra gerenciada para a regra 942250 (que está no grupo SQLI).</span><span class="sxs-lookup"><span data-stu-id="35232-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="35232-110">OS</span><span class="sxs-lookup"><span data-stu-id="35232-110">PARAMETERS</span></span>

### <span data-ttu-id="35232-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="35232-111">-Action</span></span>
<span data-ttu-id="35232-112">Ação de substituição</span><span class="sxs-lookup"><span data-stu-id="35232-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35232-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35232-113">-DefaultProfile</span></span>
<span data-ttu-id="35232-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35232-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35232-115">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="35232-115">-Disabled</span></span>
<span data-ttu-id="35232-116">Estado desabilitado</span><span class="sxs-lookup"><span data-stu-id="35232-116">Disabled state</span></span>

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

### <span data-ttu-id="35232-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="35232-117">-RuleId</span></span>
<span data-ttu-id="35232-118">ID da regra</span><span class="sxs-lookup"><span data-stu-id="35232-118">Rule ID</span></span>

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

### <span data-ttu-id="35232-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35232-119">CommonParameters</span></span>
<span data-ttu-id="35232-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35232-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35232-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35232-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35232-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35232-122">INPUTS</span></span>

### <span data-ttu-id="35232-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35232-123">None</span></span>

## <span data-ttu-id="35232-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35232-124">OUTPUTS</span></span>

### <span data-ttu-id="35232-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="35232-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="35232-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35232-126">NOTES</span></span>

## <span data-ttu-id="35232-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35232-127">RELATED LINKS</span></span>

[<span data-ttu-id="35232-128">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="35232-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)