---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428769"
---
# <span data-ttu-id="fa447-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa447-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fa447-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa447-102">SYNOPSIS</span></span>
<span data-ttu-id="fa447-103">Obtém uma descrição da regra de autorização especificada para um determinado namespace ou fila ou tópico ou alias (configurações de GeoDR).</span><span class="sxs-lookup"><span data-stu-id="fa447-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa447-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa447-104">SYNTAX</span></span>

### <span data-ttu-id="fa447-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa447-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa447-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa447-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa447-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa447-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa447-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa447-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa447-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa447-109">DESCRIPTION</span></span>
<span data-ttu-id="fa447-110">O cmdlet **Get-AzureRmServiceBusAuthorizationRule** Obtém a descrição da regra de autorização especificada no namespace ou na fila ou tópico ou alias (configurações de GeoDR) determinado.</span><span class="sxs-lookup"><span data-stu-id="fa447-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="fa447-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa447-111">EXAMPLES</span></span>

### <span data-ttu-id="fa447-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa447-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="fa447-113">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="fa447-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="fa447-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fa447-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="fa447-115">Retorna a descrição da regra de autorização especificada para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="fa447-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="fa447-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fa447-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="fa447-117">Retorna a descrição da regra de autorização especificada para um tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="fa447-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="fa447-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fa447-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="fa447-119">Retorna a descrição da regra de autorização especificada para um namespace e um alias especificado.</span><span class="sxs-lookup"><span data-stu-id="fa447-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="fa447-120">OS</span><span class="sxs-lookup"><span data-stu-id="fa447-120">PARAMETERS</span></span>

### <span data-ttu-id="fa447-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="fa447-121">-AliasName</span></span>
<span data-ttu-id="fa447-122">Nome de configuração do GeoDR</span><span class="sxs-lookup"><span data-stu-id="fa447-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa447-123">-DefaultProfile</span></span>
<span data-ttu-id="fa447-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa447-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa447-125">-Name</span></span>
<span data-ttu-id="fa447-126">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa447-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa447-127">-Namespace</span></span>
<span data-ttu-id="fa447-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="fa447-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="fa447-129">-Queue</span></span>
<span data-ttu-id="fa447-130">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="fa447-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa447-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa447-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fa447-132">Resource Group Name</span></span>

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

### <span data-ttu-id="fa447-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="fa447-133">-Topic</span></span>
<span data-ttu-id="fa447-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="fa447-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa447-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa447-135">CommonParameters</span></span>
<span data-ttu-id="fa447-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa447-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa447-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa447-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa447-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa447-138">INPUTS</span></span>

### <span data-ttu-id="fa447-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa447-139">System.String</span></span>


## <span data-ttu-id="fa447-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa447-140">OUTPUTS</span></span>

### <span data-ttu-id="fa447-141">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fa447-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="fa447-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa447-142">NOTES</span></span>

## <span data-ttu-id="fa447-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa447-143">RELATED LINKS</span></span>
