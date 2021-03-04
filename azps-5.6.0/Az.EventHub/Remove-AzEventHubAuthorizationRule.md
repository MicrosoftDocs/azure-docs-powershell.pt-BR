---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890630"
---
# <span data-ttu-id="9a0a7-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9a0a7-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="9a0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0a7-103">Remove a regra de autorização do Hub de Eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="9a0a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9a0a7-104">SYNTAX</span></span>

### <span data-ttu-id="9a0a7-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a0a7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a0a7-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a0a7-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a0a7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9a0a7-107">DESCRIPTION</span></span>
<span data-ttu-id="9a0a7-108">O Remove-AzEventHubAuthorizationRule cmdlet remove e exclui a regra de autorização especificada do Hub de Eventos determinado.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="9a0a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-109">EXAMPLES</span></span>

### <span data-ttu-id="9a0a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a0a7-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="9a0a7-111">Remove a regra de \` autorização MyAuthRuleName \` do Namespace \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="9a0a7-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="9a0a7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a0a7-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="9a0a7-113">Remove a regra de \` autorização MyAuthRuleName \` do Hub de Eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="9a0a7-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="9a0a7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-114">PARAMETERS</span></span>

### <span data-ttu-id="9a0a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0a7-115">-DefaultProfile</span></span>
<span data-ttu-id="9a0a7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0a7-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9a0a7-117">-EventHub</span></span>
<span data-ttu-id="9a0a7-118">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="9a0a7-118">EventHub Name</span></span>

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

### <span data-ttu-id="9a0a7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9a0a7-119">-Force</span></span>
<span data-ttu-id="9a0a7-120">Não peça confirmação</span><span class="sxs-lookup"><span data-stu-id="9a0a7-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="9a0a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9a0a7-121">-Name</span></span>
<span data-ttu-id="9a0a7-122">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="9a0a7-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9a0a7-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a0a7-123">-Namespace</span></span>
<span data-ttu-id="9a0a7-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="9a0a7-124">Namespace Name</span></span>

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

### <span data-ttu-id="9a0a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a0a7-125">-PassThru</span></span>
<span data-ttu-id="9a0a7-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a0a7-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a0a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a0a7-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9a0a7-129">Resource Group Name</span></span>

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

### <span data-ttu-id="9a0a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a0a7-130">-Confirm</span></span>
<span data-ttu-id="9a0a7-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a0a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a0a7-132">-WhatIf</span></span>
<span data-ttu-id="9a0a7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a0a7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a0a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0a7-135">CommonParameters</span></span>
<span data-ttu-id="9a0a7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0a7-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0a7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0a7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-138">INPUTS</span></span>

### <span data-ttu-id="9a0a7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a0a7-139">System.String</span></span>

## <span data-ttu-id="9a0a7-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-140">OUTPUTS</span></span>

### <span data-ttu-id="9a0a7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a0a7-141">System.Boolean</span></span>

## <span data-ttu-id="9a0a7-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="9a0a7-142">NOTES</span></span>

## <span data-ttu-id="9a0a7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a0a7-143">RELATED LINKS</span></span>
