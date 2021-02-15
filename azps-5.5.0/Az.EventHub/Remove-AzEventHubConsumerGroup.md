---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113826"
---
# <span data-ttu-id="5fcf0-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5fcf0-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5fcf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcf0-103">Exclui o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="5fcf0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fcf0-104">SYNTAX</span></span>

### <span data-ttu-id="5fcf0-105">ConsumergroupPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5fcf0-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcf0-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fcf0-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fcf0-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fcf0-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fcf0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fcf0-108">DESCRIPTION</span></span>
<span data-ttu-id="5fcf0-109">O Remove-AzEventHubConsumerGroup cmdlet remove e exclui o grupo de consumidores especificado do Hub de Eventos determinado.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="5fcf0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5fcf0-110">EXAMPLES</span></span>

### <span data-ttu-id="5fcf0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fcf0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="5fcf0-112">Exclui o grupo de consumidor \` MyConsumerGroupName do Hub de Eventos MyEventHubName, com escopo para o \` \` \` \` \` namespace MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="5fcf0-113">Exemplo 2: InputObject - Usando Variável</span><span class="sxs-lookup"><span data-stu-id="5fcf0-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="5fcf0-114">Exemplo 3: InputObject - Usando a piping</span><span class="sxs-lookup"><span data-stu-id="5fcf0-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="5fcf0-115">Exemplo 4: ResourceId using Variable</span><span class="sxs-lookup"><span data-stu-id="5fcf0-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="5fcf0-116">Exemplo 5: ResourceId Using string</span><span class="sxs-lookup"><span data-stu-id="5fcf0-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="5fcf0-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fcf0-117">PARAMETERS</span></span>

### <span data-ttu-id="5fcf0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fcf0-118">-AsJob</span></span>
<span data-ttu-id="5fcf0-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fcf0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fcf0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcf0-120">-DefaultProfile</span></span>
<span data-ttu-id="5fcf0-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fcf0-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5fcf0-122">-EventHub</span></span>
<span data-ttu-id="5fcf0-123">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="5fcf0-123">EventHub Name</span></span>

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

### <span data-ttu-id="5fcf0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fcf0-124">-InputObject</span></span>
<span data-ttu-id="5fcf0-125">Objeto ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5fcf0-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="5fcf0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fcf0-126">-Name</span></span>
<span data-ttu-id="5fcf0-127">Nome do Grupo do Consumidor</span><span class="sxs-lookup"><span data-stu-id="5fcf0-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="5fcf0-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fcf0-128">-Namespace</span></span>
<span data-ttu-id="5fcf0-129">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="5fcf0-129">Namespace Name</span></span>

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

### <span data-ttu-id="5fcf0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fcf0-130">-PassThru</span></span>
<span data-ttu-id="5fcf0-131">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5fcf0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcf0-132">-ResourceGroupName</span></span>
<span data-ttu-id="5fcf0-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5fcf0-133">Resource Group Name</span></span>

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

### <span data-ttu-id="5fcf0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fcf0-134">-ResourceId</span></span>
<span data-ttu-id="5fcf0-135">ID do Recurso ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5fcf0-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="5fcf0-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5fcf0-136">-Confirm</span></span>
<span data-ttu-id="5fcf0-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fcf0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcf0-138">-WhatIf</span></span>
<span data-ttu-id="5fcf0-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcf0-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fcf0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcf0-141">CommonParameters</span></span>
<span data-ttu-id="5fcf0-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcf0-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcf0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcf0-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="5fcf0-144">INPUTS</span></span>

### <span data-ttu-id="5fcf0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5fcf0-145">System.String</span></span>

### <span data-ttu-id="5fcf0-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5fcf0-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5fcf0-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="5fcf0-147">OUTPUTS</span></span>

### <span data-ttu-id="5fcf0-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="5fcf0-148">System.Void</span></span>

## <span data-ttu-id="5fcf0-149">Notas</span><span class="sxs-lookup"><span data-stu-id="5fcf0-149">NOTES</span></span>

## <span data-ttu-id="5fcf0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fcf0-150">RELATED LINKS</span></span>
