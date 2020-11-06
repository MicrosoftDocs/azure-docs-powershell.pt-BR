---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: e9b699e8839f2ba9426945ef0de883c4bfac40d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609620"
---
# <span data-ttu-id="f6122-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6122-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="f6122-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6122-102">SYNOPSIS</span></span>
<span data-ttu-id="f6122-103">Remove uma regra de autorização de um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6122-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6122-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6122-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6122-105">DESCRIPTION</span></span>
<span data-ttu-id="f6122-106">O cmdlet **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** remove uma regra de autorização de assinatura de acesso compartilhado (SAS) de um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6122-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="f6122-107">Regras de autorização gerenciem o acesso a um namespace.</span><span class="sxs-lookup"><span data-stu-id="f6122-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="f6122-108">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="f6122-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f6122-109">Os níveis de permissão podem ser dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f6122-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="f6122-110">Ouvir</span><span class="sxs-lookup"><span data-stu-id="f6122-110">Listen</span></span>
- <span data-ttu-id="f6122-111">Enviar</span><span class="sxs-lookup"><span data-stu-id="f6122-111">Send</span></span>
- <span data-ttu-id="f6122-112">Gerencia</span><span class="sxs-lookup"><span data-stu-id="f6122-112">Manage</span></span>

<span data-ttu-id="f6122-113">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="f6122-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f6122-114">Por exemplo, um cliente que recebeu a permissão de escuta é direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="f6122-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="f6122-115">A remoção de uma regra de autorização também remove a permissão do usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="f6122-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="f6122-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6122-116">EXAMPLES</span></span>

### <span data-ttu-id="f6122-117">Exemplo 1: remover uma regra de autorização de um namespace</span><span class="sxs-lookup"><span data-stu-id="f6122-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f6122-118">Esse comando Remove a regra de autorização chamada ListenRule do namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f6122-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="f6122-119">Ao executar esse comando, você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6122-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="f6122-120">OS</span><span class="sxs-lookup"><span data-stu-id="f6122-120">PARAMETERS</span></span>

### <span data-ttu-id="f6122-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6122-121">-AuthorizationRule</span></span>
<span data-ttu-id="f6122-122">Especifica o nome da regra de autenticação SAS a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f6122-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6122-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f6122-123">-Force</span></span>
<span data-ttu-id="f6122-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f6122-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f6122-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6122-125">-Namespace</span></span>
<span data-ttu-id="f6122-126">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="f6122-126">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f6122-127">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6122-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6122-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="f6122-128">-ResourceGroup</span></span>
<span data-ttu-id="f6122-129">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6122-129">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="f6122-130">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6122-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f6122-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6122-131">-Confirm</span></span>
<span data-ttu-id="f6122-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6122-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6122-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6122-133">-WhatIf</span></span>
<span data-ttu-id="f6122-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6122-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6122-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6122-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6122-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6122-136">-DefaultProfile</span></span>
<span data-ttu-id="f6122-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6122-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6122-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6122-138">CommonParameters</span></span>
<span data-ttu-id="f6122-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6122-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6122-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6122-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6122-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6122-141">INPUTS</span></span>

## <span data-ttu-id="f6122-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6122-142">OUTPUTS</span></span>

### <span data-ttu-id="f6122-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6122-143">System.Boolean</span></span>

## <span data-ttu-id="f6122-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6122-144">NOTES</span></span>

## <span data-ttu-id="f6122-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6122-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6122-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6122-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f6122-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6122-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="f6122-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f6122-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


