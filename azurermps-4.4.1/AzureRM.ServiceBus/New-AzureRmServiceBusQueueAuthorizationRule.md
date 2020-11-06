---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427781"
---
# <span data-ttu-id="cc430-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc430-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="cc430-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc430-102">SYNOPSIS</span></span>
<span data-ttu-id="cc430-103">Cria uma nova regra de autorização para a fila do barramento do serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="cc430-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc430-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc430-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc430-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc430-105">DESCRIPTION</span></span>
<span data-ttu-id="cc430-106">O cmdlet **New-AzureRmServiceBusQueueAuthorizationRule** cria uma nova regra de autorização para a fila de barramento de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="cc430-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="cc430-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc430-107">EXAMPLES</span></span>

### <span data-ttu-id="cc430-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc430-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="cc430-109">Cria uma regra de autorização `SBAuthoRule1` com os direitos de **escuta e envio** para a fila `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="cc430-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="cc430-110">OS</span><span class="sxs-lookup"><span data-stu-id="cc430-110">PARAMETERS</span></span>

### <span data-ttu-id="cc430-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="cc430-111">-ResourceGroup</span></span>
<span data-ttu-id="cc430-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc430-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc430-113">-Direitos</span><span class="sxs-lookup"><span data-stu-id="cc430-113">-Rights</span></span>
<span data-ttu-id="cc430-114">Especifica os direitos; por exemplo,</span><span class="sxs-lookup"><span data-stu-id="cc430-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="cc430-115">@ ("Ouvir", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="cc430-115">@("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc430-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc430-116">-Confirm</span></span>
<span data-ttu-id="cc430-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc430-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc430-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc430-118">-WhatIf</span></span>
<span data-ttu-id="cc430-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc430-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc430-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc430-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc430-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc430-121">-DefaultProfile</span></span>
<span data-ttu-id="cc430-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc430-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc430-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc430-123">-Name</span></span>
<span data-ttu-id="cc430-124">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="cc430-124">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc430-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc430-125">-Namespace</span></span>
<span data-ttu-id="cc430-126">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="cc430-126">Namespace Name.</span></span>

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

### <span data-ttu-id="cc430-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="cc430-127">-Queue</span></span>
<span data-ttu-id="cc430-128">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="cc430-128">Queue Name.</span></span>

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

### <span data-ttu-id="cc430-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc430-129">CommonParameters</span></span>
<span data-ttu-id="cc430-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc430-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc430-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc430-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc430-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc430-132">INPUTS</span></span>

### <span data-ttu-id="cc430-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="cc430-133">-ResourceGroup</span></span>
 <span data-ttu-id="cc430-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cc430-134">System.String</span></span>
 

### <span data-ttu-id="cc430-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cc430-135">-NamespaceName</span></span>
 <span data-ttu-id="cc430-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cc430-136">System.String</span></span>
 

### <span data-ttu-id="cc430-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="cc430-137">-QueueName</span></span>
 <span data-ttu-id="cc430-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc430-138">System.String</span></span>
 

### <span data-ttu-id="cc430-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="cc430-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="cc430-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc430-140">System.String</span></span>

## <span data-ttu-id="cc430-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc430-141">OUTPUTS</span></span>

### <span data-ttu-id="cc430-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cc430-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="cc430-143">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 Location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="cc430-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="cc430-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc430-144">NOTES</span></span>

## <span data-ttu-id="cc430-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc430-145">RELATED LINKS</span></span>

