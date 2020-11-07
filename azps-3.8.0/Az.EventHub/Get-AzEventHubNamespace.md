---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941875"
---
# <span data-ttu-id="3acd3-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3acd3-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="3acd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3acd3-102">SYNOPSIS</span></span>
<span data-ttu-id="3acd3-103">Obtém os detalhes de um namespace de hubs de eventos ou obtém uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3acd3-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="3acd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3acd3-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3acd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3acd3-105">DESCRIPTION</span></span>
<span data-ttu-id="3acd3-106">O cmdlet Get-AzEventHubNamespace Obtém os detalhes de um namespace de hubs de eventos especificado ou uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3acd3-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="3acd3-107">Se o nome do namespace for fornecido, os detalhes de um único namespace de hubs de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="3acd3-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="3acd3-108">Se o nome do namespace não for fornecido, uma lista de namespaces será retornada.</span><span class="sxs-lookup"><span data-stu-id="3acd3-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="3acd3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3acd3-109">EXAMPLES</span></span>

### <span data-ttu-id="3acd3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3acd3-110">Example 1</span></span>
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

<span data-ttu-id="3acd3-111">Obtém os detalhes do namespace \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="3acd3-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3acd3-112">OS</span><span class="sxs-lookup"><span data-stu-id="3acd3-112">PARAMETERS</span></span>

### <span data-ttu-id="3acd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acd3-113">-DefaultProfile</span></span>
<span data-ttu-id="3acd3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3acd3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3acd3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3acd3-115">-Name</span></span>
<span data-ttu-id="3acd3-116">Nome do namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="3acd3-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="3acd3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acd3-117">-ResourceGroupName</span></span>
<span data-ttu-id="3acd3-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3acd3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3acd3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acd3-119">CommonParameters</span></span>
<span data-ttu-id="3acd3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acd3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acd3-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3acd3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acd3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3acd3-122">INPUTS</span></span>

### <span data-ttu-id="3acd3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3acd3-123">System.String</span></span>

## <span data-ttu-id="3acd3-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3acd3-124">OUTPUTS</span></span>

### <span data-ttu-id="3acd3-125">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3acd3-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3acd3-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3acd3-126">NOTES</span></span>

## <span data-ttu-id="3acd3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3acd3-127">RELATED LINKS</span></span>
