---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609953"
---
# <span data-ttu-id="ed24b-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="ed24b-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="ed24b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed24b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed24b-103">Obtém uma descrição para o namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed24b-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed24b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed24b-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed24b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed24b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed24b-106">O cmdlet **Get-AzureRmRelayNamespace** Obtém uma descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed24b-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="ed24b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed24b-107">EXAMPLES</span></span>

### <span data-ttu-id="ed24b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed24b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="ed24b-109">Retorna uma descrição do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="ed24b-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="ed24b-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed24b-110">PARAMETERS</span></span>

### <span data-ttu-id="ed24b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed24b-111">-DefaultProfile</span></span>
<span data-ttu-id="ed24b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed24b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed24b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed24b-113">-Name</span></span>
<span data-ttu-id="ed24b-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="ed24b-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed24b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed24b-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed24b-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed24b-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed24b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed24b-117">CommonParameters</span></span>
<span data-ttu-id="ed24b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed24b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed24b-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed24b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed24b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed24b-120">INPUTS</span></span>

### <span data-ttu-id="ed24b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed24b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed24b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ed24b-122">System.String</span></span>

### <span data-ttu-id="ed24b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed24b-123">-Name</span></span>
 <span data-ttu-id="ed24b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ed24b-124">System.String</span></span>

## <span data-ttu-id="ed24b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed24b-125">OUTPUTS</span></span>

### <span data-ttu-id="ed24b-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ed24b-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ed24b-127">ProvisioningState: CreatedAt bem-sucedida: 4/12/2017 12:38:47 UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: TestNamespace-Relay1 local: marcas oeste dos EUA: {[tag1, Tag1Value]} ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 nome: TestNameSpace-Relay1 tipo: Microsoft. Relay/namespaces</span><span class="sxs-lookup"><span data-stu-id="ed24b-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="ed24b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed24b-128">NOTES</span></span>

## <span data-ttu-id="ed24b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed24b-129">RELATED LINKS</span></span>

