---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602409"
---
# <span data-ttu-id="53c13-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53c13-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="53c13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53c13-102">SYNOPSIS</span></span>
<span data-ttu-id="53c13-103">Cria uma nova regra de autorização para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="53c13-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53c13-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53c13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53c13-105">DESCRIPTION</span></span>
<span data-ttu-id="53c13-106">O cmdlet **New-AzureRmServiceBusTopicAuthorizationRule** cria uma nova regra de autorização para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="53c13-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="53c13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53c13-107">EXAMPLES</span></span>

### <span data-ttu-id="53c13-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53c13-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="53c13-109">Cria uma regra de autorização `SBTopicAuthoRule1` com os direitos de **escuta** e **envio** para o tópico `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="53c13-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="53c13-110">OS</span><span class="sxs-lookup"><span data-stu-id="53c13-110">PARAMETERS</span></span>

### <span data-ttu-id="53c13-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="53c13-111">-ResourceGroup</span></span>
<span data-ttu-id="53c13-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53c13-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="53c13-113">-Direitos</span><span class="sxs-lookup"><span data-stu-id="53c13-113">-Rights</span></span>
<span data-ttu-id="53c13-114">Os direitos; por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="53c13-114">The rights; for example, @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="53c13-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53c13-115">-Confirm</span></span>
<span data-ttu-id="53c13-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c13-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c13-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c13-117">-WhatIf</span></span>
<span data-ttu-id="53c13-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53c13-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c13-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53c13-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c13-120">-DefaultProfile</span></span>
<span data-ttu-id="53c13-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53c13-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c13-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="53c13-122">-Name</span></span>
<span data-ttu-id="53c13-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="53c13-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="53c13-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="53c13-124">-Namespace</span></span>
<span data-ttu-id="53c13-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="53c13-125">Namespace Name.</span></span>

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

### <span data-ttu-id="53c13-126">-Tópico</span><span class="sxs-lookup"><span data-stu-id="53c13-126">-Topic</span></span>
<span data-ttu-id="53c13-127">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="53c13-127">Topic Name.</span></span>

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

### <span data-ttu-id="53c13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c13-128">CommonParameters</span></span>
<span data-ttu-id="53c13-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c13-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c13-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c13-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53c13-131">INPUTS</span></span>

### <span data-ttu-id="53c13-132">-Resource</span><span class="sxs-lookup"><span data-stu-id="53c13-132">-ResourceGroup</span></span>
 <span data-ttu-id="53c13-133">System. String</span><span class="sxs-lookup"><span data-stu-id="53c13-133">System.String</span></span>
 

### <span data-ttu-id="53c13-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="53c13-134">-NamespaceName</span></span>
 <span data-ttu-id="53c13-135">System. String</span><span class="sxs-lookup"><span data-stu-id="53c13-135">System.String</span></span>
 

### <span data-ttu-id="53c13-136">-Topicname</span><span class="sxs-lookup"><span data-stu-id="53c13-136">-TopicName</span></span>
 <span data-ttu-id="53c13-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53c13-137">System.String</span></span>
 

### <span data-ttu-id="53c13-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="53c13-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="53c13-139">System. String</span><span class="sxs-lookup"><span data-stu-id="53c13-139">System.String</span></span>

## <span data-ttu-id="53c13-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53c13-140">OUTPUTS</span></span>

### <span data-ttu-id="53c13-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="53c13-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="53c13-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onrules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="53c13-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="53c13-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53c13-143">NOTES</span></span>

## <span data-ttu-id="53c13-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53c13-144">RELATED LINKS</span></span>

