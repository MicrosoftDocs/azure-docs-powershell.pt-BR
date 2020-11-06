---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 9e7cfbe1ec0810b9d18f884306535d37a6110dd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600831"
---
# <span data-ttu-id="c8551-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c8551-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c8551-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8551-102">SYNOPSIS</span></span>
<span data-ttu-id="c8551-103">Remove a regra de autorização do hub de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="c8551-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="c8551-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8551-104">SYNTAX</span></span>

### <span data-ttu-id="c8551-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8551-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8551-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8551-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8551-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8551-107">DESCRIPTION</span></span>
<span data-ttu-id="c8551-108">O cmdlet Remove-AzEventHubAuthorizationRule remove e exclui a regra de autorização especificada do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="c8551-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="c8551-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8551-109">EXAMPLES</span></span>

### <span data-ttu-id="c8551-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8551-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c8551-111">Remove a regra de autorização \` MyAuthRuleName \` do namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="c8551-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c8551-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c8551-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c8551-113">Remove a regra de autorização \` MyAuthRuleName \` da MyEventHubName do hub de eventos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c8551-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="c8551-114">OS</span><span class="sxs-lookup"><span data-stu-id="c8551-114">PARAMETERS</span></span>

### <span data-ttu-id="c8551-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8551-115">-DefaultProfile</span></span>
<span data-ttu-id="c8551-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8551-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8551-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c8551-117">-EventHub</span></span>
<span data-ttu-id="c8551-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="c8551-118">EventHub Name</span></span>

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

### <span data-ttu-id="c8551-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c8551-119">-Force</span></span>
<span data-ttu-id="c8551-120">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="c8551-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="c8551-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8551-121">-Name</span></span>
<span data-ttu-id="c8551-122">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c8551-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c8551-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c8551-123">-Namespace</span></span>
<span data-ttu-id="c8551-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c8551-124">Namespace Name</span></span>

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

### <span data-ttu-id="c8551-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8551-125">-PassThru</span></span>
<span data-ttu-id="c8551-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c8551-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8551-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c8551-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8551-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8551-128">-ResourceGroupName</span></span>
<span data-ttu-id="c8551-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c8551-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c8551-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8551-130">-Confirm</span></span>
<span data-ttu-id="c8551-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8551-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8551-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8551-132">-WhatIf</span></span>
<span data-ttu-id="c8551-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8551-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8551-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8551-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8551-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8551-135">CommonParameters</span></span>
<span data-ttu-id="c8551-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8551-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8551-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8551-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8551-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8551-138">INPUTS</span></span>

### <span data-ttu-id="c8551-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c8551-139">System.String</span></span>

## <span data-ttu-id="c8551-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8551-140">OUTPUTS</span></span>

### <span data-ttu-id="c8551-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8551-141">System.Boolean</span></span>

## <span data-ttu-id="c8551-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8551-142">NOTES</span></span>

## <span data-ttu-id="c8551-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8551-143">RELATED LINKS</span></span>
