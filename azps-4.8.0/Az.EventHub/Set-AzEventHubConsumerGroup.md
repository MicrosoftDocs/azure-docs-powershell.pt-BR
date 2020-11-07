---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947770"
---
# <span data-ttu-id="17d4f-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="17d4f-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="17d4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="17d4f-103">Atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="17d4f-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="17d4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17d4f-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17d4f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="17d4f-106">O cmdlet Set-AzEventHubConsumerGroup atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="17d4f-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="17d4f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="17d4f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17d4f-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="17d4f-109">Define os metadados do usuário do grupo de consumidores \` MyConsumerGroupName \` para "Testing".</span><span class="sxs-lookup"><span data-stu-id="17d4f-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="17d4f-110">OS</span><span class="sxs-lookup"><span data-stu-id="17d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="17d4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d4f-111">-DefaultProfile</span></span>
<span data-ttu-id="17d4f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17d4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17d4f-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="17d4f-113">-EventHub</span></span>
<span data-ttu-id="17d4f-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="17d4f-114">EventHub Name</span></span>

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

### <span data-ttu-id="17d4f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="17d4f-115">-Name</span></span>
<span data-ttu-id="17d4f-116">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="17d4f-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="17d4f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="17d4f-117">-Namespace</span></span>
<span data-ttu-id="17d4f-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="17d4f-118">Namespace Name</span></span>

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

### <span data-ttu-id="17d4f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d4f-119">-ResourceGroupName</span></span>
<span data-ttu-id="17d4f-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="17d4f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="17d4f-121">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="17d4f-121">-UserMetadata</span></span>
<span data-ttu-id="17d4f-122">Metadados do usuário para o modo de consumidor</span><span class="sxs-lookup"><span data-stu-id="17d4f-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="17d4f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17d4f-123">-Confirm</span></span>
<span data-ttu-id="17d4f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17d4f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17d4f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d4f-125">-WhatIf</span></span>
<span data-ttu-id="17d4f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17d4f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d4f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17d4f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17d4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d4f-128">CommonParameters</span></span>
<span data-ttu-id="17d4f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17d4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d4f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d4f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d4f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17d4f-131">INPUTS</span></span>

### <span data-ttu-id="17d4f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17d4f-132">System.String</span></span>

## <span data-ttu-id="17d4f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17d4f-133">OUTPUTS</span></span>

### <span data-ttu-id="17d4f-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="17d4f-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="17d4f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17d4f-135">NOTES</span></span>

## <span data-ttu-id="17d4f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17d4f-136">RELATED LINKS</span></span>
