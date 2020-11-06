---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: cbac380f317025154f25c3c4dfe449832c864741
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596489"
---
# <span data-ttu-id="c4495-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4495-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="c4495-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4495-102">SYNOPSIS</span></span>
<span data-ttu-id="c4495-103">Obtém os detalhes de um NetworkruleSet de hubs de evento de namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4495-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="c4495-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4495-104">SYNTAX</span></span>

### <span data-ttu-id="c4495-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4495-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4495-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c4495-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4495-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4495-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4495-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4495-108">DESCRIPTION</span></span>
<span data-ttu-id="c4495-109">Obtém os detalhes de um NetworkruleSet de hubs de evento de namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4495-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="c4495-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4495-110">EXAMPLES</span></span>

### <span data-ttu-id="c4495-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4495-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="c4495-112">Obtenha os detalhes dos hubs de evento NetworkruleSet do namespace usando o Resource e os parâmetros de namespace.</span><span class="sxs-lookup"><span data-stu-id="c4495-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="c4495-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c4495-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="c4495-114">Obtenha os detalhes dos hubs de eventos NetworkruleSet de namespace usando namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c4495-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="c4495-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c4495-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="c4495-116">Obter os detalhes dos hubs de evento NetworkruleSet do namespace usando a ID do recurso de outro namespace</span><span class="sxs-lookup"><span data-stu-id="c4495-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="c4495-117">OS</span><span class="sxs-lookup"><span data-stu-id="c4495-117">PARAMETERS</span></span>

### <span data-ttu-id="c4495-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4495-118">-DefaultProfile</span></span>
<span data-ttu-id="c4495-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4495-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4495-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4495-120">-Namespace</span></span>
<span data-ttu-id="c4495-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c4495-121">Namespace Name</span></span>

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

### <span data-ttu-id="c4495-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4495-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4495-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c4495-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c4495-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4495-124">-ResourceId</span></span>
<span data-ttu-id="c4495-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="c4495-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c4495-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4495-126">CommonParameters</span></span>
<span data-ttu-id="c4495-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4495-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c4495-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4495-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4495-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4495-129">INPUTS</span></span>

### <span data-ttu-id="c4495-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c4495-130">System.String</span></span>

## <span data-ttu-id="c4495-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4495-131">OUTPUTS</span></span>

### <span data-ttu-id="c4495-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="c4495-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="c4495-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4495-133">NOTES</span></span>

## <span data-ttu-id="c4495-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4495-134">RELATED LINKS</span></span>