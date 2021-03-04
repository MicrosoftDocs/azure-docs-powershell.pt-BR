---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: e550afd0b7f580c46b15bd8b6ac68b3b0ad1bc89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886039"
---
# <span data-ttu-id="f2e79-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e79-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="f2e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e79-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e79-103">Obtém os detalhes de um namespace hubs de eventos ou obtém uma lista de todos os namespaces de Hubs de Eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e79-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="f2e79-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2e79-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e79-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2e79-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e79-106">O Get-AzEventHubNamespace cmdlet obtém os detalhes de um namespace de Hubs de Eventos especificado ou uma lista de todos os namespaces de Hubs de Eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e79-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="f2e79-107">Se o nome do namespace for fornecido, os detalhes de um único namespace de Hubs de Eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="f2e79-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="f2e79-108">Se o nome do namespace não for fornecido, uma lista de namespaces será retornada.</span><span class="sxs-lookup"><span data-stu-id="f2e79-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="f2e79-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2e79-109">EXAMPLES</span></span>

### <span data-ttu-id="f2e79-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2e79-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="f2e79-111">Obtém os detalhes do namespace \` MyNamespaceName \` no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f2e79-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f2e79-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2e79-112">PARAMETERS</span></span>

### <span data-ttu-id="f2e79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e79-113">-DefaultProfile</span></span>
<span data-ttu-id="f2e79-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2e79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2e79-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f2e79-115">-Name</span></span>
<span data-ttu-id="f2e79-116">Nome do Namespace EventHub</span><span class="sxs-lookup"><span data-stu-id="f2e79-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e79-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2e79-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f2e79-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e79-119">CommonParameters</span></span>
<span data-ttu-id="f2e79-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e79-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e79-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e79-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2e79-122">INPUTS</span></span>

### <span data-ttu-id="f2e79-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f2e79-123">System.String</span></span>

## <span data-ttu-id="f2e79-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2e79-124">OUTPUTS</span></span>

### <span data-ttu-id="f2e79-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f2e79-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f2e79-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2e79-126">NOTES</span></span>

## <span data-ttu-id="f2e79-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2e79-127">RELATED LINKS</span></span>
