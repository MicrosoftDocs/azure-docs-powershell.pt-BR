---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: dad2cfc6c53352237cc677fd601d9da0b769f542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777605"
---
# <span data-ttu-id="dd28a-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dd28a-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="dd28a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd28a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd28a-103">Exclui o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="dd28a-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="dd28a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd28a-104">SYNTAX</span></span>

### <span data-ttu-id="dd28a-105">ConsumergroupPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd28a-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd28a-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd28a-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd28a-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd28a-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd28a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd28a-108">DESCRIPTION</span></span>
<span data-ttu-id="dd28a-109">O cmdlet Remove-AzEventHubConsumerGroup remove e exclui o grupo consumidor especificado do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="dd28a-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="dd28a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd28a-110">EXAMPLES</span></span>

### <span data-ttu-id="dd28a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd28a-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="dd28a-112">Exclui o \` MyConsumerGroupName do grupo \` do consumidor do MyEventHubName do hub de eventos \` \` , escopo do \` namespace mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="dd28a-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="dd28a-113">Exemplo 2,1-InputObject-using Variable</span><span class="sxs-lookup"><span data-stu-id="dd28a-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="dd28a-114">Exemplo 2,2-InputObject-usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="dd28a-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="dd28a-115">Exemplo 3,1-ResourceId usando variável</span><span class="sxs-lookup"><span data-stu-id="dd28a-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="dd28a-116">Exemplo 3,2-ResourceId usando cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="dd28a-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="dd28a-117">OS</span><span class="sxs-lookup"><span data-stu-id="dd28a-117">PARAMETERS</span></span>

### <span data-ttu-id="dd28a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd28a-118">-AsJob</span></span>
<span data-ttu-id="dd28a-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dd28a-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd28a-120">-DefaultProfile</span></span>
<span data-ttu-id="dd28a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd28a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd28a-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="dd28a-122">-EventHub</span></span>
<span data-ttu-id="dd28a-123">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="dd28a-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd28a-124">-InputObject</span></span>
<span data-ttu-id="dd28a-125">Objeto do objeto do consumidor</span><span class="sxs-lookup"><span data-stu-id="dd28a-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd28a-126">-Name</span></span>
<span data-ttu-id="dd28a-127">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="dd28a-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd28a-128">-Namespace</span></span>
<span data-ttu-id="dd28a-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="dd28a-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd28a-130">-PassThru</span></span>
<span data-ttu-id="dd28a-131">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dd28a-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd28a-132">-ResourceGroupName</span></span>
<span data-ttu-id="dd28a-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dd28a-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd28a-134">-ResourceId</span></span>
<span data-ttu-id="dd28a-135">ID do recurso de usuário do usuário</span><span class="sxs-lookup"><span data-stu-id="dd28a-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd28a-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd28a-136">-Confirm</span></span>
<span data-ttu-id="dd28a-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd28a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd28a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd28a-138">-WhatIf</span></span>
<span data-ttu-id="dd28a-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd28a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd28a-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd28a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd28a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd28a-141">CommonParameters</span></span>
<span data-ttu-id="dd28a-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd28a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd28a-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd28a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd28a-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd28a-144">INPUTS</span></span>

### <span data-ttu-id="dd28a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dd28a-145">System.String</span></span>

### <span data-ttu-id="dd28a-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="dd28a-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="dd28a-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd28a-147">OUTPUTS</span></span>

### <span data-ttu-id="dd28a-148">System. void</span><span class="sxs-lookup"><span data-stu-id="dd28a-148">System.Void</span></span>

## <span data-ttu-id="dd28a-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd28a-149">NOTES</span></span>

## <span data-ttu-id="dd28a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd28a-150">RELATED LINKS</span></span>
