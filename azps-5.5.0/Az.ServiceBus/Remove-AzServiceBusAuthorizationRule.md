---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116386"
---
# <span data-ttu-id="b6438-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b6438-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="b6438-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6438-102">SYNOPSIS</span></span>
<span data-ttu-id="b6438-103">Remove a regra de autorização de um namespace de Barra de Serviços ou fila ou tópico do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6438-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="b6438-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6438-104">SYNTAX</span></span>

### <span data-ttu-id="b6438-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b6438-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6438-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6438-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6438-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6438-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6438-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6438-108">DESCRIPTION</span></span>
<span data-ttu-id="b6438-109">O cmdlet **Remove-AzServiceBusAuthorizationRule** remove a regra de autorização de um namespace de Barra de Serviços ou fila ou tópico para o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6438-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="b6438-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6438-110">EXAMPLES</span></span>

### <span data-ttu-id="b6438-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6438-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="b6438-112">Remove a regra de `SBAuthoRule1` autorização do namespace `SB-Example1` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6438-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="b6438-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b6438-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="b6438-114">Remove a regra de `SBAuthoRule1` autorização da `SBQueue` fila do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6438-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="b6438-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b6438-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="b6438-116">Remove a regra de `SBAuthoRule1` autorização do tópico `SBTopic` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6438-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="b6438-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6438-117">PARAMETERS</span></span>

### <span data-ttu-id="b6438-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6438-118">-DefaultProfile</span></span>
<span data-ttu-id="b6438-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6438-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6438-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b6438-120">-Force</span></span>
<span data-ttu-id="b6438-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b6438-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6438-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6438-122">-InputObject</span></span>
<span data-ttu-id="b6438-123">Objeto ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b6438-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="b6438-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6438-124">-Name</span></span>
<span data-ttu-id="b6438-125">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b6438-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b6438-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6438-126">-Namespace</span></span>
<span data-ttu-id="b6438-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b6438-127">Namespace Name</span></span>

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

### <span data-ttu-id="b6438-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6438-128">-PassThru</span></span>
<span data-ttu-id="b6438-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b6438-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6438-130">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="b6438-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6438-131">-Fila</span><span class="sxs-lookup"><span data-stu-id="b6438-131">-Queue</span></span>
<span data-ttu-id="b6438-132">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="b6438-132">Queue Name</span></span>

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

### <span data-ttu-id="b6438-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6438-133">-ResourceGroupName</span></span>
<span data-ttu-id="b6438-134">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b6438-134">Resource Group Name</span></span>

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

### <span data-ttu-id="b6438-135">-Tópico</span><span class="sxs-lookup"><span data-stu-id="b6438-135">-Topic</span></span>
<span data-ttu-id="b6438-136">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="b6438-136">Topic Name</span></span>

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

### <span data-ttu-id="b6438-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b6438-137">-Confirm</span></span>
<span data-ttu-id="b6438-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6438-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6438-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6438-139">-WhatIf</span></span>
<span data-ttu-id="b6438-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b6438-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6438-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6438-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6438-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6438-142">CommonParameters</span></span>
<span data-ttu-id="b6438-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6438-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6438-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6438-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6438-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6438-145">INPUTS</span></span>

### <span data-ttu-id="b6438-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b6438-146">System.String</span></span>

### <span data-ttu-id="b6438-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b6438-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b6438-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6438-148">OUTPUTS</span></span>

### <span data-ttu-id="b6438-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6438-149">System.Boolean</span></span>

## <span data-ttu-id="b6438-150">Notas</span><span class="sxs-lookup"><span data-stu-id="b6438-150">NOTES</span></span>

## <span data-ttu-id="b6438-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6438-151">RELATED LINKS</span></span>
