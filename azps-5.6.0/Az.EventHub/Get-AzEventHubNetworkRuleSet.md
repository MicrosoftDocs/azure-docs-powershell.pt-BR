---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886037"
---
# <span data-ttu-id="408db-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="408db-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="408db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408db-102">SYNOPSIS</span></span>
<span data-ttu-id="408db-103">Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="408db-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="408db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="408db-104">SYNTAX</span></span>

### <span data-ttu-id="408db-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="408db-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="408db-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="408db-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="408db-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="408db-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="408db-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="408db-108">DESCRIPTION</span></span>
<span data-ttu-id="408db-109">Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="408db-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="408db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="408db-110">EXAMPLES</span></span>

### <span data-ttu-id="408db-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="408db-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="408db-112">Obter os detalhes de Event Hubs NetworkruleSet do namespace usando parâmetros ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="408db-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="408db-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="408db-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="408db-114">Obter os detalhes de Event Hubs NetworkruleSet do namespace usando Namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="408db-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="408db-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="408db-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="408db-116">Obter os detalhes de Hubs de Eventos NetworkruleSet do namespace usando a ID de Recurso de outro Namespace</span><span class="sxs-lookup"><span data-stu-id="408db-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="408db-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="408db-117">PARAMETERS</span></span>

### <span data-ttu-id="408db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408db-118">-DefaultProfile</span></span>
<span data-ttu-id="408db-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="408db-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408db-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="408db-120">-Namespace</span></span>
<span data-ttu-id="408db-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="408db-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408db-122">-ResourceGroupName</span></span>
<span data-ttu-id="408db-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="408db-123">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408db-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="408db-124">-ResourceId</span></span>
<span data-ttu-id="408db-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="408db-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="408db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408db-126">CommonParameters</span></span>
<span data-ttu-id="408db-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="408db-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408db-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408db-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="408db-129">INPUTS</span></span>

### <span data-ttu-id="408db-130">System.String</span><span class="sxs-lookup"><span data-stu-id="408db-130">System.String</span></span>

## <span data-ttu-id="408db-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="408db-131">OUTPUTS</span></span>

### <span data-ttu-id="408db-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="408db-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="408db-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="408db-133">NOTES</span></span>

## <span data-ttu-id="408db-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="408db-134">RELATED LINKS</span></span>