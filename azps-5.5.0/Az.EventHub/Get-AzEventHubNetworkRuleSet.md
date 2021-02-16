---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113200"
---
# <span data-ttu-id="577d6-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="577d6-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="577d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="577d6-102">SYNOPSIS</span></span>
<span data-ttu-id="577d6-103">Obtém os detalhes de um NetworkruleSet de Hubs de Eventos do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="577d6-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="577d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="577d6-104">SYNTAX</span></span>

### <span data-ttu-id="577d6-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="577d6-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="577d6-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="577d6-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="577d6-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="577d6-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="577d6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="577d6-108">DESCRIPTION</span></span>
<span data-ttu-id="577d6-109">Obtém os detalhes de um NetworkruleSet de Hubs de Eventos do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="577d6-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="577d6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="577d6-110">EXAMPLES</span></span>

### <span data-ttu-id="577d6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="577d6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="577d6-112">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando parâmetros ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="577d6-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="577d6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="577d6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="577d6-114">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando o Namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="577d6-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="577d6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="577d6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="577d6-116">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando a ID de Recurso de outro Namespace</span><span class="sxs-lookup"><span data-stu-id="577d6-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="577d6-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="577d6-117">PARAMETERS</span></span>

### <span data-ttu-id="577d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577d6-118">-DefaultProfile</span></span>
<span data-ttu-id="577d6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="577d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577d6-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="577d6-120">-Namespace</span></span>
<span data-ttu-id="577d6-121">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="577d6-121">Namespace Name</span></span>

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

### <span data-ttu-id="577d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="577d6-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="577d6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="577d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="577d6-124">-ResourceId</span></span>
<span data-ttu-id="577d6-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="577d6-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="577d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577d6-126">CommonParameters</span></span>
<span data-ttu-id="577d6-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="577d6-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577d6-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="577d6-129">INPUTS</span></span>

### <span data-ttu-id="577d6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="577d6-130">System.String</span></span>

## <span data-ttu-id="577d6-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="577d6-131">OUTPUTS</span></span>

### <span data-ttu-id="577d6-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="577d6-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="577d6-133">Notas</span><span class="sxs-lookup"><span data-stu-id="577d6-133">NOTES</span></span>

## <span data-ttu-id="577d6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="577d6-134">RELATED LINKS</span></span>