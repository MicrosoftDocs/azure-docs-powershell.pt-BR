---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 62edcb426fe62f834b876b0dd4e2006712f81348
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599190"
---
# <span data-ttu-id="2b58b-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b58b-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2b58b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b58b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b58b-103">Cria uma nova regra de autorização para o namespace ou a fila ou tópico específico do barramento do serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2b58b-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="2b58b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b58b-104">SYNTAX</span></span>

### <span data-ttu-id="2b58b-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b58b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b58b-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b58b-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b58b-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b58b-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b58b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b58b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b58b-109">O cmdlet **New-AzServiceBusAuthorizationRule** cria uma nova regra de autorização para o namespace ou a fila ou tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2b58b-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="2b58b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b58b-110">EXAMPLES</span></span>

### <span data-ttu-id="2b58b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b58b-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2b58b-112">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para o namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2b58b-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="2b58b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2b58b-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2b58b-114">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para a fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="2b58b-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="2b58b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2b58b-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="2b58b-116">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para o tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="2b58b-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="2b58b-117">OS</span><span class="sxs-lookup"><span data-stu-id="2b58b-117">PARAMETERS</span></span>

### <span data-ttu-id="2b58b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b58b-118">-DefaultProfile</span></span>
<span data-ttu-id="2b58b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b58b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b58b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b58b-120">-Name</span></span>
<span data-ttu-id="2b58b-121">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b58b-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2b58b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b58b-122">-Namespace</span></span>
<span data-ttu-id="2b58b-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2b58b-123">Namespace Name</span></span>

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

### <span data-ttu-id="2b58b-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="2b58b-124">-Queue</span></span>
<span data-ttu-id="2b58b-125">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="2b58b-125">Queue Name</span></span>

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

### <span data-ttu-id="2b58b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b58b-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b58b-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2b58b-127">Resource Group Name</span></span>

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

### <span data-ttu-id="2b58b-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="2b58b-128">-Rights</span></span>
<span data-ttu-id="2b58b-129">Direitos, como "escutar", "enviar", "gerenciar"</span><span class="sxs-lookup"><span data-stu-id="2b58b-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="2b58b-130">-Tópico</span><span class="sxs-lookup"><span data-stu-id="2b58b-130">-Topic</span></span>
<span data-ttu-id="2b58b-131">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="2b58b-131">Topic Name</span></span>

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

### <span data-ttu-id="2b58b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b58b-132">-Confirm</span></span>
<span data-ttu-id="2b58b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b58b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b58b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b58b-134">-WhatIf</span></span>
<span data-ttu-id="2b58b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b58b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b58b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b58b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b58b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b58b-137">CommonParameters</span></span>
<span data-ttu-id="2b58b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b58b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b58b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b58b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b58b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b58b-140">INPUTS</span></span>

### <span data-ttu-id="2b58b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2b58b-141">System.String</span></span>

### <span data-ttu-id="2b58b-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="2b58b-142">System.String[]</span></span>

## <span data-ttu-id="2b58b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b58b-143">OUTPUTS</span></span>

### <span data-ttu-id="2b58b-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2b58b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2b58b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b58b-145">NOTES</span></span>

## <span data-ttu-id="2b58b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b58b-146">RELATED LINKS</span></span>
