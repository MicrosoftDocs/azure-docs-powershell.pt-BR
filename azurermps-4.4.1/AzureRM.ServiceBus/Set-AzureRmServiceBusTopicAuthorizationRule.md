---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610168"
---
# <span data-ttu-id="442b7-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="442b7-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="442b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="442b7-102">SYNOPSIS</span></span>
<span data-ttu-id="442b7-103">Atualiza a descrição da regra de autorização especificada para o tópico de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="442b7-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="442b7-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="442b7-105">DESCRIPTION</span></span>
<span data-ttu-id="442b7-106">O cmdlet **set-AzureRmServiceBusTopicAuthorizationRule** atualiza a descrição da regra de autorização especificada do tópico de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="442b7-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="442b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="442b7-107">EXAMPLES</span></span>

### <span data-ttu-id="442b7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="442b7-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="442b7-109">Adiciona **gerenciar** aos direitos de acesso da regra de autorização `SBTopicAuthoRule1` no tópico `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="442b7-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="442b7-110">OS</span><span class="sxs-lookup"><span data-stu-id="442b7-110">PARAMETERS</span></span>

### <span data-ttu-id="442b7-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="442b7-111">-ResourceGroup</span></span>
<span data-ttu-id="442b7-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="442b7-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="442b7-113">-Direitos</span><span class="sxs-lookup"><span data-stu-id="442b7-113">-Rights</span></span>
<span data-ttu-id="442b7-114">Direitos por exemplo, @ ("Listen", "enviar", "gerenciar").</span><span class="sxs-lookup"><span data-stu-id="442b7-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="442b7-115">Obrigatório se **-AuthruleObj** não for especificado.</span><span class="sxs-lookup"><span data-stu-id="442b7-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442b7-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="442b7-116">-Confirm</span></span>
<span data-ttu-id="442b7-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="442b7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442b7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442b7-118">-WhatIf</span></span>
<span data-ttu-id="442b7-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="442b7-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="442b7-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="442b7-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442b7-121">-DefaultProfile</span></span>
<span data-ttu-id="442b7-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="442b7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="442b7-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="442b7-123">-InputObj</span></span>
<span data-ttu-id="442b7-124">Objeto AuthorizationRule do tópico do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="442b7-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442b7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="442b7-125">-Name</span></span>
<span data-ttu-id="442b7-126">Nome do AuthorizationRule-necessário se ' AuthruleObj ' não especificado.</span><span class="sxs-lookup"><span data-stu-id="442b7-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="442b7-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="442b7-127">-Namespace</span></span>
<span data-ttu-id="442b7-128">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="442b7-128">Namespace Name.</span></span>

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

### <span data-ttu-id="442b7-129">-Tópico</span><span class="sxs-lookup"><span data-stu-id="442b7-129">-Topic</span></span>
<span data-ttu-id="442b7-130">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="442b7-130">Topic Name.</span></span>

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

### <span data-ttu-id="442b7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442b7-131">CommonParameters</span></span>
<span data-ttu-id="442b7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442b7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442b7-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442b7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442b7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="442b7-134">INPUTS</span></span>

### <span data-ttu-id="442b7-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="442b7-135">-ResourceGroup</span></span>
 <span data-ttu-id="442b7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="442b7-136">System.String</span></span>

### <span data-ttu-id="442b7-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="442b7-137">-NamespaceName</span></span>
 <span data-ttu-id="442b7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="442b7-138">System.String</span></span>

### <span data-ttu-id="442b7-139">-Topicname</span><span class="sxs-lookup"><span data-stu-id="442b7-139">-TopicName</span></span>
 <span data-ttu-id="442b7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="442b7-140">System.String</span></span>

### <span data-ttu-id="442b7-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="442b7-141">-AuthRuleObj</span></span>
 <span data-ttu-id="442b7-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="442b7-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="442b7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="442b7-143">OUTPUTS</span></span>

### <span data-ttu-id="442b7-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="442b7-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="442b7-145">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization de regras/SBTopicAuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 local: rótulos do oeste dos EUA: direitos: {Listen, enviar, gerenciar}</span><span class="sxs-lookup"><span data-stu-id="442b7-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="442b7-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="442b7-146">NOTES</span></span>

## <span data-ttu-id="442b7-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="442b7-147">RELATED LINKS</span></span>

