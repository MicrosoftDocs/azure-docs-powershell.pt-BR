---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262052"
---
# <span data-ttu-id="e9c22-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e9c22-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="e9c22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c22-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c22-103">Criar uma nova coleção de regras de filtro de política do firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e9c22-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="e9c22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9c22-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c22-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9c22-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c22-106">O cmdlet **New-AzFirewallPolicyFilterRuleCollection** cria uma coleção de regras de filtro para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c22-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e9c22-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9c22-107">EXAMPLES</span></span>

### <span data-ttu-id="e9c22-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9c22-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="e9c22-109">Este exemplo cria uma regra de filtro com duas condições de regra</span><span class="sxs-lookup"><span data-stu-id="e9c22-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="e9c22-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9c22-110">PARAMETERS</span></span>

### <span data-ttu-id="e9c22-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="e9c22-111">-ActionType</span></span>
<span data-ttu-id="e9c22-112">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="e9c22-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="e9c22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c22-113">-DefaultProfile</span></span>
<span data-ttu-id="e9c22-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c22-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9c22-115">-Name</span></span>
<span data-ttu-id="e9c22-116">O nome da coleção de regras do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e9c22-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="e9c22-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="e9c22-117">-Priority</span></span>
<span data-ttu-id="e9c22-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="e9c22-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="e9c22-119">-Regra</span><span class="sxs-lookup"><span data-stu-id="e9c22-119">-Rule</span></span>
<span data-ttu-id="e9c22-120">A lista de regras do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e9c22-120">The list of application rules</span></span>

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

### <span data-ttu-id="e9c22-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9c22-121">-Confirm</span></span>
<span data-ttu-id="e9c22-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9c22-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c22-123">-WhatIf</span></span>
<span data-ttu-id="e9c22-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9c22-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c22-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9c22-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c22-126">CommonParameters</span></span>
<span data-ttu-id="e9c22-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c22-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9c22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c22-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9c22-129">INPUTS</span></span>

### <span data-ttu-id="e9c22-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e9c22-130">None</span></span>

## <span data-ttu-id="e9c22-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9c22-131">OUTPUTS</span></span>

### <span data-ttu-id="e9c22-132">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="e9c22-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="e9c22-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9c22-133">NOTES</span></span>

## <span data-ttu-id="e9c22-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c22-134">RELATED LINKS</span></span>
