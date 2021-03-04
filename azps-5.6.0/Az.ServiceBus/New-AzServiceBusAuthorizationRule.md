---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 08560730438fe5bca85a78e8a7f75f427c07de0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888793"
---
# <span data-ttu-id="983d7-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="983d7-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="983d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="983d7-102">SYNOPSIS</span></span>
<span data-ttu-id="983d7-103">Cria uma nova regra de autorização para o Barramento de Serviço especificado dado Namespace ou Queue ou Topic.</span><span class="sxs-lookup"><span data-stu-id="983d7-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="983d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="983d7-104">SYNTAX</span></span>

### <span data-ttu-id="983d7-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="983d7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="983d7-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="983d7-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="983d7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="983d7-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="983d7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="983d7-108">DESCRIPTION</span></span>
<span data-ttu-id="983d7-109">O cmdlet **New-AzServiceBusAuthorizationRule** cria uma nova regra de autorização para o namespace de Barramento de Serviço especificado ou fila ou tópico.</span><span class="sxs-lookup"><span data-stu-id="983d7-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="983d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="983d7-110">EXAMPLES</span></span>

### <span data-ttu-id="983d7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="983d7-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="983d7-112">Cria `AuthoRule1` com **Ouvir** e **Enviar direitos** para o namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="983d7-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="983d7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="983d7-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="983d7-114">Cria `AuthoRule1` com Os direitos **de** Escuta **e** Envio para a fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="983d7-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="983d7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="983d7-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="983d7-116">Cria `AuthoRule1` com Os **direitos** de Escuta **e** Envio para o tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="983d7-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="983d7-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="983d7-117">PARAMETERS</span></span>

### <span data-ttu-id="983d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983d7-118">-DefaultProfile</span></span>
<span data-ttu-id="983d7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="983d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="983d7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="983d7-120">-Name</span></span>
<span data-ttu-id="983d7-121">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="983d7-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="983d7-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="983d7-122">-Namespace</span></span>
<span data-ttu-id="983d7-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="983d7-123">Namespace Name</span></span>

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

### <span data-ttu-id="983d7-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="983d7-124">-Queue</span></span>
<span data-ttu-id="983d7-125">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="983d7-125">Queue Name</span></span>

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

### <span data-ttu-id="983d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="983d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="983d7-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="983d7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="983d7-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="983d7-128">-Rights</span></span>
<span data-ttu-id="983d7-129">Direitos, por exemplo, "Listen","Send","Manage"</span><span class="sxs-lookup"><span data-stu-id="983d7-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983d7-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="983d7-130">-Topic</span></span>
<span data-ttu-id="983d7-131">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="983d7-131">Topic Name</span></span>

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

### <span data-ttu-id="983d7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="983d7-132">-Confirm</span></span>
<span data-ttu-id="983d7-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="983d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="983d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="983d7-134">-WhatIf</span></span>
<span data-ttu-id="983d7-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="983d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="983d7-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="983d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="983d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983d7-137">CommonParameters</span></span>
<span data-ttu-id="983d7-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983d7-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983d7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983d7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="983d7-140">INPUTS</span></span>

### <span data-ttu-id="983d7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="983d7-141">System.String</span></span>

### <span data-ttu-id="983d7-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="983d7-142">System.String[]</span></span>

## <span data-ttu-id="983d7-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="983d7-143">OUTPUTS</span></span>

### <span data-ttu-id="983d7-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="983d7-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="983d7-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="983d7-145">NOTES</span></span>

## <span data-ttu-id="983d7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="983d7-146">RELATED LINKS</span></span>
