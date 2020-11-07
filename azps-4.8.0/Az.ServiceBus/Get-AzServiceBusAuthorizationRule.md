---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954682"
---
# <span data-ttu-id="c3ad5-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3ad5-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="c3ad5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ad5-103">Obtém uma descrição da regra de autorização especificada para um determinado namespace ou fila ou tópico ou alias (configurações de GeoDR).</span><span class="sxs-lookup"><span data-stu-id="c3ad5-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="c3ad5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3ad5-104">SYNTAX</span></span>

### <span data-ttu-id="c3ad5-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3ad5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3ad5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3ad5-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3ad5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3ad5-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3ad5-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3ad5-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3ad5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3ad5-109">DESCRIPTION</span></span>
<span data-ttu-id="c3ad5-110">O cmdlet **Get-AzServiceBusAuthorizationRule** Obtém a descrição da regra de autorização especificada no namespace ou na fila ou tópico ou alias (configurações de GeoDR) determinado.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="c3ad5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3ad5-111">EXAMPLES</span></span>

### <span data-ttu-id="c3ad5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3ad5-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="c3ad5-113">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="c3ad5-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3ad5-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="c3ad5-115">Retorna a descrição da regra de autorização especificada para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="c3ad5-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c3ad5-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="c3ad5-117">Retorna a descrição da regra de autorização especificada para um tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="c3ad5-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c3ad5-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="c3ad5-119">Retorna a descrição da regra de autorização especificada para um namespace e um alias especificado.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="c3ad5-120">OS</span><span class="sxs-lookup"><span data-stu-id="c3ad5-120">PARAMETERS</span></span>

### <span data-ttu-id="c3ad5-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="c3ad5-121">-AliasName</span></span>
<span data-ttu-id="c3ad5-122">Nome de configuração do GeoDR</span><span class="sxs-lookup"><span data-stu-id="c3ad5-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ad5-123">-DefaultProfile</span></span>
<span data-ttu-id="c3ad5-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3ad5-125">-Name</span></span>
<span data-ttu-id="c3ad5-126">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3ad5-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3ad5-127">-Namespace</span></span>
<span data-ttu-id="c3ad5-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="c3ad5-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="c3ad5-129">-Queue</span></span>
<span data-ttu-id="c3ad5-130">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="c3ad5-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ad5-131">-ResourceGroupName</span></span>
<span data-ttu-id="c3ad5-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c3ad5-132">Resource Group Name</span></span>

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

### <span data-ttu-id="c3ad5-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="c3ad5-133">-Topic</span></span>
<span data-ttu-id="c3ad5-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="c3ad5-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ad5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ad5-135">CommonParameters</span></span>
<span data-ttu-id="c3ad5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ad5-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ad5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ad5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3ad5-138">INPUTS</span></span>

### <span data-ttu-id="c3ad5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c3ad5-139">System.String</span></span>

## <span data-ttu-id="c3ad5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3ad5-140">OUTPUTS</span></span>

### <span data-ttu-id="c3ad5-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c3ad5-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c3ad5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3ad5-142">NOTES</span></span>

## <span data-ttu-id="c3ad5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3ad5-143">RELATED LINKS</span></span>
