---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8f5f1ae36355f1f8d76476e5eee69f63187847ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890623"
---
# <span data-ttu-id="65c91-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65c91-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="65c91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65c91-102">SYNOPSIS</span></span>
<span data-ttu-id="65c91-103">Exclui o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="65c91-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="65c91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65c91-104">SYNTAX</span></span>

### <span data-ttu-id="65c91-105">ConsumergroupPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65c91-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65c91-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65c91-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c91-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65c91-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65c91-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65c91-108">DESCRIPTION</span></span>
<span data-ttu-id="65c91-109">O Remove-AzEventHubConsumerGroup cmdlet remove e exclui o grupo de consumidores especificado do Hub de Eventos determinado.</span><span class="sxs-lookup"><span data-stu-id="65c91-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="65c91-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65c91-110">EXAMPLES</span></span>

### <span data-ttu-id="65c91-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65c91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="65c91-112">Exclui o grupo de consumidor \` MyConsumerGroupName do Hub de Eventos MyEventHubName , com escopo para o \` \` \` \` \` namespace MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="65c91-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="65c91-113">Exemplo 2: InputObject - Usando Variável</span><span class="sxs-lookup"><span data-stu-id="65c91-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="65c91-114">Exemplo 3: InputObject - Usando a canalização</span><span class="sxs-lookup"><span data-stu-id="65c91-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="65c91-115">Exemplo 4: ResourceId usando variável</span><span class="sxs-lookup"><span data-stu-id="65c91-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="65c91-116">Exemplo 5: ResourceId Usando cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="65c91-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="65c91-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65c91-117">PARAMETERS</span></span>

### <span data-ttu-id="65c91-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65c91-118">-AsJob</span></span>
<span data-ttu-id="65c91-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="65c91-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65c91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c91-120">-DefaultProfile</span></span>
<span data-ttu-id="65c91-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65c91-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65c91-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="65c91-122">-EventHub</span></span>
<span data-ttu-id="65c91-123">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="65c91-123">EventHub Name</span></span>

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

### <span data-ttu-id="65c91-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65c91-124">-InputObject</span></span>
<span data-ttu-id="65c91-125">Objeto ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65c91-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="65c91-126">-Name</span><span class="sxs-lookup"><span data-stu-id="65c91-126">-Name</span></span>
<span data-ttu-id="65c91-127">Nome do ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65c91-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="65c91-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65c91-128">-Namespace</span></span>
<span data-ttu-id="65c91-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="65c91-129">Namespace Name</span></span>

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

### <span data-ttu-id="65c91-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65c91-130">-PassThru</span></span>
<span data-ttu-id="65c91-131">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="65c91-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="65c91-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c91-132">-ResourceGroupName</span></span>
<span data-ttu-id="65c91-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="65c91-133">Resource Group Name</span></span>

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

### <span data-ttu-id="65c91-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65c91-134">-ResourceId</span></span>
<span data-ttu-id="65c91-135">ID do Recurso ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65c91-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="65c91-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65c91-136">-Confirm</span></span>
<span data-ttu-id="65c91-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65c91-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c91-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c91-138">-WhatIf</span></span>
<span data-ttu-id="65c91-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65c91-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65c91-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65c91-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c91-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c91-141">CommonParameters</span></span>
<span data-ttu-id="65c91-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c91-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c91-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c91-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c91-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65c91-144">INPUTS</span></span>

### <span data-ttu-id="65c91-145">System.String</span><span class="sxs-lookup"><span data-stu-id="65c91-145">System.String</span></span>

### <span data-ttu-id="65c91-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="65c91-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="65c91-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65c91-147">OUTPUTS</span></span>

### <span data-ttu-id="65c91-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="65c91-148">System.Void</span></span>

## <span data-ttu-id="65c91-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="65c91-149">NOTES</span></span>

## <span data-ttu-id="65c91-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65c91-150">RELATED LINKS</span></span>
