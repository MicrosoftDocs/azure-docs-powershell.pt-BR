---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610458"
---
# <span data-ttu-id="11499-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="11499-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="11499-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11499-102">SYNOPSIS</span></span>
<span data-ttu-id="11499-103">Atualiza a descrição da regra de autorização especificada para o namespace de barramento de serviço fornecido.</span><span class="sxs-lookup"><span data-stu-id="11499-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11499-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11499-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11499-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11499-105">DESCRIPTION</span></span>
<span data-ttu-id="11499-106">O cmdlet **set-AzureRmServiceBusNamespaceAuthorizationRule** atualiza a descrição da regra de autorização especificada no namespace de barramento do serviço específico.</span><span class="sxs-lookup"><span data-stu-id="11499-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="11499-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11499-107">EXAMPLES</span></span>

### <span data-ttu-id="11499-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11499-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="11499-109">Remove o **Gerenciamento** dos direitos de acesso da regra de autorização `AuthoRule1` no namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="11499-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="11499-110">OS</span><span class="sxs-lookup"><span data-stu-id="11499-110">PARAMETERS</span></span>

### <span data-ttu-id="11499-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="11499-111">-ResourceGroup</span></span>
<span data-ttu-id="11499-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11499-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="11499-113">-Direitos</span><span class="sxs-lookup"><span data-stu-id="11499-113">-Rights</span></span>
<span data-ttu-id="11499-114">Direitos por exemplo, @ ("Listen", "enviar", "gerenciar").</span><span class="sxs-lookup"><span data-stu-id="11499-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="11499-115">Obrigatório se **AuthruleObj** não for especificado.</span><span class="sxs-lookup"><span data-stu-id="11499-115">Required if **AuthruleObj** is not specified.</span></span>

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

### <span data-ttu-id="11499-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11499-116">-Confirm</span></span>
<span data-ttu-id="11499-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11499-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11499-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11499-118">-WhatIf</span></span>
<span data-ttu-id="11499-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11499-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11499-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11499-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11499-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11499-121">-DefaultProfile</span></span>
<span data-ttu-id="11499-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11499-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11499-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="11499-123">-InputObj</span></span>
<span data-ttu-id="11499-124">NameSpace do ServiceBus objeto AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="11499-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="11499-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="11499-125">-Name</span></span>
<span data-ttu-id="11499-126">Nome do AuthorizationRule-necessário se ' AuthruleObj ' não especificado.</span><span class="sxs-lookup"><span data-stu-id="11499-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="11499-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11499-127">-Namespace</span></span>
<span data-ttu-id="11499-128">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="11499-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="11499-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11499-129">CommonParameters</span></span>
<span data-ttu-id="11499-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11499-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11499-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11499-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11499-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11499-132">INPUTS</span></span>

### <span data-ttu-id="11499-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="11499-133">-ResourceGroup</span></span>
 <span data-ttu-id="11499-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11499-134">System.String</span></span>

### <span data-ttu-id="11499-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="11499-135">-NamespaceName</span></span>
 <span data-ttu-id="11499-136">System. String</span><span class="sxs-lookup"><span data-stu-id="11499-136">System.String</span></span>

### <span data-ttu-id="11499-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="11499-137">-AuthRuleObj</span></span>
 <span data-ttu-id="11499-138">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="11499-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="11499-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11499-139">OUTPUTS</span></span>

### <span data-ttu-id="11499-140">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="11499-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="11499-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="11499-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="11499-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11499-142">NOTES</span></span>

## <span data-ttu-id="11499-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11499-143">RELATED LINKS</span></span>

