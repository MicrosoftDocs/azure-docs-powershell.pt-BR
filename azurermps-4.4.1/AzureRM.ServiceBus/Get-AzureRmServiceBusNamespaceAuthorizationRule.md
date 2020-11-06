---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430630"
---
# <span data-ttu-id="b97fd-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b97fd-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b97fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b97fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b97fd-103">Obtém uma descrição da regra de autorização especificada para um determinado namespace.</span><span class="sxs-lookup"><span data-stu-id="b97fd-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b97fd-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b97fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b97fd-106">O cmdlet **Get-AzureRmServiceBusNamespaceAuthorizationRule** Obtém a descrição da regra de autorização especificada no namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="b97fd-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="b97fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b97fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b97fd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b97fd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="b97fd-109">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="b97fd-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="b97fd-110">OS</span><span class="sxs-lookup"><span data-stu-id="b97fd-110">PARAMETERS</span></span>

### <span data-ttu-id="b97fd-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="b97fd-111">-ResourceGroup</span></span>
<span data-ttu-id="b97fd-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b97fd-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b97fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97fd-113">-DefaultProfile</span></span>
<span data-ttu-id="b97fd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b97fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b97fd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b97fd-115">-Name</span></span>
<span data-ttu-id="b97fd-116">Nome do namespace do ServiceBus AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b97fd-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b97fd-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b97fd-117">-Namespace</span></span>
<span data-ttu-id="b97fd-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="b97fd-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="b97fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97fd-119">CommonParameters</span></span>
<span data-ttu-id="b97fd-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97fd-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97fd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97fd-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b97fd-122">INPUTS</span></span>

### <span data-ttu-id="b97fd-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="b97fd-123">-ResourceGroup</span></span>
 <span data-ttu-id="b97fd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b97fd-124">System.String</span></span>
 

### <span data-ttu-id="b97fd-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b97fd-125">-NamespaceName</span></span>
 <span data-ttu-id="b97fd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b97fd-126">System.String</span></span>
 

### <span data-ttu-id="b97fd-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b97fd-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b97fd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b97fd-128">System.String</span></span>

## <span data-ttu-id="b97fd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b97fd-129">OUTPUTS</span></span>

### <span data-ttu-id="b97fd-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b97fd-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b97fd-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="b97fd-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="b97fd-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b97fd-132">NOTES</span></span>

## <span data-ttu-id="b97fd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b97fd-133">RELATED LINKS</span></span>

