---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901563"
---
# <span data-ttu-id="51a08-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="51a08-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="51a08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a08-102">SYNOPSIS</span></span>
<span data-ttu-id="51a08-103">Remove a regra especificada de uma determinada assinatura .</span><span class="sxs-lookup"><span data-stu-id="51a08-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="51a08-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51a08-104">SYNTAX</span></span>

### <span data-ttu-id="51a08-105">RulePropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51a08-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51a08-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="51a08-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51a08-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51a08-107">DESCRIPTION</span></span>
<span data-ttu-id="51a08-108">O cmdlet **Remove-AzServiceBusRule** remove a regra de uma assinatura de determinado tópico.</span><span class="sxs-lookup"><span data-stu-id="51a08-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="51a08-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51a08-109">EXAMPLES</span></span>

### <span data-ttu-id="51a08-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51a08-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="51a08-111">Remove a regra `SBRule` de assinatura do tópico especificado `SBSubscription` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="51a08-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="51a08-112">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="51a08-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="51a08-113">Remove a regra fornecida por meio $inputobject parâmetro -InputObject</span><span class="sxs-lookup"><span data-stu-id="51a08-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="51a08-114">Exemplo 3: InputObject - Usando a canalização:</span><span class="sxs-lookup"><span data-stu-id="51a08-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="51a08-115">Exemplo 4: ResourceId - Usando Variável</span><span class="sxs-lookup"><span data-stu-id="51a08-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="51a08-116">Exemplo 5: ResourceId - Usando o valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="51a08-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="51a08-117">Remove a regra fornecida por meio ARM ID em $resourceid/cadeia de caracteres para o parâmetro -ResourceId</span><span class="sxs-lookup"><span data-stu-id="51a08-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="51a08-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51a08-118">PARAMETERS</span></span>

### <span data-ttu-id="51a08-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51a08-119">-AsJob</span></span>
<span data-ttu-id="51a08-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51a08-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51a08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a08-121">-DefaultProfile</span></span>
<span data-ttu-id="51a08-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51a08-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a08-123">-Force</span><span class="sxs-lookup"><span data-stu-id="51a08-123">-Force</span></span>
<span data-ttu-id="51a08-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="51a08-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="51a08-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51a08-125">-InputObject</span></span>
<span data-ttu-id="51a08-126">Objeto De regra de barramento de serviço</span><span class="sxs-lookup"><span data-stu-id="51a08-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="51a08-127">-Name</span><span class="sxs-lookup"><span data-stu-id="51a08-127">-Name</span></span>
<span data-ttu-id="51a08-128">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="51a08-128">Rule Name</span></span>

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

### <span data-ttu-id="51a08-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51a08-129">-Namespace</span></span>
<span data-ttu-id="51a08-130">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="51a08-130">Namespace Name</span></span>

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

### <span data-ttu-id="51a08-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51a08-131">-PassThru</span></span>
<span data-ttu-id="51a08-132">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="51a08-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="51a08-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a08-133">-ResourceGroupName</span></span>
<span data-ttu-id="51a08-134">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="51a08-134">The name of the resource group</span></span>

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

### <span data-ttu-id="51a08-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51a08-135">-ResourceId</span></span>
<span data-ttu-id="51a08-136">ID do Recurso de Regra de Barramento de Serviço</span><span class="sxs-lookup"><span data-stu-id="51a08-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="51a08-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="51a08-137">-Subscription</span></span>
<span data-ttu-id="51a08-138">Nome da Assinatura</span><span class="sxs-lookup"><span data-stu-id="51a08-138">Subscription Name</span></span>

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

### <span data-ttu-id="51a08-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="51a08-139">-Topic</span></span>
<span data-ttu-id="51a08-140">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="51a08-140">Topic Name</span></span>

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

### <span data-ttu-id="51a08-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51a08-141">-Confirm</span></span>
<span data-ttu-id="51a08-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a08-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a08-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a08-143">-WhatIf</span></span>
<span data-ttu-id="51a08-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51a08-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a08-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51a08-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a08-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a08-146">CommonParameters</span></span>
<span data-ttu-id="51a08-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a08-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a08-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a08-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a08-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51a08-149">INPUTS</span></span>

### <span data-ttu-id="51a08-150">System.String</span><span class="sxs-lookup"><span data-stu-id="51a08-150">System.String</span></span>

### <span data-ttu-id="51a08-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="51a08-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="51a08-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51a08-152">OUTPUTS</span></span>

### <span data-ttu-id="51a08-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51a08-153">System.Boolean</span></span>

## <span data-ttu-id="51a08-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="51a08-154">NOTES</span></span>

## <span data-ttu-id="51a08-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51a08-155">RELATED LINKS</span></span>
