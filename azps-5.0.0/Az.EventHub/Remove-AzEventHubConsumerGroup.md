---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125017"
---
# <span data-ttu-id="c619b-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c619b-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="c619b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c619b-102">SYNOPSIS</span></span>
<span data-ttu-id="c619b-103">Exclui o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="c619b-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="c619b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c619b-104">SYNTAX</span></span>

### <span data-ttu-id="c619b-105">ConsumergroupPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c619b-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c619b-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c619b-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c619b-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c619b-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c619b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c619b-108">DESCRIPTION</span></span>
<span data-ttu-id="c619b-109">O cmdlet Remove-AzEventHubConsumerGroup remove e exclui o grupo consumidor especificado do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="c619b-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="c619b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c619b-110">EXAMPLES</span></span>

### <span data-ttu-id="c619b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c619b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="c619b-112">Exclui o \` MyConsumerGroupName do grupo \` do consumidor do MyEventHubName do hub de eventos \` \` , escopo do \` namespace mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="c619b-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="c619b-113">Exemplo 2: InputObject-using Variable</span><span class="sxs-lookup"><span data-stu-id="c619b-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="c619b-114">Exemplo 3: InputObject-usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="c619b-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="c619b-115">Exemplo 4: ResourceId usando variável</span><span class="sxs-lookup"><span data-stu-id="c619b-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="c619b-116">Exemplo 5: ResourceId usando String</span><span class="sxs-lookup"><span data-stu-id="c619b-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="c619b-117">OS</span><span class="sxs-lookup"><span data-stu-id="c619b-117">PARAMETERS</span></span>

### <span data-ttu-id="c619b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c619b-118">-AsJob</span></span>
<span data-ttu-id="c619b-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c619b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c619b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c619b-120">-DefaultProfile</span></span>
<span data-ttu-id="c619b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c619b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c619b-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c619b-122">-EventHub</span></span>
<span data-ttu-id="c619b-123">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="c619b-123">EventHub Name</span></span>

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

### <span data-ttu-id="c619b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c619b-124">-InputObject</span></span>
<span data-ttu-id="c619b-125">Objeto do objeto do consumidor</span><span class="sxs-lookup"><span data-stu-id="c619b-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="c619b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c619b-126">-Name</span></span>
<span data-ttu-id="c619b-127">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="c619b-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="c619b-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c619b-128">-Namespace</span></span>
<span data-ttu-id="c619b-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c619b-129">Namespace Name</span></span>

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

### <span data-ttu-id="c619b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c619b-130">-PassThru</span></span>
<span data-ttu-id="c619b-131">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c619b-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c619b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c619b-132">-ResourceGroupName</span></span>
<span data-ttu-id="c619b-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c619b-133">Resource Group Name</span></span>

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

### <span data-ttu-id="c619b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c619b-134">-ResourceId</span></span>
<span data-ttu-id="c619b-135">ID do recurso de usuário do usuário</span><span class="sxs-lookup"><span data-stu-id="c619b-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="c619b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c619b-136">-Confirm</span></span>
<span data-ttu-id="c619b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c619b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c619b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c619b-138">-WhatIf</span></span>
<span data-ttu-id="c619b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c619b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c619b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c619b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c619b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c619b-141">CommonParameters</span></span>
<span data-ttu-id="c619b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c619b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c619b-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c619b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c619b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c619b-144">INPUTS</span></span>

### <span data-ttu-id="c619b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c619b-145">System.String</span></span>

### <span data-ttu-id="c619b-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="c619b-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="c619b-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c619b-147">OUTPUTS</span></span>

### <span data-ttu-id="c619b-148">System. void</span><span class="sxs-lookup"><span data-stu-id="c619b-148">System.Void</span></span>

## <span data-ttu-id="c619b-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c619b-149">NOTES</span></span>

## <span data-ttu-id="c619b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c619b-150">RELATED LINKS</span></span>
