---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440559"
---
# <span data-ttu-id="7a9bc-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7a9bc-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="7a9bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9bc-103">Remove a regra de autorização de um tópico do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a9bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a9bc-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9bc-106">O cmdlet **Remove-AzureRmServiceBusTopicAuthorizationRule** remove a regra de autorização de um tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7a9bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="7a9bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a9bc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="7a9bc-109">Remove a regra `SBTopicAuthoRule1` de autorização do tópico `SB-Topic_exampl1` do namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7a9bc-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7a9bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="7a9bc-110">PARAMETERS</span></span>

### <span data-ttu-id="7a9bc-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="7a9bc-111">-ResourceGroup</span></span>
<span data-ttu-id="7a9bc-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a9bc-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a9bc-113">-Confirm</span></span>
<span data-ttu-id="7a9bc-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9bc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9bc-115">-WhatIf</span></span>
<span data-ttu-id="7a9bc-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a9bc-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9bc-118">-DefaultProfile</span></span>
<span data-ttu-id="7a9bc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a9bc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a9bc-120">-Name</span></span>
<span data-ttu-id="7a9bc-121">Nome do tópico AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7a9bc-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a9bc-122">-Namespace</span></span>
<span data-ttu-id="7a9bc-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-123">Namespace Name.</span></span>

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

### <span data-ttu-id="7a9bc-124">-Tópico</span><span class="sxs-lookup"><span data-stu-id="7a9bc-124">-Topic</span></span>
<span data-ttu-id="7a9bc-125">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-125">Topic Name.</span></span>

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

### <span data-ttu-id="7a9bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9bc-126">CommonParameters</span></span>
<span data-ttu-id="7a9bc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a9bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9bc-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9bc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a9bc-129">INPUTS</span></span>

### <span data-ttu-id="7a9bc-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="7a9bc-130">-ResourceGroup</span></span>
 <span data-ttu-id="7a9bc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9bc-131">System.String</span></span>

### <span data-ttu-id="7a9bc-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7a9bc-132">-NamespaceName</span></span>
 <span data-ttu-id="7a9bc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9bc-133">System.String</span></span>

### <span data-ttu-id="7a9bc-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="7a9bc-134">-TopicName</span></span>
 <span data-ttu-id="7a9bc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9bc-135">System.String</span></span>

### <span data-ttu-id="7a9bc-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7a9bc-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7a9bc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9bc-137">System.String</span></span>

## <span data-ttu-id="7a9bc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a9bc-138">OUTPUTS</span></span>

### <span data-ttu-id="7a9bc-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="7a9bc-139">System.Object</span></span>

## <span data-ttu-id="7a9bc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a9bc-140">NOTES</span></span>

## <span data-ttu-id="7a9bc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a9bc-141">RELATED LINKS</span></span>

