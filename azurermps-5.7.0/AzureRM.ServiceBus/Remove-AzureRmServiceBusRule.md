---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431605"
---
# <span data-ttu-id="a5152-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="a5152-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="a5152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5152-102">SYNOPSIS</span></span>
<span data-ttu-id="a5152-103">Remove a regra speficied de uma determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="a5152-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5152-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5152-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5152-105">DESCRIPTION</span></span>
<span data-ttu-id="a5152-106">O cmdlet **Remove-AzureRmServiceBusRule** remove a regra de uma assinatura de determinado tópico.</span><span class="sxs-lookup"><span data-stu-id="a5152-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="a5152-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5152-107">EXAMPLES</span></span>

### <span data-ttu-id="a5152-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5152-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="a5152-109">Remove a regra `SBRule` de assinatura `SBSubscription` do tópico especificado `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="a5152-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="a5152-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5152-110">PARAMETERS</span></span>

### <span data-ttu-id="a5152-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5152-111">-DefaultProfile</span></span>
<span data-ttu-id="a5152-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5152-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5152-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a5152-113">-Force</span></span>
<span data-ttu-id="a5152-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a5152-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a5152-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5152-115">-Name</span></span>
<span data-ttu-id="a5152-116">Nome da regra.</span><span class="sxs-lookup"><span data-stu-id="a5152-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5152-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5152-117">-Namespace</span></span>
<span data-ttu-id="a5152-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="a5152-118">Namespace Name.</span></span>

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

### <span data-ttu-id="a5152-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5152-119">-PassThru</span></span>
<span data-ttu-id="a5152-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="a5152-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a5152-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5152-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5152-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a5152-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5152-123">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="a5152-123">-Subscription</span></span>
<span data-ttu-id="a5152-124">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a5152-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5152-125">-Tópico</span><span class="sxs-lookup"><span data-stu-id="a5152-125">-Topic</span></span>
<span data-ttu-id="a5152-126">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="a5152-126">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5152-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5152-127">-Confirm</span></span>
<span data-ttu-id="a5152-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5152-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5152-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5152-129">-WhatIf</span></span>
<span data-ttu-id="a5152-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5152-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5152-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5152-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5152-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5152-132">CommonParameters</span></span>
<span data-ttu-id="a5152-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5152-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5152-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5152-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5152-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5152-135">INPUTS</span></span>

### <span data-ttu-id="a5152-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5152-136">System.String</span></span>

## <span data-ttu-id="a5152-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5152-137">OUTPUTS</span></span>

### <span data-ttu-id="a5152-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5152-138">System.Boolean</span></span>

## <span data-ttu-id="a5152-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5152-139">NOTES</span></span>

## <span data-ttu-id="a5152-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5152-140">RELATED LINKS</span></span>
