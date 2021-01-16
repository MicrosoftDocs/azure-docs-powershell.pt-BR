---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261569"
---
# <span data-ttu-id="c0e36-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0e36-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c0e36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0e36-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e36-103">Remove a regra de autorização do hub de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="c0e36-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="c0e36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0e36-104">SYNTAX</span></span>

### <span data-ttu-id="c0e36-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0e36-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e36-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0e36-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e36-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0e36-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e36-108">O cmdlet Remove-AzEventHubAuthorizationRule remove e exclui a regra de autorização especificada do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="c0e36-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="c0e36-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0e36-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e36-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0e36-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="c0e36-111">Remove a regra de autorização \` MyAuthRuleName \` do namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="c0e36-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c0e36-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0e36-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="c0e36-113">Remove a regra de autorização \` MyAuthRuleName \` da MyEventHubName do hub de eventos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c0e36-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="c0e36-114">OS</span><span class="sxs-lookup"><span data-stu-id="c0e36-114">PARAMETERS</span></span>

### <span data-ttu-id="c0e36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e36-115">-DefaultProfile</span></span>
<span data-ttu-id="c0e36-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e36-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c0e36-117">-EventHub</span></span>
<span data-ttu-id="c0e36-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="c0e36-118">EventHub Name</span></span>

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

### <span data-ttu-id="c0e36-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c0e36-119">-Force</span></span>
<span data-ttu-id="c0e36-120">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="c0e36-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="c0e36-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0e36-121">-Name</span></span>
<span data-ttu-id="c0e36-122">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0e36-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c0e36-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c0e36-123">-Namespace</span></span>
<span data-ttu-id="c0e36-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c0e36-124">Namespace Name</span></span>

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

### <span data-ttu-id="c0e36-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0e36-125">-PassThru</span></span>
<span data-ttu-id="c0e36-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c0e36-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0e36-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c0e36-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0e36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e36-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0e36-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c0e36-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c0e36-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0e36-130">-Confirm</span></span>
<span data-ttu-id="c0e36-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0e36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e36-132">-WhatIf</span></span>
<span data-ttu-id="c0e36-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0e36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e36-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0e36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e36-135">CommonParameters</span></span>
<span data-ttu-id="c0e36-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e36-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e36-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e36-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0e36-138">INPUTS</span></span>

### <span data-ttu-id="c0e36-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e36-139">System.String</span></span>

## <span data-ttu-id="c0e36-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0e36-140">OUTPUTS</span></span>

### <span data-ttu-id="c0e36-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0e36-141">System.Boolean</span></span>

## <span data-ttu-id="c0e36-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0e36-142">NOTES</span></span>

## <span data-ttu-id="c0e36-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0e36-143">RELATED LINKS</span></span>
