---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d77a0a31cdf9e7731346bd70a24533ce7a464c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430299"
---
# <span data-ttu-id="40b60-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40b60-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="40b60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40b60-102">SYNOPSIS</span></span>
<span data-ttu-id="40b60-103">Atualiza a regra de autorização especificada em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="40b60-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40b60-104">SYNTAX</span></span>

### <span data-ttu-id="40b60-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="40b60-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b60-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="40b60-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b60-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40b60-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40b60-108">DESCRIPTION</span></span>
<span data-ttu-id="40b60-109">O cmdlet Set-AzureRmEventHubAuthorizationRule atualiza a regra de autorização especificada em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="40b60-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="40b60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40b60-110">EXAMPLES</span></span>

### <span data-ttu-id="40b60-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40b60-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="40b60-112">Atualiza a regra de autorização \` MyAuthRuleName \` para conceder direitos de gerenciamento ao Hub de eventos \` MyEventHubName \` , delimitado pelo namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="40b60-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="40b60-113">OS</span><span class="sxs-lookup"><span data-stu-id="40b60-113">PARAMETERS</span></span>

### <span data-ttu-id="40b60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b60-114">-DefaultProfile</span></span>
<span data-ttu-id="40b60-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40b60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b60-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="40b60-116">-EventHub</span></span>
<span data-ttu-id="40b60-117">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="40b60-117">EventHub Name</span></span>

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

### <span data-ttu-id="40b60-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40b60-118">-InputObject</span></span>
<span data-ttu-id="40b60-119">Objeto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40b60-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="40b60-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="40b60-120">-Name</span></span>
<span data-ttu-id="40b60-121">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40b60-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="40b60-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40b60-122">-Namespace</span></span>
<span data-ttu-id="40b60-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="40b60-123">Namespace Name</span></span>

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

### <span data-ttu-id="40b60-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b60-124">-ResourceGroupName</span></span>
<span data-ttu-id="40b60-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="40b60-125">Resource Group Name</span></span>

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

### <span data-ttu-id="40b60-126">-Direitos</span><span class="sxs-lookup"><span data-stu-id="40b60-126">-Rights</span></span>
<span data-ttu-id="40b60-127">Direitos, por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="40b60-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="40b60-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40b60-128">-Confirm</span></span>
<span data-ttu-id="40b60-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40b60-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b60-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b60-130">-WhatIf</span></span>
<span data-ttu-id="40b60-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40b60-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b60-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40b60-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b60-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b60-133">CommonParameters</span></span>
<span data-ttu-id="40b60-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b60-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b60-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b60-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b60-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40b60-136">INPUTS</span></span>

### <span data-ttu-id="40b60-137">System. String</span><span class="sxs-lookup"><span data-stu-id="40b60-137">System.String</span></span>

### <span data-ttu-id="40b60-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="40b60-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="40b60-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="40b60-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="40b60-140">System. String []</span><span class="sxs-lookup"><span data-stu-id="40b60-140">System.String[]</span></span>

## <span data-ttu-id="40b60-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40b60-141">OUTPUTS</span></span>

### <span data-ttu-id="40b60-142">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="40b60-142">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="40b60-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40b60-143">NOTES</span></span>

## <span data-ttu-id="40b60-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40b60-144">RELATED LINKS</span></span>
