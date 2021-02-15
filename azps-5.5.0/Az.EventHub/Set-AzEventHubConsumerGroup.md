---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115310"
---
# <span data-ttu-id="0c5f5-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0c5f5-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="0c5f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5f5-103">Atualiza o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="0c5f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c5f5-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c5f5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c5f5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5f5-106">O Set-AzEventHubConsumerGroup cmdlet atualiza o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="0c5f5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c5f5-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5f5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c5f5-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="0c5f5-109">Define os metadados do usuário do grupo de consumidor \` MyConsumerGroupName \` como "Teste".</span><span class="sxs-lookup"><span data-stu-id="0c5f5-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="0c5f5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c5f5-110">PARAMETERS</span></span>

### <span data-ttu-id="0c5f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5f5-111">-DefaultProfile</span></span>
<span data-ttu-id="0c5f5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c5f5-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0c5f5-113">-EventHub</span></span>
<span data-ttu-id="0c5f5-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="0c5f5-114">EventHub Name</span></span>

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

### <span data-ttu-id="0c5f5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c5f5-115">-Name</span></span>
<span data-ttu-id="0c5f5-116">Nome do Grupo do Consumidor</span><span class="sxs-lookup"><span data-stu-id="0c5f5-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="0c5f5-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c5f5-117">-Namespace</span></span>
<span data-ttu-id="0c5f5-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="0c5f5-118">Namespace Name</span></span>

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

### <span data-ttu-id="0c5f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c5f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c5f5-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0c5f5-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0c5f5-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0c5f5-121">-UserMetadata</span></span>
<span data-ttu-id="0c5f5-122">Metadados do Usuário para ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0c5f5-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="0c5f5-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0c5f5-123">-Confirm</span></span>
<span data-ttu-id="0c5f5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5f5-125">-WhatIf</span></span>
<span data-ttu-id="0c5f5-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c5f5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5f5-128">CommonParameters</span></span>
<span data-ttu-id="0c5f5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5f5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5f5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c5f5-131">INPUTS</span></span>

### <span data-ttu-id="0c5f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0c5f5-132">System.String</span></span>

## <span data-ttu-id="0c5f5-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c5f5-133">OUTPUTS</span></span>

### <span data-ttu-id="0c5f5-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0c5f5-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="0c5f5-135">Notas</span><span class="sxs-lookup"><span data-stu-id="0c5f5-135">NOTES</span></span>

## <span data-ttu-id="0c5f5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c5f5-136">RELATED LINKS</span></span>
