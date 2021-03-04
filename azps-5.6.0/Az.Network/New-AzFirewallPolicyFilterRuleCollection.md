---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: 3bdd96bfe85d6b78476e16a49b2700131ae5aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886724"
---
# <span data-ttu-id="7a65b-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7a65b-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="7a65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a65b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a65b-103">Criar uma nova coleção de regras de filtro de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7a65b-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="7a65b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a65b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a65b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a65b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a65b-106">O cmdlet **New-AzFirewallPolicyFilterRuleCollection** cria uma coleção de regras filter para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a65b-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7a65b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a65b-107">EXAMPLES</span></span>

### <span data-ttu-id="7a65b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a65b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="7a65b-109">Este exemplo cria uma regra Filter com 2 condições de regra</span><span class="sxs-lookup"><span data-stu-id="7a65b-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="7a65b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a65b-110">PARAMETERS</span></span>

### <span data-ttu-id="7a65b-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="7a65b-111">-ActionType</span></span>
<span data-ttu-id="7a65b-112">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="7a65b-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a65b-113">-DefaultProfile</span></span>
<span data-ttu-id="7a65b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a65b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7a65b-115">-Name</span></span>
<span data-ttu-id="7a65b-116">O nome da coleção Application Rule</span><span class="sxs-lookup"><span data-stu-id="7a65b-116">The name of the Application Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="7a65b-117">-Priority</span></span>
<span data-ttu-id="7a65b-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="7a65b-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="7a65b-119">-Rule</span></span>
<span data-ttu-id="7a65b-120">A lista de regras de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a65b-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a65b-121">-Confirm</span></span>
<span data-ttu-id="7a65b-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a65b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a65b-123">-WhatIf</span></span>
<span data-ttu-id="7a65b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a65b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a65b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a65b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a65b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a65b-126">CommonParameters</span></span>
<span data-ttu-id="7a65b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a65b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a65b-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a65b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a65b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a65b-129">INPUTS</span></span>

### <span data-ttu-id="7a65b-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7a65b-130">None</span></span>

## <span data-ttu-id="7a65b-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a65b-131">OUTPUTS</span></span>

### <span data-ttu-id="7a65b-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="7a65b-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="7a65b-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a65b-133">NOTES</span></span>

## <span data-ttu-id="7a65b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a65b-134">RELATED LINKS</span></span>
