---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440184"
---
# <span data-ttu-id="c6bf0-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c6bf0-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="c6bf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="c6bf0-103">Retorna a descrição da descrição da regra de autorização especificada para o tópico fornecido.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6bf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6bf0-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6bf0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="c6bf0-106">O cmdlet **Get-AzureRmServiceBusTopicAuthorizationRule** Obtém a descrição da regra de autorização especificada em um determinado tópico de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="c6bf0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="c6bf0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6bf0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="c6bf0-109">Retorna a descrição da regra de autorização especificada para o tópico fornecido.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="c6bf0-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="c6bf0-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="c6bf0-111">-ResourceGroup</span></span>
<span data-ttu-id="c6bf0-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6bf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bf0-113">-DefaultProfile</span></span>
<span data-ttu-id="c6bf0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6bf0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6bf0-115">-Name</span></span>
<span data-ttu-id="c6bf0-116">Nome do tópico AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c6bf0-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6bf0-117">-Namespace</span></span>
<span data-ttu-id="c6bf0-118">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-118">Namespace Name.</span></span>

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

### <span data-ttu-id="c6bf0-119">-Tópico</span><span class="sxs-lookup"><span data-stu-id="c6bf0-119">-Topic</span></span>
<span data-ttu-id="c6bf0-120">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-120">Topic Name.</span></span>

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

### <span data-ttu-id="c6bf0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bf0-121">CommonParameters</span></span>
<span data-ttu-id="c6bf0-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bf0-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6bf0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bf0-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6bf0-124">INPUTS</span></span>

### <span data-ttu-id="c6bf0-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="c6bf0-125">-ResourceGroup</span></span>
 <span data-ttu-id="c6bf0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf0-126">System.String</span></span>
 

### <span data-ttu-id="c6bf0-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c6bf0-127">-NamespaceName</span></span>
 <span data-ttu-id="c6bf0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf0-128">System.String</span></span>
 

### <span data-ttu-id="c6bf0-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="c6bf0-129">-TopicName</span></span>
 <span data-ttu-id="c6bf0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf0-130">System.String</span></span>
 

### <span data-ttu-id="c6bf0-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c6bf0-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="c6bf0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf0-132">System.String</span></span>

## <span data-ttu-id="c6bf0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6bf0-133">OUTPUTS</span></span>

### <span data-ttu-id="c6bf0-134">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c6bf0-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c6bf0-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onrules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: West US Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="c6bf0-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="c6bf0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6bf0-136">NOTES</span></span>

## <span data-ttu-id="c6bf0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6bf0-137">RELATED LINKS</span></span>

