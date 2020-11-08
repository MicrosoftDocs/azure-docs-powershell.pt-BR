---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115683"
---
# <span data-ttu-id="ea7cc-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea7cc-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ea7cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7cc-103">Cria uma nova regra de autorização para o namespace ou a fila ou tópico específico do barramento do serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="ea7cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea7cc-104">SYNTAX</span></span>

### <span data-ttu-id="ea7cc-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea7cc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7cc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea7cc-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea7cc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea7cc-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea7cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea7cc-108">DESCRIPTION</span></span>
<span data-ttu-id="ea7cc-109">O cmdlet **New-AzServiceBusAuthorizationRule** cria uma nova regra de autorização para o namespace ou a fila ou tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ea7cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea7cc-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea7cc-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ea7cc-112">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para o namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ea7cc-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ea7cc-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea7cc-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ea7cc-114">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para a fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="ea7cc-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="ea7cc-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea7cc-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ea7cc-116">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para o tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="ea7cc-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="ea7cc-117">OS</span><span class="sxs-lookup"><span data-stu-id="ea7cc-117">PARAMETERS</span></span>

### <span data-ttu-id="ea7cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7cc-118">-DefaultProfile</span></span>
<span data-ttu-id="ea7cc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea7cc-120">-Name</span></span>
<span data-ttu-id="ea7cc-121">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea7cc-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ea7cc-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea7cc-122">-Namespace</span></span>
<span data-ttu-id="ea7cc-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="ea7cc-123">Namespace Name</span></span>

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

### <span data-ttu-id="ea7cc-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="ea7cc-124">-Queue</span></span>
<span data-ttu-id="ea7cc-125">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="ea7cc-125">Queue Name</span></span>

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

### <span data-ttu-id="ea7cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea7cc-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ea7cc-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ea7cc-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="ea7cc-128">-Rights</span></span>
<span data-ttu-id="ea7cc-129">Direitos, como "escutar", "enviar", "gerenciar"</span><span class="sxs-lookup"><span data-stu-id="ea7cc-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="ea7cc-130">-Tópico</span><span class="sxs-lookup"><span data-stu-id="ea7cc-130">-Topic</span></span>
<span data-ttu-id="ea7cc-131">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="ea7cc-131">Topic Name</span></span>

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

### <span data-ttu-id="ea7cc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea7cc-132">-Confirm</span></span>
<span data-ttu-id="ea7cc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7cc-134">-WhatIf</span></span>
<span data-ttu-id="ea7cc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7cc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7cc-137">CommonParameters</span></span>
<span data-ttu-id="ea7cc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7cc-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7cc-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7cc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea7cc-140">INPUTS</span></span>

### <span data-ttu-id="ea7cc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea7cc-141">System.String</span></span>

### <span data-ttu-id="ea7cc-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="ea7cc-142">System.String[]</span></span>

## <span data-ttu-id="ea7cc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea7cc-143">OUTPUTS</span></span>

### <span data-ttu-id="ea7cc-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ea7cc-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ea7cc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea7cc-145">NOTES</span></span>

## <span data-ttu-id="ea7cc-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea7cc-146">RELATED LINKS</span></span>
