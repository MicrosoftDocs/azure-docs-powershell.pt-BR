---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111887"
---
# <span data-ttu-id="2f808-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2f808-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="2f808-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f808-102">SYNOPSIS</span></span>
<span data-ttu-id="2f808-103">Cria um novo grupo de consumidores para o Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="2f808-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="2f808-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f808-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f808-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f808-105">DESCRIPTION</span></span>
<span data-ttu-id="2f808-106">Cria um novo grupo de consumidores para o Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="2f808-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="2f808-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f808-107">EXAMPLES</span></span>

### <span data-ttu-id="2f808-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f808-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="2f808-109">Cria o grupo de consumidor MyConsumerGroupName no Hub de Eventos MyEventHubName, com escopo para o namespace MyNamespaceName, com o grupo de recursos \` \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="2f808-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2f808-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f808-110">PARAMETERS</span></span>

### <span data-ttu-id="2f808-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f808-111">-DefaultProfile</span></span>
<span data-ttu-id="2f808-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f808-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f808-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2f808-113">-EventHub</span></span>
<span data-ttu-id="2f808-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="2f808-114">EventHub Name</span></span>

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

### <span data-ttu-id="2f808-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f808-115">-Name</span></span>
<span data-ttu-id="2f808-116">Nome do Grupo do Consumidor</span><span class="sxs-lookup"><span data-stu-id="2f808-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="2f808-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f808-117">-Namespace</span></span>
<span data-ttu-id="2f808-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2f808-118">Namespace Name</span></span>

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

### <span data-ttu-id="2f808-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f808-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f808-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2f808-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2f808-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="2f808-121">-UserMetadata</span></span>
<span data-ttu-id="2f808-122">Metadados do Usuário para ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2f808-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="2f808-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2f808-123">-Confirm</span></span>
<span data-ttu-id="2f808-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f808-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f808-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f808-125">-WhatIf</span></span>
<span data-ttu-id="2f808-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2f808-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f808-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f808-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f808-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f808-128">CommonParameters</span></span>
<span data-ttu-id="2f808-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f808-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f808-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f808-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f808-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="2f808-131">INPUTS</span></span>

### <span data-ttu-id="2f808-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2f808-132">System.String</span></span>

## <span data-ttu-id="2f808-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="2f808-133">OUTPUTS</span></span>

### <span data-ttu-id="2f808-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="2f808-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="2f808-135">Notas</span><span class="sxs-lookup"><span data-stu-id="2f808-135">NOTES</span></span>

## <span data-ttu-id="2f808-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f808-136">RELATED LINKS</span></span>
