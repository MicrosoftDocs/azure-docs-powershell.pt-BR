---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440552"
---
# <span data-ttu-id="59197-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59197-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="59197-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59197-102">SYNOPSIS</span></span>
<span data-ttu-id="59197-103">Atualiza a descrição da regra de autorização especificada para a fila de barramento do serviço determinada.</span><span class="sxs-lookup"><span data-stu-id="59197-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59197-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59197-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59197-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59197-105">DESCRIPTION</span></span>
<span data-ttu-id="59197-106">O cmdlet **set-AzureRmServiceBusQueueAuthorizationRule** atualiza a descrição da regra de autorização especificada da fila de barramento de serviço determinada.</span><span class="sxs-lookup"><span data-stu-id="59197-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="59197-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59197-107">EXAMPLES</span></span>

### <span data-ttu-id="59197-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59197-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="59197-109">Adiciona **gerenciar** aos direitos de acesso da regra de autorização `SBAuthoRule1` da fila `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="59197-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="59197-110">OS</span><span class="sxs-lookup"><span data-stu-id="59197-110">PARAMETERS</span></span>

### <span data-ttu-id="59197-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="59197-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="59197-112">O nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="59197-112">The authorization rule name.</span></span> <span data-ttu-id="59197-113">Obrigatório se **-AuthruleObj** não for especificado.</span><span class="sxs-lookup"><span data-stu-id="59197-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59197-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="59197-114">-AuthRuleObj</span></span>
<span data-ttu-id="59197-115">O objeto de regra de autorização da fila de barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="59197-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59197-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="59197-116">-NamespaceName</span></span>
<span data-ttu-id="59197-117">O nome do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="59197-117">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="59197-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="59197-118">-QueueName</span></span>
<span data-ttu-id="59197-119">O nome da fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="59197-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59197-120">-Resource</span><span class="sxs-lookup"><span data-stu-id="59197-120">-ResourceGroup</span></span>
<span data-ttu-id="59197-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59197-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="59197-122">-Direitos</span><span class="sxs-lookup"><span data-stu-id="59197-122">-Rights</span></span>
<span data-ttu-id="59197-123">Os direitos; por exemplo, @ ("Listen", "enviar", "gerenciar").</span><span class="sxs-lookup"><span data-stu-id="59197-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="59197-124">Obrigatório se ' AuthruleObj ' não especificado.</span><span class="sxs-lookup"><span data-stu-id="59197-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59197-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59197-125">-Confirm</span></span>
<span data-ttu-id="59197-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59197-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59197-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59197-127">-WhatIf</span></span>
<span data-ttu-id="59197-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59197-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59197-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59197-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59197-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59197-130">CommonParameters</span></span>
<span data-ttu-id="59197-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59197-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59197-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59197-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59197-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59197-133">INPUTS</span></span>

### <span data-ttu-id="59197-134">-Resource</span><span class="sxs-lookup"><span data-stu-id="59197-134">-ResourceGroup</span></span>
 <span data-ttu-id="59197-135">System. String</span><span class="sxs-lookup"><span data-stu-id="59197-135">System.String</span></span>

### <span data-ttu-id="59197-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="59197-136">-NamespaceName</span></span>
 <span data-ttu-id="59197-137">System. String</span><span class="sxs-lookup"><span data-stu-id="59197-137">System.String</span></span>

### <span data-ttu-id="59197-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="59197-138">-QueueName</span></span>
 <span data-ttu-id="59197-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59197-139">System.String</span></span>

### <span data-ttu-id="59197-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="59197-140">-AuthRuleObj</span></span>
 <span data-ttu-id="59197-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="59197-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="59197-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59197-142">OUTPUTS</span></span>

### <span data-ttu-id="59197-143">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="59197-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="59197-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59197-144">NOTES</span></span>

## <span data-ttu-id="59197-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59197-145">RELATED LINKS</span></span>

