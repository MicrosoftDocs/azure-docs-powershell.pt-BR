---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429115"
---
# <span data-ttu-id="4591f-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4591f-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="4591f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4591f-102">SYNOPSIS</span></span>
<span data-ttu-id="4591f-103">Obtém a descrição de uma regra de autorização especificada para uma determinada fila de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="4591f-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4591f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4591f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4591f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4591f-105">DESCRIPTION</span></span>
<span data-ttu-id="4591f-106">O cmdlet **Get-AzureRmServiceBusQueueAuthorizationRule** Obtém a descrição de uma regra de autorização especificada em uma determinada fila de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4591f-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="4591f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4591f-107">EXAMPLES</span></span>

### <span data-ttu-id="4591f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4591f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="4591f-109">Retorna a descrição da regra de autorização especificada para uma determinada fila de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4591f-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="4591f-110">OS</span><span class="sxs-lookup"><span data-stu-id="4591f-110">PARAMETERS</span></span>

### <span data-ttu-id="4591f-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="4591f-111">-ResourceGroup</span></span>
<span data-ttu-id="4591f-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4591f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="4591f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4591f-113">-DefaultProfile</span></span>
<span data-ttu-id="4591f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4591f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4591f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4591f-115">-Name</span></span>
<span data-ttu-id="4591f-116">Nome do AuthorizationRule do EventHub.</span><span class="sxs-lookup"><span data-stu-id="4591f-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4591f-117">-Namespace</span></span>
<span data-ttu-id="4591f-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="4591f-118">Namespace Name.</span></span>

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

### <span data-ttu-id="4591f-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="4591f-119">-Queue</span></span>
<span data-ttu-id="4591f-120">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="4591f-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4591f-121">CommonParameters</span></span>
<span data-ttu-id="4591f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4591f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4591f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4591f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4591f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4591f-124">INPUTS</span></span>

### <span data-ttu-id="4591f-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="4591f-125">-ResourceGroup</span></span>
 <span data-ttu-id="4591f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4591f-126">System.String</span></span>
 

### <span data-ttu-id="4591f-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4591f-127">-NamespaceName</span></span>
 <span data-ttu-id="4591f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4591f-128">System.String</span></span>
 

### <span data-ttu-id="4591f-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="4591f-129">-QueueName</span></span>
 <span data-ttu-id="4591f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4591f-130">System.String</span></span>
 

### <span data-ttu-id="4591f-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4591f-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="4591f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4591f-132">System.String</span></span>

## <span data-ttu-id="4591f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4591f-133">OUTPUTS</span></span>

### <span data-ttu-id="4591f-134">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4591f-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4591f-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 Location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="4591f-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="4591f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4591f-136">NOTES</span></span>

## <span data-ttu-id="4591f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4591f-137">RELATED LINKS</span></span>

