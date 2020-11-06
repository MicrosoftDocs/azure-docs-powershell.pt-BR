---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429104"
---
# <span data-ttu-id="0cf1a-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0cf1a-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="0cf1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf1a-103">Remove a regra de autorização de uma fila do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cf1a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cf1a-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf1a-106">O cmdlet **Remove-AzureRmServiceBusQueueAuthorizationRule** remove a regra de autorização de uma fila do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0cf1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cf1a-107">EXAMPLES</span></span>

### <span data-ttu-id="0cf1a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0cf1a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="0cf1a-109">Remove a regra `SBAuthoRule1` de autorização da fila `SB-Queue_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0cf1a-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="0cf1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="0cf1a-110">PARAMETERS</span></span>

### <span data-ttu-id="0cf1a-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="0cf1a-111">-ResourceGroup</span></span>
<span data-ttu-id="0cf1a-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="0cf1a-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cf1a-113">-Confirm</span></span>
<span data-ttu-id="0cf1a-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf1a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf1a-115">-WhatIf</span></span>
<span data-ttu-id="0cf1a-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf1a-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf1a-118">-DefaultProfile</span></span>
<span data-ttu-id="0cf1a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf1a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cf1a-120">-Name</span></span>
<span data-ttu-id="0cf1a-121">Nome da fila AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="0cf1a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0cf1a-122">-Namespace</span></span>
<span data-ttu-id="0cf1a-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-123">Namespace Name.</span></span>

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

### <span data-ttu-id="0cf1a-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="0cf1a-124">-Queue</span></span>
<span data-ttu-id="0cf1a-125">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-125">Queue Name.</span></span>

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

### <span data-ttu-id="0cf1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf1a-126">CommonParameters</span></span>
<span data-ttu-id="0cf1a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf1a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf1a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cf1a-129">INPUTS</span></span>

### <span data-ttu-id="0cf1a-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="0cf1a-130">-ResourceGroup</span></span>
 <span data-ttu-id="0cf1a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf1a-131">System.String</span></span>

### <span data-ttu-id="0cf1a-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0cf1a-132">-NamespaceName</span></span>
 <span data-ttu-id="0cf1a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf1a-133">System.String</span></span>

### <span data-ttu-id="0cf1a-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="0cf1a-134">-QueueName</span></span>
 <span data-ttu-id="0cf1a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf1a-135">System.String</span></span>

### <span data-ttu-id="0cf1a-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0cf1a-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="0cf1a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf1a-137">System.String</span></span>

## <span data-ttu-id="0cf1a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cf1a-138">OUTPUTS</span></span>

### <span data-ttu-id="0cf1a-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="0cf1a-139">System.Object</span></span>

## <span data-ttu-id="0cf1a-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cf1a-140">NOTES</span></span>

## <span data-ttu-id="0cf1a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf1a-141">RELATED LINKS</span></span>

