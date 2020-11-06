---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427235"
---
# <span data-ttu-id="6ca91-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6ca91-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="6ca91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ca91-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca91-103">Cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="6ca91-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca91-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ca91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ca91-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca91-106">Cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="6ca91-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="6ca91-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ca91-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca91-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ca91-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="6ca91-109">Cria o grupo \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="6ca91-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6ca91-110">OS</span><span class="sxs-lookup"><span data-stu-id="6ca91-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca91-111">-DefaultProfile</span></span>
<span data-ttu-id="6ca91-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca91-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca91-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6ca91-113">-EventHub</span></span>
<span data-ttu-id="6ca91-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="6ca91-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca91-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca91-115">-Name</span></span>
<span data-ttu-id="6ca91-116">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="6ca91-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca91-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ca91-117">-Namespace</span></span>
<span data-ttu-id="6ca91-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6ca91-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca91-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ca91-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6ca91-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca91-121">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="6ca91-121">-UserMetadata</span></span>
<span data-ttu-id="6ca91-122">Metadados do usuário para o modo de consumidor</span><span class="sxs-lookup"><span data-stu-id="6ca91-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca91-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ca91-123">-Confirm</span></span>
<span data-ttu-id="6ca91-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca91-125">-WhatIf</span></span>
<span data-ttu-id="6ca91-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ca91-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca91-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ca91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca91-128">CommonParameters</span></span>
<span data-ttu-id="6ca91-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca91-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca91-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ca91-131">INPUTS</span></span>

### <span data-ttu-id="6ca91-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca91-132">System.String</span></span>

## <span data-ttu-id="6ca91-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ca91-133">OUTPUTS</span></span>

### <span data-ttu-id="6ca91-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="6ca91-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="6ca91-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ca91-135">NOTES</span></span>

## <span data-ttu-id="6ca91-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ca91-136">RELATED LINKS</span></span>
