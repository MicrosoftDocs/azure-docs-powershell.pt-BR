---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124618"
---
# <span data-ttu-id="1af81-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1af81-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="1af81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1af81-102">SYNOPSIS</span></span>
<span data-ttu-id="1af81-103">Cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="1af81-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="1af81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1af81-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1af81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1af81-105">DESCRIPTION</span></span>
<span data-ttu-id="1af81-106">Cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="1af81-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="1af81-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1af81-107">EXAMPLES</span></span>

### <span data-ttu-id="1af81-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1af81-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="1af81-109">Cria o grupo \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="1af81-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1af81-110">OS</span><span class="sxs-lookup"><span data-stu-id="1af81-110">PARAMETERS</span></span>

### <span data-ttu-id="1af81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af81-111">-DefaultProfile</span></span>
<span data-ttu-id="1af81-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1af81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af81-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1af81-113">-EventHub</span></span>
<span data-ttu-id="1af81-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="1af81-114">EventHub Name</span></span>

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

### <span data-ttu-id="1af81-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1af81-115">-Name</span></span>
<span data-ttu-id="1af81-116">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="1af81-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="1af81-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1af81-117">-Namespace</span></span>
<span data-ttu-id="1af81-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="1af81-118">Namespace Name</span></span>

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

### <span data-ttu-id="1af81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af81-119">-ResourceGroupName</span></span>
<span data-ttu-id="1af81-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1af81-120">Resource Group Name</span></span>

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

### <span data-ttu-id="1af81-121">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="1af81-121">-UserMetadata</span></span>
<span data-ttu-id="1af81-122">Metadados do usuário para o modo de consumidor</span><span class="sxs-lookup"><span data-stu-id="1af81-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="1af81-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1af81-123">-Confirm</span></span>
<span data-ttu-id="1af81-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af81-125">-WhatIf</span></span>
<span data-ttu-id="1af81-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1af81-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af81-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1af81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af81-128">CommonParameters</span></span>
<span data-ttu-id="1af81-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af81-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af81-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af81-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1af81-131">INPUTS</span></span>

### <span data-ttu-id="1af81-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1af81-132">System.String</span></span>

## <span data-ttu-id="1af81-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1af81-133">OUTPUTS</span></span>

### <span data-ttu-id="1af81-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="1af81-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="1af81-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1af81-135">NOTES</span></span>

## <span data-ttu-id="1af81-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1af81-136">RELATED LINKS</span></span>
