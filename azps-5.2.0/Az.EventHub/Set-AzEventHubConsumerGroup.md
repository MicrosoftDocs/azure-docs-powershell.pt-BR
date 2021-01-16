---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261553"
---
# <span data-ttu-id="5a2d9-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5a2d9-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5a2d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2d9-103">Atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="5a2d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a2d9-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a2d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a2d9-105">DESCRIPTION</span></span>
<span data-ttu-id="5a2d9-106">O cmdlet Set-AzEventHubConsumerGroup atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="5a2d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a2d9-107">EXAMPLES</span></span>

### <span data-ttu-id="5a2d9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a2d9-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="5a2d9-109">Define os metadados do usuário do grupo de consumidores \` MyConsumerGroupName \` para "Testing".</span><span class="sxs-lookup"><span data-stu-id="5a2d9-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="5a2d9-110">OS</span><span class="sxs-lookup"><span data-stu-id="5a2d9-110">PARAMETERS</span></span>

### <span data-ttu-id="5a2d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2d9-111">-DefaultProfile</span></span>
<span data-ttu-id="5a2d9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a2d9-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5a2d9-113">-EventHub</span></span>
<span data-ttu-id="5a2d9-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="5a2d9-114">EventHub Name</span></span>

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

### <span data-ttu-id="5a2d9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a2d9-115">-Name</span></span>
<span data-ttu-id="5a2d9-116">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="5a2d9-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="5a2d9-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a2d9-117">-Namespace</span></span>
<span data-ttu-id="5a2d9-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="5a2d9-118">Namespace Name</span></span>

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

### <span data-ttu-id="5a2d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a2d9-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5a2d9-120">Resource Group Name</span></span>

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

### <span data-ttu-id="5a2d9-121">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="5a2d9-121">-UserMetadata</span></span>
<span data-ttu-id="5a2d9-122">Metadados do usuário para o modo de consumidor</span><span class="sxs-lookup"><span data-stu-id="5a2d9-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="5a2d9-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a2d9-123">-Confirm</span></span>
<span data-ttu-id="5a2d9-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a2d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a2d9-125">-WhatIf</span></span>
<span data-ttu-id="5a2d9-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a2d9-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a2d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2d9-128">CommonParameters</span></span>
<span data-ttu-id="5a2d9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2d9-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2d9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a2d9-131">INPUTS</span></span>

### <span data-ttu-id="5a2d9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5a2d9-132">System.String</span></span>

## <span data-ttu-id="5a2d9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a2d9-133">OUTPUTS</span></span>

### <span data-ttu-id="5a2d9-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5a2d9-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5a2d9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a2d9-135">NOTES</span></span>

## <span data-ttu-id="5a2d9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a2d9-136">RELATED LINKS</span></span>
