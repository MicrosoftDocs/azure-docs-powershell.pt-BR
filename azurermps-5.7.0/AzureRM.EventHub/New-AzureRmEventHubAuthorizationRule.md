---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: ae7fe44bf0fd3eccb157cefd6f57dade203d4fb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609967"
---
# <span data-ttu-id="7d024-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d024-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7d024-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d024-102">SYNOPSIS</span></span>
<span data-ttu-id="7d024-103">Cria uma nova regra de autorização de hubs de eventos para namespace ou eventhub.</span><span class="sxs-lookup"><span data-stu-id="7d024-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d024-104">SYNTAX</span></span>

### <span data-ttu-id="7d024-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d024-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d024-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d024-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d024-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d024-107">DESCRIPTION</span></span>
<span data-ttu-id="7d024-108">O cmdlet New-AzureRmEventHubAuthorizationRule cria uma nova regra de autorização de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="7d024-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7d024-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d024-109">EXAMPLES</span></span>

### <span data-ttu-id="7d024-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d024-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="7d024-111">Cria uma regra de autorização \` MyAuthRuleName \` concedendo os direitos de escuta e envio ao namespace \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7d024-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7d024-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7d024-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="7d024-113">Cria uma regra de autorização \` MyAuthRuleName \` concedendo os direitos de escuta e envio ao Hub de eventos \` MyEventHubName \` no namespace \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7d024-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7d024-114">OS</span><span class="sxs-lookup"><span data-stu-id="7d024-114">PARAMETERS</span></span>

### <span data-ttu-id="7d024-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d024-115">-DefaultProfile</span></span>
<span data-ttu-id="7d024-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d024-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7d024-117">-EventHub</span></span>
<span data-ttu-id="7d024-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="7d024-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d024-119">-Name</span></span>
<span data-ttu-id="7d024-120">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d024-120">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d024-121">-Namespace</span></span>
<span data-ttu-id="7d024-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7d024-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d024-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d024-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d024-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-125">-Direitos</span><span class="sxs-lookup"><span data-stu-id="7d024-125">-Rights</span></span>
<span data-ttu-id="7d024-126">Direitos, como "escutar", "enviar", "gerenciar"</span><span class="sxs-lookup"><span data-stu-id="7d024-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d024-127">-Confirm</span></span>
<span data-ttu-id="7d024-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d024-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d024-129">-WhatIf</span></span>
<span data-ttu-id="7d024-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d024-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d024-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d024-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d024-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d024-132">CommonParameters</span></span>
<span data-ttu-id="7d024-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d024-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7d024-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d024-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d024-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d024-135">INPUTS</span></span>

### <span data-ttu-id="7d024-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7d024-136">System.String</span></span>
<span data-ttu-id="7d024-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d024-137">System.String[]</span></span>


## <span data-ttu-id="7d024-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d024-138">OUTPUTS</span></span>

### <span data-ttu-id="7d024-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7d024-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="7d024-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d024-140">NOTES</span></span>

## <span data-ttu-id="7d024-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d024-141">RELATED LINKS</span></span>
