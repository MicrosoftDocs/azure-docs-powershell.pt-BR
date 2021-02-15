---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114683"
---
# <span data-ttu-id="5a6ea-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5a6ea-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="5a6ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6ea-103">Criar um novo Conjunto de Regras de Filtro de Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5a6ea-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="5a6ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a6ea-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6ea-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="5a6ea-106">O cmdlet **New-AzFirewallPolicyFilterRuleCollection** cria um conjunto de regras de Filtro para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5a6ea-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a6ea-107">EXAMPLES</span></span>

### <span data-ttu-id="5a6ea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a6ea-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="5a6ea-109">Este exemplo cria uma regra de Filtro com 2 condições de regra</span><span class="sxs-lookup"><span data-stu-id="5a6ea-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="5a6ea-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a6ea-110">PARAMETERS</span></span>

### <span data-ttu-id="5a6ea-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="5a6ea-111">-ActionType</span></span>
<span data-ttu-id="5a6ea-112">A ação da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="5a6ea-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="5a6ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6ea-113">-DefaultProfile</span></span>
<span data-ttu-id="5a6ea-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a6ea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a6ea-115">-Name</span></span>
<span data-ttu-id="5a6ea-116">O nome do Conjunto de Regras de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a6ea-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="5a6ea-117">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="5a6ea-117">-Priority</span></span>
<span data-ttu-id="5a6ea-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="5a6ea-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="5a6ea-119">-Regra</span><span class="sxs-lookup"><span data-stu-id="5a6ea-119">-Rule</span></span>
<span data-ttu-id="5a6ea-120">A lista de regras do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a6ea-120">The list of application rules</span></span>

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

### <span data-ttu-id="5a6ea-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5a6ea-121">-Confirm</span></span>
<span data-ttu-id="5a6ea-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6ea-123">-WhatIf</span></span>
<span data-ttu-id="5a6ea-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6ea-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6ea-126">CommonParameters</span></span>
<span data-ttu-id="5a6ea-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6ea-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a6ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6ea-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a6ea-129">INPUTS</span></span>

### <span data-ttu-id="5a6ea-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5a6ea-130">None</span></span>

## <span data-ttu-id="5a6ea-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a6ea-131">OUTPUTS</span></span>

### <span data-ttu-id="5a6ea-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="5a6ea-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="5a6ea-133">Notas</span><span class="sxs-lookup"><span data-stu-id="5a6ea-133">NOTES</span></span>

## <span data-ttu-id="5a6ea-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a6ea-134">RELATED LINKS</span></span>
