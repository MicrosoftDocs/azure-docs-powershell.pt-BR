---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117133"
---
# <span data-ttu-id="6e2a1-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e2a1-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="6e2a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2a1-103">Cria uma nova regra de autorização para o Barramento de Serviço especificado, dado Namespace ou Fila ou Tópico.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="6e2a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e2a1-104">SYNTAX</span></span>

### <span data-ttu-id="6e2a1-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e2a1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2a1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e2a1-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e2a1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e2a1-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e2a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e2a1-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2a1-109">O cmdlet **New-AzServiceBusAuthorizationRule** cria uma nova regra de autorização para o namespace ou fila ou tópico do Service Bus especificado.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="6e2a1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e2a1-110">EXAMPLES</span></span>

### <span data-ttu-id="6e2a1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e2a1-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6e2a1-112">Cria `AuthoRule1` com os **direitos** ouvir **e enviar** para o namespace. `SB-Example1`</span><span class="sxs-lookup"><span data-stu-id="6e2a1-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6e2a1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e2a1-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6e2a1-114">Cria `AuthoRule1` com os **direitos** ouvir **e** enviar para a `SBQueue` fila.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="6e2a1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6e2a1-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="6e2a1-116">Cria `AuthoRule1` com Os **direitos** de **Ouvir e** Enviar para o `SBTopic` tópico.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="6e2a1-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e2a1-117">PARAMETERS</span></span>

### <span data-ttu-id="6e2a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2a1-118">-DefaultProfile</span></span>
<span data-ttu-id="6e2a1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2a1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e2a1-120">-Name</span></span>
<span data-ttu-id="6e2a1-121">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e2a1-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6e2a1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e2a1-122">-Namespace</span></span>
<span data-ttu-id="6e2a1-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6e2a1-123">Namespace Name</span></span>

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

### <span data-ttu-id="6e2a1-124">-Fila</span><span class="sxs-lookup"><span data-stu-id="6e2a1-124">-Queue</span></span>
<span data-ttu-id="6e2a1-125">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="6e2a1-125">Queue Name</span></span>

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

### <span data-ttu-id="6e2a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e2a1-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6e2a1-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6e2a1-128">-Direitos</span><span class="sxs-lookup"><span data-stu-id="6e2a1-128">-Rights</span></span>
<span data-ttu-id="6e2a1-129">Direitos, por exemplo, "Ouvir","Enviar","Gerenciar"</span><span class="sxs-lookup"><span data-stu-id="6e2a1-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="6e2a1-130">-Tópico</span><span class="sxs-lookup"><span data-stu-id="6e2a1-130">-Topic</span></span>
<span data-ttu-id="6e2a1-131">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="6e2a1-131">Topic Name</span></span>

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

### <span data-ttu-id="6e2a1-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6e2a1-132">-Confirm</span></span>
<span data-ttu-id="6e2a1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e2a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2a1-134">-WhatIf</span></span>
<span data-ttu-id="6e2a1-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2a1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2a1-137">CommonParameters</span></span>
<span data-ttu-id="6e2a1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2a1-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2a1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2a1-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6e2a1-140">INPUTS</span></span>

### <span data-ttu-id="6e2a1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6e2a1-141">System.String</span></span>

### <span data-ttu-id="6e2a1-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6e2a1-142">System.String[]</span></span>

## <span data-ttu-id="6e2a1-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6e2a1-143">OUTPUTS</span></span>

### <span data-ttu-id="6e2a1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6e2a1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6e2a1-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6e2a1-145">NOTES</span></span>

## <span data-ttu-id="6e2a1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e2a1-146">RELATED LINKS</span></span>
