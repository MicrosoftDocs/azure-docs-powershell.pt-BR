---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602615"
---
# <span data-ttu-id="b5d30-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5d30-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b5d30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5d30-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d30-103">Remove a regra de autorização do hub de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="b5d30-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5d30-104">SYNTAX</span></span>

### <span data-ttu-id="b5d30-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5d30-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5d30-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5d30-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d30-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5d30-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d30-108">O cmdlet Remove-AzureRmEventHubAuthorizationRule remove e exclui a regra de autorização especificada do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="b5d30-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="b5d30-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5d30-109">EXAMPLES</span></span>

### <span data-ttu-id="b5d30-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5d30-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="b5d30-111">Remove a regra de autorização \` MyAuthRuleName \` do namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="b5d30-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="b5d30-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b5d30-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="b5d30-113">Remove a regra de autorização \` MyAuthRuleName \` da MyEventHubName do hub de eventos \` \` .</span><span class="sxs-lookup"><span data-stu-id="b5d30-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="b5d30-114">OS</span><span class="sxs-lookup"><span data-stu-id="b5d30-114">PARAMETERS</span></span>

### <span data-ttu-id="b5d30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d30-115">-DefaultProfile</span></span>
<span data-ttu-id="b5d30-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5d30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d30-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b5d30-117">-EventHub</span></span>
<span data-ttu-id="b5d30-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="b5d30-118">EventHub Name</span></span>

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

### <span data-ttu-id="b5d30-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b5d30-119">-Force</span></span>
<span data-ttu-id="b5d30-120">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="b5d30-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="b5d30-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5d30-121">-Name</span></span>
<span data-ttu-id="b5d30-122">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5d30-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b5d30-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5d30-123">-Namespace</span></span>
<span data-ttu-id="b5d30-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b5d30-124">Namespace Name</span></span>

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

### <span data-ttu-id="b5d30-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5d30-125">-PassThru</span></span>
<span data-ttu-id="b5d30-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b5d30-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5d30-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b5d30-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5d30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d30-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5d30-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b5d30-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b5d30-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5d30-130">-Confirm</span></span>
<span data-ttu-id="b5d30-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5d30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d30-132">-WhatIf</span></span>
<span data-ttu-id="b5d30-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5d30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d30-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5d30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d30-135">CommonParameters</span></span>
<span data-ttu-id="b5d30-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d30-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d30-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d30-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5d30-138">INPUTS</span></span>

### <span data-ttu-id="b5d30-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b5d30-139">System.String</span></span>

## <span data-ttu-id="b5d30-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5d30-140">OUTPUTS</span></span>

### <span data-ttu-id="b5d30-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5d30-141">System.Boolean</span></span>

## <span data-ttu-id="b5d30-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5d30-142">NOTES</span></span>

## <span data-ttu-id="b5d30-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5d30-143">RELATED LINKS</span></span>
