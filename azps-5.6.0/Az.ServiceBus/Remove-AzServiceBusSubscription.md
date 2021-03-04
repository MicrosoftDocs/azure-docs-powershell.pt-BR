---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890716"
---
# <span data-ttu-id="d3e6e-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d3e6e-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="d3e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e6e-103">Remove a assinatura de um tópico do namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d3e6e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3e6e-104">SYNTAX</span></span>

### <span data-ttu-id="d3e6e-105">SubscriptionPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3e6e-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e6e-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d3e6e-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e6e-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d3e6e-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e6e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3e6e-108">DESCRIPTION</span></span>
<span data-ttu-id="d3e6e-109">O cmdlet **Remove-AzServiceBusSubscription** remove a assinatura de um tópico do namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d3e6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-110">EXAMPLES</span></span>

### <span data-ttu-id="d3e6e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3e6e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="d3e6e-112">Remove a assinatura do tópico no namespace de Barramento de `SB-TopicSubscription-Example1` `SB-Topic_exampl1` Serviço `SB-Example1` especificado.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d3e6e-113">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="d3e6e-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="d3e6e-114">Exemplo 3: InputObject - Usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="d3e6e-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="d3e6e-115">Exemplo 4: ResourceId - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="d3e6e-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="d3e6e-116">Exemplo 5: ResourceId - Usando o valor da cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="d3e6e-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="d3e6e-117">Remove a assinatura fornecida por meio ARM ID em $resourceid/cadeia de caracteres para o parâmetro -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e6e-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="d3e6e-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-118">PARAMETERS</span></span>

### <span data-ttu-id="d3e6e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e6e-119">-AsJob</span></span>
<span data-ttu-id="d3e6e-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d3e6e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e6e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e6e-121">-DefaultProfile</span></span>
<span data-ttu-id="d3e6e-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e6e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e6e-123">-InputObject</span></span>
<span data-ttu-id="d3e6e-124">Objeto de assinatura do Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="d3e6e-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d3e6e-125">-Name</span></span>
<span data-ttu-id="d3e6e-126">Nome da Assinatura</span><span class="sxs-lookup"><span data-stu-id="d3e6e-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d3e6e-127">-Namespace</span></span>
<span data-ttu-id="d3e6e-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d3e6e-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3e6e-129">-PassThru</span></span>
<span data-ttu-id="d3e6e-130">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d3e6e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e6e-131">-ResourceGroupName</span></span>
<span data-ttu-id="d3e6e-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d3e6e-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e6e-133">-ResourceId</span></span>
<span data-ttu-id="d3e6e-134">ID do Recurso de Assinatura de Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="d3e6e-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="d3e6e-135">-Topic</span></span>
<span data-ttu-id="d3e6e-136">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="d3e6e-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e6e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e6e-137">-Confirm</span></span>
<span data-ttu-id="d3e6e-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e6e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e6e-139">-WhatIf</span></span>
<span data-ttu-id="d3e6e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e6e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e6e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e6e-142">CommonParameters</span></span>
<span data-ttu-id="d3e6e-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e6e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e6e-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e6e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e6e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-145">INPUTS</span></span>

### <span data-ttu-id="d3e6e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e6e-146">System.String</span></span>

### <span data-ttu-id="d3e6e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="d3e6e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="d3e6e-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-148">OUTPUTS</span></span>

### <span data-ttu-id="d3e6e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3e6e-149">System.Boolean</span></span>

## <span data-ttu-id="d3e6e-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3e6e-150">NOTES</span></span>

## <span data-ttu-id="d3e6e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3e6e-151">RELATED LINKS</span></span>
