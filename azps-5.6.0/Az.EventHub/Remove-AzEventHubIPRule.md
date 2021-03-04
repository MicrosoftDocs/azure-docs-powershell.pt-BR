---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: c8a42bd69cc253d66fede2339f4080558e2f07cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889675"
---
# <span data-ttu-id="302c5-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="302c5-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="302c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302c5-102">SYNOPSIS</span></span>
<span data-ttu-id="302c5-103">Remover uma única regra IP para o NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="302c5-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="302c5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="302c5-104">SYNTAX</span></span>

### <span data-ttu-id="302c5-105">IPRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="302c5-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="302c5-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="302c5-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="302c5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="302c5-107">DESCRIPTION</span></span>
<span data-ttu-id="302c5-108">Remover uma única regra IP para o NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="302c5-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="302c5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="302c5-109">EXAMPLES</span></span>

### <span data-ttu-id="302c5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="302c5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="302c5-111">Remove IpMask do NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="302c5-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="302c5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="302c5-112">PARAMETERS</span></span>

### <span data-ttu-id="302c5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="302c5-113">-AsJob</span></span>
<span data-ttu-id="302c5-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="302c5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="302c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302c5-115">-DefaultProfile</span></span>
<span data-ttu-id="302c5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="302c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302c5-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="302c5-117">-IpMask</span></span>
<span data-ttu-id="302c5-118">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="302c5-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="302c5-119">-IpRuleObject</span></span>
<span data-ttu-id="302c5-120">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="302c5-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="302c5-121">-Name</span></span>
<span data-ttu-id="302c5-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="302c5-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="302c5-123">-PassThru</span></span>
<span data-ttu-id="302c5-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="302c5-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="302c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="302c5-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="302c5-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="302c5-127">-Confirm</span></span>
<span data-ttu-id="302c5-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302c5-129">-WhatIf</span></span>
<span data-ttu-id="302c5-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="302c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302c5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="302c5-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302c5-132">CommonParameters</span></span>
<span data-ttu-id="302c5-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="302c5-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302c5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302c5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="302c5-135">INPUTS</span></span>

### <span data-ttu-id="302c5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="302c5-136">System.String</span></span>

### <span data-ttu-id="302c5-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="302c5-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="302c5-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="302c5-138">OUTPUTS</span></span>

### <span data-ttu-id="302c5-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="302c5-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="302c5-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="302c5-140">NOTES</span></span>

## <span data-ttu-id="302c5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="302c5-141">RELATED LINKS</span></span>