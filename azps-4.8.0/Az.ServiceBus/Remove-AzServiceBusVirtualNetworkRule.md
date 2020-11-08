---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113327"
---
# <span data-ttu-id="605f4-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="605f4-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="605f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="605f4-102">SYNOPSIS</span></span>
<span data-ttu-id="605f4-103">Remove o único VirtualNetworkRule específico para o NetworkRuleSet do namespace</span><span class="sxs-lookup"><span data-stu-id="605f4-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="605f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="605f4-104">SYNTAX</span></span>

### <span data-ttu-id="605f4-105">VirtualNetworkRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="605f4-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="605f4-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="605f4-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="605f4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="605f4-107">DESCRIPTION</span></span>
<span data-ttu-id="605f4-108">Remove o único VirtualNetworkRule específico para o NetworkRuleSet do namespace</span><span class="sxs-lookup"><span data-stu-id="605f4-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="605f4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="605f4-109">EXAMPLES</span></span>

### <span data-ttu-id="605f4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="605f4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="605f4-111">Remove o único VirtualNetworkRule específico para o NetworkRuleSet do namespace</span><span class="sxs-lookup"><span data-stu-id="605f4-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="605f4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="605f4-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="605f4-113">Remover a $virtualruleset 1 de NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="605f4-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="605f4-114">OS</span><span class="sxs-lookup"><span data-stu-id="605f4-114">PARAMETERS</span></span>

### <span data-ttu-id="605f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="605f4-115">-AsJob</span></span>
<span data-ttu-id="605f4-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="605f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="605f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605f4-117">-DefaultProfile</span></span>
<span data-ttu-id="605f4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="605f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605f4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="605f4-119">-Name</span></span>
<span data-ttu-id="605f4-120">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="605f4-120">Namespace Name</span></span>

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

### <span data-ttu-id="605f4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="605f4-121">-PassThru</span></span>
<span data-ttu-id="605f4-122">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="605f4-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="605f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="605f4-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="605f4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="605f4-125">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="605f4-125">-SubnetId</span></span>
<span data-ttu-id="605f4-126">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="605f4-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605f4-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="605f4-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="605f4-128">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="605f4-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="605f4-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="605f4-129">-Confirm</span></span>
<span data-ttu-id="605f4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="605f4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605f4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605f4-131">-WhatIf</span></span>
<span data-ttu-id="605f4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="605f4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605f4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="605f4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605f4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605f4-134">CommonParameters</span></span>
<span data-ttu-id="605f4-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="605f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="605f4-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605f4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605f4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="605f4-137">INPUTS</span></span>

### <span data-ttu-id="605f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="605f4-138">System.String</span></span>

### <span data-ttu-id="605f4-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="605f4-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="605f4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="605f4-140">OUTPUTS</span></span>

### <span data-ttu-id="605f4-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="605f4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="605f4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="605f4-142">NOTES</span></span>

## <span data-ttu-id="605f4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="605f4-143">RELATED LINKS</span></span>
