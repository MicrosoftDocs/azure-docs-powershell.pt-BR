---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: 35f9342fa66b46cfd029d6440d8d82134a6822a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427237"
---
# <span data-ttu-id="ed965-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ed965-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="ed965-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed965-102">SYNOPSIS</span></span>
<span data-ttu-id="ed965-103">Obtém os detalhes de um namespace de hubs de eventos ou obtém uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed965-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed965-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed965-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed965-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed965-105">DESCRIPTION</span></span>
<span data-ttu-id="ed965-106">O cmdlet Get-AzureRmEventHubNamespace Obtém os detalhes de um namespace de hubs de eventos especificado ou uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed965-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="ed965-107">Se o nome do namespace for fornecido, os detalhes de um único namespace de hubs de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="ed965-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="ed965-108">Se o nome do namespace não for fornecido, uma lista de namespaces será retornada.</span><span class="sxs-lookup"><span data-stu-id="ed965-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="ed965-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed965-109">EXAMPLES</span></span>

### <span data-ttu-id="ed965-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed965-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ed965-111">Obtém os detalhes do namespace \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="ed965-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ed965-112">OS</span><span class="sxs-lookup"><span data-stu-id="ed965-112">PARAMETERS</span></span>

### <span data-ttu-id="ed965-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed965-113">-DefaultProfile</span></span>
<span data-ttu-id="ed965-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed965-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed965-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed965-115">-Name</span></span>
<span data-ttu-id="ed965-116">Nome do namespace do EventHub</span><span class="sxs-lookup"><span data-stu-id="ed965-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="ed965-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed965-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed965-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed965-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ed965-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed965-119">CommonParameters</span></span>
<span data-ttu-id="ed965-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed965-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed965-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed965-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed965-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed965-122">INPUTS</span></span>

### <span data-ttu-id="ed965-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ed965-123">System.String</span></span>

## <span data-ttu-id="ed965-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed965-124">OUTPUTS</span></span>

### <span data-ttu-id="ed965-125">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ed965-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ed965-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed965-126">NOTES</span></span>

## <span data-ttu-id="ed965-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed965-127">RELATED LINKS</span></span>