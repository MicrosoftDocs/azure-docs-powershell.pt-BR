---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f79188c2d45582b8ecdbd52a9fa6931a4cc90b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775864"
---
# <span data-ttu-id="53ae2-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="53ae2-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="53ae2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="53ae2-103">Remove o NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="53ae2-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="53ae2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ae2-104">SYNTAX</span></span>

### <span data-ttu-id="53ae2-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="53ae2-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53ae2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="53ae2-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53ae2-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53ae2-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ae2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ae2-108">DESCRIPTION</span></span>
<span data-ttu-id="53ae2-109">Remove o NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="53ae2-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="53ae2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ae2-110">EXAMPLES</span></span>

### <span data-ttu-id="53ae2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53ae2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="53ae2-112">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="53ae2-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="53ae2-113">Exclui o NetworkRuleSet para o namespace "Eventhub-Namespace1-1375" especificado</span><span class="sxs-lookup"><span data-stu-id="53ae2-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="53ae2-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53ae2-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="53ae2-115">Exclui o NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="53ae2-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="53ae2-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="53ae2-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="53ae2-117">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="53ae2-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="53ae2-118">Exclui o NetworkRuleSet usando o ResourceId do namespace</span><span class="sxs-lookup"><span data-stu-id="53ae2-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="53ae2-119">OS</span><span class="sxs-lookup"><span data-stu-id="53ae2-119">PARAMETERS</span></span>

### <span data-ttu-id="53ae2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53ae2-120">-AsJob</span></span>
<span data-ttu-id="53ae2-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="53ae2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53ae2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ae2-122">-DefaultProfile</span></span>
<span data-ttu-id="53ae2-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53ae2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53ae2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53ae2-124">-InputObject</span></span>
<span data-ttu-id="53ae2-125">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="53ae2-125">Namespace Object</span></span>

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

### <span data-ttu-id="53ae2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="53ae2-126">-Name</span></span>
<span data-ttu-id="53ae2-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="53ae2-127">Namespace Name</span></span>

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

### <span data-ttu-id="53ae2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53ae2-128">-PassThru</span></span>
<span data-ttu-id="53ae2-129">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="53ae2-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="53ae2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ae2-130">-ResourceGroupName</span></span>
<span data-ttu-id="53ae2-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="53ae2-131">Resource Group Name</span></span>

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

### <span data-ttu-id="53ae2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53ae2-132">-ResourceId</span></span>
<span data-ttu-id="53ae2-133">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="53ae2-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="53ae2-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53ae2-134">-Confirm</span></span>
<span data-ttu-id="53ae2-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53ae2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ae2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ae2-136">-WhatIf</span></span>
<span data-ttu-id="53ae2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53ae2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ae2-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53ae2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ae2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ae2-139">CommonParameters</span></span>
<span data-ttu-id="53ae2-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ae2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53ae2-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ae2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ae2-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ae2-142">INPUTS</span></span>

### <span data-ttu-id="53ae2-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="53ae2-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="53ae2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="53ae2-144">System.String</span></span>

## <span data-ttu-id="53ae2-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ae2-145">OUTPUTS</span></span>

### <span data-ttu-id="53ae2-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53ae2-146">System.Boolean</span></span>

## <span data-ttu-id="53ae2-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ae2-147">NOTES</span></span>

## <span data-ttu-id="53ae2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ae2-148">RELATED LINKS</span></span>