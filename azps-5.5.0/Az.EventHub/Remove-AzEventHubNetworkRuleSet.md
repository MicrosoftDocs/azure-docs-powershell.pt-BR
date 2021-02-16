---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126966"
---
# <span data-ttu-id="943fe-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="943fe-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="943fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="943fe-102">SYNOPSIS</span></span>
<span data-ttu-id="943fe-103">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="943fe-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="943fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="943fe-104">SYNTAX</span></span>

### <span data-ttu-id="943fe-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="943fe-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="943fe-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="943fe-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="943fe-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="943fe-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="943fe-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="943fe-108">DESCRIPTION</span></span>
<span data-ttu-id="943fe-109">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="943fe-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="943fe-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="943fe-110">EXAMPLES</span></span>

### <span data-ttu-id="943fe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="943fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="943fe-112">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="943fe-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="943fe-113">Exclui o NetworkRuleSet para o namespace "Eventhub-Namespace1-1375" dado</span><span class="sxs-lookup"><span data-stu-id="943fe-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="943fe-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="943fe-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="943fe-115">Exclui o NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="943fe-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="943fe-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="943fe-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="943fe-117">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="943fe-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="943fe-118">Exclui o NetworkRuleSet usando ResourceId do Namespace</span><span class="sxs-lookup"><span data-stu-id="943fe-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="943fe-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="943fe-119">PARAMETERS</span></span>

### <span data-ttu-id="943fe-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="943fe-120">-AsJob</span></span>
<span data-ttu-id="943fe-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="943fe-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="943fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943fe-122">-DefaultProfile</span></span>
<span data-ttu-id="943fe-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="943fe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="943fe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="943fe-124">-InputObject</span></span>
<span data-ttu-id="943fe-125">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="943fe-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943fe-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="943fe-126">-Name</span></span>
<span data-ttu-id="943fe-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="943fe-127">Namespace Name</span></span>

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

### <span data-ttu-id="943fe-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="943fe-128">-PassThru</span></span>
<span data-ttu-id="943fe-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="943fe-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="943fe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="943fe-130">-ResourceGroupName</span></span>
<span data-ttu-id="943fe-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="943fe-131">Resource Group Name</span></span>

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

### <span data-ttu-id="943fe-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="943fe-132">-ResourceId</span></span>
<span data-ttu-id="943fe-133">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="943fe-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="943fe-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="943fe-134">-Confirm</span></span>
<span data-ttu-id="943fe-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943fe-136">-WhatIf</span></span>
<span data-ttu-id="943fe-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="943fe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="943fe-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="943fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943fe-139">CommonParameters</span></span>
<span data-ttu-id="943fe-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="943fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="943fe-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="943fe-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943fe-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="943fe-142">INPUTS</span></span>

### <span data-ttu-id="943fe-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="943fe-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="943fe-144">System.String</span><span class="sxs-lookup"><span data-stu-id="943fe-144">System.String</span></span>

## <span data-ttu-id="943fe-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="943fe-145">OUTPUTS</span></span>

### <span data-ttu-id="943fe-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="943fe-146">System.Boolean</span></span>

## <span data-ttu-id="943fe-147">Notas</span><span class="sxs-lookup"><span data-stu-id="943fe-147">NOTES</span></span>

## <span data-ttu-id="943fe-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="943fe-148">RELATED LINKS</span></span>