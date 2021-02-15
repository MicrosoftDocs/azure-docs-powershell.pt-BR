---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112597"
---
# <span data-ttu-id="82d4e-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="82d4e-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="82d4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="82d4e-103">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="82d4e-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="82d4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82d4e-104">SYNTAX</span></span>

### <span data-ttu-id="82d4e-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="82d4e-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82d4e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82d4e-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82d4e-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82d4e-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82d4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="82d4e-108">DESCRIPTION</span></span>
<span data-ttu-id="82d4e-109">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="82d4e-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="82d4e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82d4e-110">EXAMPLES</span></span>

### <span data-ttu-id="82d4e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82d4e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="82d4e-112">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="82d4e-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82d4e-113">Exclui o NetworkRuleSet do namespace "ServiceBus-Namespace1-1375" dado</span><span class="sxs-lookup"><span data-stu-id="82d4e-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="82d4e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="82d4e-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="82d4e-115">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="82d4e-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82d4e-116">Exclui o NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="82d4e-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="82d4e-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="82d4e-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="82d4e-118">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="82d4e-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="82d4e-119">Exclui o NetworkRuleSet usando ResourceId do Namespace</span><span class="sxs-lookup"><span data-stu-id="82d4e-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="82d4e-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82d4e-120">PARAMETERS</span></span>

### <span data-ttu-id="82d4e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82d4e-121">-AsJob</span></span>
<span data-ttu-id="82d4e-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="82d4e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82d4e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d4e-123">-DefaultProfile</span></span>
<span data-ttu-id="82d4e-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82d4e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82d4e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82d4e-125">-InputObject</span></span>
<span data-ttu-id="82d4e-126">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="82d4e-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82d4e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="82d4e-127">-Name</span></span>
<span data-ttu-id="82d4e-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="82d4e-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d4e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82d4e-129">-PassThru</span></span>
<span data-ttu-id="82d4e-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82d4e-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="82d4e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d4e-131">-ResourceGroupName</span></span>
<span data-ttu-id="82d4e-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="82d4e-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d4e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82d4e-133">-ResourceId</span></span>
<span data-ttu-id="82d4e-134">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="82d4e-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82d4e-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="82d4e-135">-Confirm</span></span>
<span data-ttu-id="82d4e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82d4e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82d4e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82d4e-137">-WhatIf</span></span>
<span data-ttu-id="82d4e-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="82d4e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82d4e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82d4e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82d4e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d4e-140">CommonParameters</span></span>
<span data-ttu-id="82d4e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d4e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82d4e-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d4e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d4e-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="82d4e-143">INPUTS</span></span>

### <span data-ttu-id="82d4e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="82d4e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="82d4e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="82d4e-145">System.String</span></span>

## <span data-ttu-id="82d4e-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="82d4e-146">OUTPUTS</span></span>

### <span data-ttu-id="82d4e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82d4e-147">System.Boolean</span></span>

## <span data-ttu-id="82d4e-148">Notas</span><span class="sxs-lookup"><span data-stu-id="82d4e-148">NOTES</span></span>

## <span data-ttu-id="82d4e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82d4e-149">RELATED LINKS</span></span>
