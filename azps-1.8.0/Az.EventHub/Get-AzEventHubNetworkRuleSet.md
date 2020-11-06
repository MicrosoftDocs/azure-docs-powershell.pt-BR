---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 29eab81028de58c8f23345249ef079f87380257a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600844"
---
# <span data-ttu-id="7c729-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c729-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="7c729-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c729-102">SYNOPSIS</span></span>
<span data-ttu-id="7c729-103">Obtém os detalhes de um NetwrokruleSet de hubs de evento de namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c729-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="7c729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c729-104">SYNTAX</span></span>

### <span data-ttu-id="7c729-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c729-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c729-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7c729-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c729-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c729-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c729-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c729-108">DESCRIPTION</span></span>
<span data-ttu-id="7c729-109">Obtém os detalhes de um NetwrokruleSet de hubs de evento de namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c729-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="7c729-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c729-110">EXAMPLES</span></span>

### <span data-ttu-id="7c729-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c729-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="7c729-112">Obtenha os detalhes dos hubs de evento NetwrokruleSet do namespace usando o Resource e os parâmetros de Namesape.</span><span class="sxs-lookup"><span data-stu-id="7c729-112">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="7c729-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7c729-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="7c729-114">Obtenha os detalhes dos hubs de eventos NetwrokruleSet de namespace usando namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7c729-114">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="7c729-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7c729-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="7c729-116">Obter os detalhes dos hubs de evento NetwrokruleSet do namespace usando a ID do recurso de outro namespace</span><span class="sxs-lookup"><span data-stu-id="7c729-116">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="7c729-117">OS</span><span class="sxs-lookup"><span data-stu-id="7c729-117">PARAMETERS</span></span>

### <span data-ttu-id="7c729-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c729-118">-DefaultProfile</span></span>
<span data-ttu-id="7c729-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c729-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c729-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c729-120">-Namespace</span></span>
<span data-ttu-id="7c729-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7c729-121">Namespace Name</span></span>

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

### <span data-ttu-id="7c729-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c729-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c729-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c729-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7c729-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c729-124">-ResourceId</span></span>
<span data-ttu-id="7c729-125">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="7c729-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="7c729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c729-126">CommonParameters</span></span>
<span data-ttu-id="7c729-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7c729-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c729-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c729-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c729-129">INPUTS</span></span>

### <span data-ttu-id="7c729-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7c729-130">System.String</span></span>

## <span data-ttu-id="7c729-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c729-131">OUTPUTS</span></span>

### <span data-ttu-id="7c729-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="7c729-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="7c729-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c729-133">NOTES</span></span>

## <span data-ttu-id="7c729-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c729-134">RELATED LINKS</span></span>