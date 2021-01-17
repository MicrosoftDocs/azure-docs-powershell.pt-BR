---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433113"
---
# <span data-ttu-id="d514c-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d514c-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="d514c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d514c-102">SYNOPSIS</span></span>
<span data-ttu-id="d514c-103">Remove a assinatura de um tópico do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="d514c-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d514c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d514c-104">SYNTAX</span></span>

### <span data-ttu-id="d514c-105">SubscriptionPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d514c-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d514c-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d514c-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d514c-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d514c-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d514c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d514c-108">DESCRIPTION</span></span>
<span data-ttu-id="d514c-109">O cmdlet **Remove-AzServiceBusSubscription** remove a assinatura de um tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d514c-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d514c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d514c-110">EXAMPLES</span></span>

### <span data-ttu-id="d514c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d514c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="d514c-112">Remove a assinatura do `SB-TopicSubscription-Example1` tópico `SB-Topic_exampl1` no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d514c-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d514c-113">Exemplo 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="d514c-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="d514c-114">Exemplo 3: InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="d514c-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="d514c-115">Exemplo 4: ResourceId-usando a variável:</span><span class="sxs-lookup"><span data-stu-id="d514c-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="d514c-116">Exemplo 5: ResourceId-usando valor de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="d514c-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="d514c-117">Remove a assinatura fornecida por meio da ID do ARM no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d514c-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="d514c-118">OS</span><span class="sxs-lookup"><span data-stu-id="d514c-118">PARAMETERS</span></span>

### <span data-ttu-id="d514c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d514c-119">-AsJob</span></span>
<span data-ttu-id="d514c-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d514c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d514c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d514c-121">-DefaultProfile</span></span>
<span data-ttu-id="d514c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d514c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d514c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d514c-123">-InputObject</span></span>
<span data-ttu-id="d514c-124">Objeto de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="d514c-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="d514c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d514c-125">-Name</span></span>
<span data-ttu-id="d514c-126">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="d514c-126">Subscription Name</span></span>

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

### <span data-ttu-id="d514c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d514c-127">-Namespace</span></span>
<span data-ttu-id="d514c-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="d514c-128">Namespace Name</span></span>

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

### <span data-ttu-id="d514c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d514c-129">-PassThru</span></span>
<span data-ttu-id="d514c-130">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d514c-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d514c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d514c-131">-ResourceGroupName</span></span>
<span data-ttu-id="d514c-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d514c-132">The name of the resource group</span></span>

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

### <span data-ttu-id="d514c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d514c-133">-ResourceId</span></span>
<span data-ttu-id="d514c-134">ID do recurso de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="d514c-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="d514c-135">-Tópico</span><span class="sxs-lookup"><span data-stu-id="d514c-135">-Topic</span></span>
<span data-ttu-id="d514c-136">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="d514c-136">Topic Name</span></span>

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

### <span data-ttu-id="d514c-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d514c-137">-Confirm</span></span>
<span data-ttu-id="d514c-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d514c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d514c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d514c-139">-WhatIf</span></span>
<span data-ttu-id="d514c-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d514c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d514c-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d514c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d514c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d514c-142">CommonParameters</span></span>
<span data-ttu-id="d514c-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d514c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d514c-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d514c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d514c-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d514c-145">INPUTS</span></span>

### <span data-ttu-id="d514c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d514c-146">System.String</span></span>

### <span data-ttu-id="d514c-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="d514c-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="d514c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d514c-148">OUTPUTS</span></span>

### <span data-ttu-id="d514c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d514c-149">System.Boolean</span></span>

## <span data-ttu-id="d514c-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d514c-150">NOTES</span></span>

## <span data-ttu-id="d514c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d514c-151">RELATED LINKS</span></span>
