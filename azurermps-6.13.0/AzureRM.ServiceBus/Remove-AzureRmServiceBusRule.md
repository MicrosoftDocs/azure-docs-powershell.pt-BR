---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430862"
---
# <span data-ttu-id="da7dd-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="da7dd-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="da7dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="da7dd-103">Remove a regra speficied de uma determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="da7dd-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da7dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da7dd-104">SYNTAX</span></span>

### <span data-ttu-id="da7dd-105">RulePropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="da7dd-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da7dd-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="da7dd-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da7dd-107">DESCRIPTION</span></span>
<span data-ttu-id="da7dd-108">O cmdlet **Remove-AzureRmServiceBusRule** remove a regra de uma assinatura de determinado tópico.</span><span class="sxs-lookup"><span data-stu-id="da7dd-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="da7dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da7dd-109">EXAMPLES</span></span>

### <span data-ttu-id="da7dd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da7dd-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="da7dd-111">Remove a regra `SBRule` de assinatura `SBSubscription` do tópico especificado `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="da7dd-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="da7dd-112">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="da7dd-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="da7dd-113">Remove a regra fornecida por meio do $inputobject para o parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="da7dd-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="da7dd-114">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="da7dd-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="da7dd-115">Exemplo 3,1-ResourceId-usando variável</span><span class="sxs-lookup"><span data-stu-id="da7dd-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="da7dd-116">Exemplo 3,1-ResourceId-usando o valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="da7dd-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="da7dd-117">Remove a regra fornecida por meio da ID do ARM no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da7dd-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="da7dd-118">OS</span><span class="sxs-lookup"><span data-stu-id="da7dd-118">PARAMETERS</span></span>

### <span data-ttu-id="da7dd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da7dd-119">-AsJob</span></span>
<span data-ttu-id="da7dd-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="da7dd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da7dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7dd-121">-DefaultProfile</span></span>
<span data-ttu-id="da7dd-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da7dd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="da7dd-123">-Force</span></span>
<span data-ttu-id="da7dd-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="da7dd-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="da7dd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da7dd-125">-InputObject</span></span>
<span data-ttu-id="da7dd-126">Objeto regra do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="da7dd-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="da7dd-127">-Name</span></span>
<span data-ttu-id="da7dd-128">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="da7dd-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="da7dd-129">-Namespace</span></span>
<span data-ttu-id="da7dd-130">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="da7dd-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da7dd-131">-PassThru</span></span>
<span data-ttu-id="da7dd-132">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="da7dd-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="da7dd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7dd-133">-ResourceGroupName</span></span>
<span data-ttu-id="da7dd-134">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="da7dd-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da7dd-135">-ResourceId</span></span>
<span data-ttu-id="da7dd-136">ID do recurso regra de barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="da7dd-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-137">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="da7dd-137">-Subscription</span></span>
<span data-ttu-id="da7dd-138">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="da7dd-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-139">-Tópico</span><span class="sxs-lookup"><span data-stu-id="da7dd-139">-Topic</span></span>
<span data-ttu-id="da7dd-140">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="da7dd-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7dd-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da7dd-141">-Confirm</span></span>
<span data-ttu-id="da7dd-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7dd-143">-WhatIf</span></span>
<span data-ttu-id="da7dd-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da7dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da7dd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da7dd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7dd-146">CommonParameters</span></span>
<span data-ttu-id="da7dd-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7dd-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7dd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7dd-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da7dd-149">INPUTS</span></span>

### <span data-ttu-id="da7dd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="da7dd-150">System.String</span></span>

### <span data-ttu-id="da7dd-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="da7dd-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="da7dd-152">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da7dd-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="da7dd-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da7dd-153">OUTPUTS</span></span>

### <span data-ttu-id="da7dd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da7dd-154">System.Boolean</span></span>

## <span data-ttu-id="da7dd-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da7dd-155">NOTES</span></span>

## <span data-ttu-id="da7dd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da7dd-156">RELATED LINKS</span></span>
