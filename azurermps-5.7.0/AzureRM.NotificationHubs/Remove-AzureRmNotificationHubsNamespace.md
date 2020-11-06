---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428855"
---
# <span data-ttu-id="462b2-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="462b2-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="462b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="462b2-102">SYNOPSIS</span></span>
<span data-ttu-id="462b2-103">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="462b2-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="462b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="462b2-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="462b2-105">DESCRIPTION</span></span>
<span data-ttu-id="462b2-106">O cmdlet **Remove-AzureRmNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="462b2-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="462b2-107">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="462b2-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="462b2-108">O cmdlet **Remove-AzureRmNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="462b2-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="462b2-109">Quando você executar esse cmdlet, o namespace especificado será excluído juntamente com todos os hubs de notificação associados a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="462b2-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="462b2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="462b2-110">EXAMPLES</span></span>

### <span data-ttu-id="462b2-111">Exemplo 1: remover um namespace do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="462b2-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="462b2-112">Esse comando Remove o namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="462b2-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="462b2-113">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="462b2-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="462b2-114">OS</span><span class="sxs-lookup"><span data-stu-id="462b2-114">PARAMETERS</span></span>

### <span data-ttu-id="462b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462b2-115">-DefaultProfile</span></span>
<span data-ttu-id="462b2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="462b2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="462b2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="462b2-117">-Force</span></span>
<span data-ttu-id="462b2-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="462b2-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462b2-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="462b2-119">-Namespace</span></span>
<span data-ttu-id="462b2-120">Especifica o namespace que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="462b2-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="462b2-121">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="462b2-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462b2-122">-Resource</span><span class="sxs-lookup"><span data-stu-id="462b2-122">-ResourceGroup</span></span>
<span data-ttu-id="462b2-123">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="462b2-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="462b2-124">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="462b2-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="462b2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="462b2-125">-Confirm</span></span>
<span data-ttu-id="462b2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="462b2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462b2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462b2-127">-WhatIf</span></span>
<span data-ttu-id="462b2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="462b2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="462b2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="462b2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462b2-130">CommonParameters</span></span>
<span data-ttu-id="462b2-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="462b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462b2-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462b2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462b2-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="462b2-133">INPUTS</span></span>

### <span data-ttu-id="462b2-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="462b2-134">None</span></span>
<span data-ttu-id="462b2-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="462b2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="462b2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="462b2-136">OUTPUTS</span></span>

## <span data-ttu-id="462b2-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="462b2-137">NOTES</span></span>

## <span data-ttu-id="462b2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="462b2-138">RELATED LINKS</span></span>

[<span data-ttu-id="462b2-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="462b2-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="462b2-140">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="462b2-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="462b2-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="462b2-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


