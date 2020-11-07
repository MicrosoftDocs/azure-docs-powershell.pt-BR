---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: d1cb165b537815227a15223a1b646c38892005bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773229"
---
# <span data-ttu-id="f8384-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8384-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f8384-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8384-102">SYNOPSIS</span></span>
<span data-ttu-id="f8384-103">Remove a regra de autorização de um namespace ou uma fila ou tópico de barramento do serviço do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f8384-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="f8384-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8384-104">SYNTAX</span></span>

### <span data-ttu-id="f8384-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8384-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8384-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8384-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8384-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8384-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8384-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8384-108">DESCRIPTION</span></span>
<span data-ttu-id="f8384-109">O cmdlet **Remove-AzServiceBusAuthorizationRule** remove a regra de autorização de um namespace ou uma fila ou tópico de barramento do serviço para o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f8384-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="f8384-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8384-110">EXAMPLES</span></span>

### <span data-ttu-id="f8384-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8384-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f8384-112">Remove a regra `SBAuthoRule1` de autorização do namespace `SB-Example1` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f8384-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="f8384-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f8384-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f8384-114">Remove a regra `SBAuthoRule1` de autorização da fila `SBQueue` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f8384-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="f8384-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f8384-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f8384-116">Remove a regra `SBAuthoRule1` de autorização do tópico `SBTopic` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f8384-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="f8384-117">OS</span><span class="sxs-lookup"><span data-stu-id="f8384-117">PARAMETERS</span></span>

### <span data-ttu-id="f8384-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8384-118">-DefaultProfile</span></span>
<span data-ttu-id="f8384-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8384-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8384-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f8384-120">-Force</span></span>
<span data-ttu-id="f8384-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f8384-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f8384-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8384-122">-InputObject</span></span>
<span data-ttu-id="f8384-123">Objeto AuthorizationRule do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f8384-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8384-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8384-124">-Name</span></span>
<span data-ttu-id="f8384-125">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8384-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8384-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8384-126">-Namespace</span></span>
<span data-ttu-id="f8384-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="f8384-127">Namespace Name</span></span>

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

### <span data-ttu-id="f8384-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8384-128">-PassThru</span></span>
<span data-ttu-id="f8384-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f8384-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8384-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f8384-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8384-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="f8384-131">-Queue</span></span>
<span data-ttu-id="f8384-132">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="f8384-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8384-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8384-133">-ResourceGroupName</span></span>
<span data-ttu-id="f8384-134">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f8384-134">Resource Group Name</span></span>

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

### <span data-ttu-id="f8384-135">-Tópico</span><span class="sxs-lookup"><span data-stu-id="f8384-135">-Topic</span></span>
<span data-ttu-id="f8384-136">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="f8384-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8384-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8384-137">-Confirm</span></span>
<span data-ttu-id="f8384-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8384-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8384-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8384-139">-WhatIf</span></span>
<span data-ttu-id="f8384-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8384-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8384-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8384-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8384-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8384-142">CommonParameters</span></span>
<span data-ttu-id="f8384-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8384-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8384-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8384-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8384-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8384-145">INPUTS</span></span>

### <span data-ttu-id="f8384-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f8384-146">System.String</span></span>

### <span data-ttu-id="f8384-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8384-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f8384-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8384-148">OUTPUTS</span></span>

### <span data-ttu-id="f8384-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8384-149">System.Boolean</span></span>

## <span data-ttu-id="f8384-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8384-150">NOTES</span></span>

## <span data-ttu-id="f8384-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8384-151">RELATED LINKS</span></span>
