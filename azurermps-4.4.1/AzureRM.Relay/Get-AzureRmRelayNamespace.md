---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429140"
---
# <span data-ttu-id="5f641-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="5f641-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="5f641-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f641-102">SYNOPSIS</span></span>
<span data-ttu-id="5f641-103">Obtém uma descrição para o namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f641-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f641-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f641-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f641-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f641-105">DESCRIPTION</span></span>
<span data-ttu-id="5f641-106">O cmdlet **Get-AzureRmRelayNamespace** Obtém uma descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f641-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="5f641-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f641-107">EXAMPLES</span></span>

### <span data-ttu-id="5f641-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f641-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="5f641-109">Retorna uma descrição do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="5f641-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="5f641-110">OS</span><span class="sxs-lookup"><span data-stu-id="5f641-110">PARAMETERS</span></span>

### <span data-ttu-id="5f641-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f641-111">-Name</span></span>
<span data-ttu-id="5f641-112">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="5f641-112">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f641-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f641-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f641-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f641-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="5f641-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f641-115">-DefaultProfile</span></span>
<span data-ttu-id="5f641-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f641-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f641-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f641-117">CommonParameters</span></span>
<span data-ttu-id="5f641-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f641-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f641-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f641-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f641-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f641-120">INPUTS</span></span>

### <span data-ttu-id="5f641-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f641-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f641-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5f641-122">System.String</span></span>

### <span data-ttu-id="5f641-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f641-123">-Name</span></span>
 <span data-ttu-id="5f641-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5f641-124">System.String</span></span>

## <span data-ttu-id="5f641-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f641-125">OUTPUTS</span></span>

### <span data-ttu-id="5f641-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5f641-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5f641-127">ProvisioningState: CreatedAt bem-sucedida: 4/12/2017 12:38:47 UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: TestNamespace-Relay1 local: marcas oeste dos EUA: {[tag1, Tag1Value]} ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 nome: TestNameSpace-Relay1 tipo: Microsoft. Relay/namespaces</span><span class="sxs-lookup"><span data-stu-id="5f641-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="5f641-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f641-128">NOTES</span></span>

## <span data-ttu-id="5f641-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f641-129">RELATED LINKS</span></span>

