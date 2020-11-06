---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429100"
---
# <span data-ttu-id="707c2-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="707c2-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="707c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="707c2-102">SYNOPSIS</span></span>
<span data-ttu-id="707c2-103">Remove a assinatura de um tópico do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="707c2-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="707c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="707c2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="707c2-105">DESCRIPTION</span></span>
<span data-ttu-id="707c2-106">O cmdlet **Remove-AzureRmServiceBusSubscription** remove a assinatura de um tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="707c2-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="707c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="707c2-107">EXAMPLES</span></span>

### <span data-ttu-id="707c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="707c2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="707c2-109">Remove a assinatura do `SB-TopicSubscription-Example1` tópico `SB-Topic_exampl1` no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="707c2-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="707c2-110">OS</span><span class="sxs-lookup"><span data-stu-id="707c2-110">PARAMETERS</span></span>

### <span data-ttu-id="707c2-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="707c2-111">-Confirm</span></span>
<span data-ttu-id="707c2-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="707c2-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707c2-113">-WhatIf</span></span>
<span data-ttu-id="707c2-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="707c2-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707c2-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="707c2-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707c2-116">-DefaultProfile</span></span>
<span data-ttu-id="707c2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="707c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="707c2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="707c2-118">-Name</span></span>
<span data-ttu-id="707c2-119">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="707c2-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="707c2-120">-Namespace</span></span>
<span data-ttu-id="707c2-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="707c2-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="707c2-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="707c2-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-124">-Tópico</span><span class="sxs-lookup"><span data-stu-id="707c2-124">-Topic</span></span>
<span data-ttu-id="707c2-125">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="707c2-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707c2-126">CommonParameters</span></span>
<span data-ttu-id="707c2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707c2-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707c2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="707c2-129">INPUTS</span></span>

### <span data-ttu-id="707c2-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="707c2-130">-ResourceGroup</span></span>
 <span data-ttu-id="707c2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="707c2-131">System.String</span></span>

### <span data-ttu-id="707c2-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="707c2-132">-NamespaceName</span></span>
 <span data-ttu-id="707c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="707c2-133">System.String</span></span>

### <span data-ttu-id="707c2-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="707c2-134">-TopicName</span></span>
 <span data-ttu-id="707c2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="707c2-135">System.String</span></span>

### <span data-ttu-id="707c2-136">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="707c2-136">-SubscriptionName</span></span>
 <span data-ttu-id="707c2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="707c2-137">System.String</span></span>

## <span data-ttu-id="707c2-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="707c2-138">OUTPUTS</span></span>

### <span data-ttu-id="707c2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="707c2-139">System.Boolean</span></span>

## <span data-ttu-id="707c2-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="707c2-140">NOTES</span></span>

## <span data-ttu-id="707c2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="707c2-141">RELATED LINKS</span></span>

