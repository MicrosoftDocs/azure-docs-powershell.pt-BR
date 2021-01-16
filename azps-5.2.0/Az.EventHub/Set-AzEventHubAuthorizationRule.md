---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261556"
---
# <span data-ttu-id="c64ac-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c64ac-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c64ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c64ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c64ac-103">Atualiza a regra de autorização especificada em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="c64ac-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="c64ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c64ac-104">SYNTAX</span></span>

### <span data-ttu-id="c64ac-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c64ac-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c64ac-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c64ac-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c64ac-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c64ac-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c64ac-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c64ac-108">DESCRIPTION</span></span>
<span data-ttu-id="c64ac-109">O cmdlet Set-AzEventHubAuthorizationRule atualiza a regra de autorização especificada em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="c64ac-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="c64ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c64ac-110">EXAMPLES</span></span>

### <span data-ttu-id="c64ac-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c64ac-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="c64ac-112">Atualiza a regra de autorização \` MyAuthRuleName \` para conceder direitos de gerenciamento ao Hub de eventos \` MyEventHubName \` , delimitado pelo namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="c64ac-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c64ac-113">OS</span><span class="sxs-lookup"><span data-stu-id="c64ac-113">PARAMETERS</span></span>

### <span data-ttu-id="c64ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64ac-114">-DefaultProfile</span></span>
<span data-ttu-id="c64ac-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c64ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c64ac-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c64ac-116">-EventHub</span></span>
<span data-ttu-id="c64ac-117">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="c64ac-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ac-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c64ac-118">-InputObject</span></span>
<span data-ttu-id="c64ac-119">Objeto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c64ac-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c64ac-120">-Name</span></span>
<span data-ttu-id="c64ac-121">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c64ac-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c64ac-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c64ac-122">-Namespace</span></span>
<span data-ttu-id="c64ac-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c64ac-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="c64ac-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c64ac-125">Resource Group Name</span></span>

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

### <span data-ttu-id="c64ac-126">-Direitos</span><span class="sxs-lookup"><span data-stu-id="c64ac-126">-Rights</span></span>
<span data-ttu-id="c64ac-127">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="c64ac-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64ac-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c64ac-128">-Confirm</span></span>
<span data-ttu-id="c64ac-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c64ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c64ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c64ac-130">-WhatIf</span></span>
<span data-ttu-id="c64ac-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c64ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c64ac-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c64ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c64ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64ac-133">CommonParameters</span></span>
<span data-ttu-id="c64ac-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64ac-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64ac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64ac-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c64ac-136">INPUTS</span></span>

### <span data-ttu-id="c64ac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c64ac-137">System.String</span></span>

### <span data-ttu-id="c64ac-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c64ac-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="c64ac-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="c64ac-139">System.String[]</span></span>

## <span data-ttu-id="c64ac-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c64ac-140">OUTPUTS</span></span>

### <span data-ttu-id="c64ac-141">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c64ac-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c64ac-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c64ac-142">NOTES</span></span>

## <span data-ttu-id="c64ac-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c64ac-143">RELATED LINKS</span></span>
