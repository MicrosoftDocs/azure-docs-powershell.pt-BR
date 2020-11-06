---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440558"
---
# <span data-ttu-id="e9315-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e9315-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e9315-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9315-102">SYNOPSIS</span></span>
<span data-ttu-id="e9315-103">Atualiza a descrição da regra de autorização especificada para o namespace ou a fila ou o tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="e9315-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9315-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9315-104">SYNTAX</span></span>

### <span data-ttu-id="e9315-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9315-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9315-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9315-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9315-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9315-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9315-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9315-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9315-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e9315-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9315-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9315-110">DESCRIPTION</span></span>
<span data-ttu-id="e9315-111">O cmdlet **set-AzureRmServiceBusAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace ou na fila ou no tópico específico do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="e9315-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="e9315-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9315-112">EXAMPLES</span></span>

### <span data-ttu-id="e9315-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9315-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="e9315-114">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e9315-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e9315-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e9315-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="e9315-116">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` na fila `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="e9315-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="e9315-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e9315-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="e9315-118">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no tópico `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="e9315-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="e9315-119">OS</span><span class="sxs-lookup"><span data-stu-id="e9315-119">PARAMETERS</span></span>

### <span data-ttu-id="e9315-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9315-120">-Confirm</span></span>
<span data-ttu-id="e9315-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9315-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9315-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9315-122">-InputObject</span></span>
<span data-ttu-id="e9315-123">Objeto AuthorizationRule do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="e9315-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9315-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9315-124">-Name</span></span>
<span data-ttu-id="e9315-125">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e9315-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e9315-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9315-126">-Namespace</span></span>
<span data-ttu-id="e9315-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="e9315-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9315-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="e9315-128">-Queue</span></span>
<span data-ttu-id="e9315-129">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="e9315-129">Queue Name.</span></span>

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

### <span data-ttu-id="e9315-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9315-130">-ResourceGroupName</span></span>
<span data-ttu-id="e9315-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9315-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9315-132">-Direitos</span><span class="sxs-lookup"><span data-stu-id="e9315-132">-Rights</span></span>
<span data-ttu-id="e9315-133">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="e9315-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9315-134">-Tópico</span><span class="sxs-lookup"><span data-stu-id="e9315-134">-Topic</span></span>
<span data-ttu-id="e9315-135">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="e9315-135">Topic Name.</span></span>

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

### <span data-ttu-id="e9315-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9315-136">-WhatIf</span></span>
<span data-ttu-id="e9315-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9315-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9315-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9315-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9315-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9315-139">-DefaultProfile</span></span>
<span data-ttu-id="e9315-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9315-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9315-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9315-141">CommonParameters</span></span>
<span data-ttu-id="e9315-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9315-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9315-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9315-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9315-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9315-144">INPUTS</span></span>

### <span data-ttu-id="e9315-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e9315-145">System.String</span></span>
<span data-ttu-id="e9315-146">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="e9315-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="e9315-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9315-147">OUTPUTS</span></span>

### <span data-ttu-id="e9315-148">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e9315-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e9315-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9315-149">NOTES</span></span>

## <span data-ttu-id="e9315-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9315-150">RELATED LINKS</span></span>

