---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 39f43af6685f754cacfd1340560fd4c3429f792d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886596"
---
# <span data-ttu-id="2e19e-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e19e-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2e19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e19e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e19e-103">Obtém uma descrição da regra de autorização especificada para um determinado Namespace ou Queue ou Topic ou Alias (Configurações GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2e19e-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="2e19e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e19e-104">SYNTAX</span></span>

### <span data-ttu-id="2e19e-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e19e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e19e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e19e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e19e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e19e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e19e-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e19e-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e19e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e19e-109">DESCRIPTION</span></span>
<span data-ttu-id="2e19e-110">O cmdlet **Get-AzServiceBusAuthorizationRule** obtém a descrição da regra de autorização especificada no Namespace ou Queue ou Topic ou Alias (Configurações GeoDR).</span><span class="sxs-lookup"><span data-stu-id="2e19e-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="2e19e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e19e-111">EXAMPLES</span></span>

### <span data-ttu-id="2e19e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e19e-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="2e19e-113">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="2e19e-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="2e19e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e19e-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="2e19e-115">Retorna a descrição da regra de autorização especificada para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="2e19e-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="2e19e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2e19e-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="2e19e-117">Retorna a descrição da regra de autorização especificada para um tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="2e19e-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="2e19e-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="2e19e-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="2e19e-119">Retorna a descrição da regra de autorização especificada para um namespace e alias especificados.</span><span class="sxs-lookup"><span data-stu-id="2e19e-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="2e19e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e19e-120">PARAMETERS</span></span>

### <span data-ttu-id="2e19e-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2e19e-121">-AliasName</span></span>
<span data-ttu-id="2e19e-122">Nome da Configuração GeoDR</span><span class="sxs-lookup"><span data-stu-id="2e19e-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="2e19e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e19e-123">-DefaultProfile</span></span>
<span data-ttu-id="2e19e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e19e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e19e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2e19e-125">-Name</span></span>
<span data-ttu-id="2e19e-126">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e19e-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2e19e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e19e-127">-Namespace</span></span>
<span data-ttu-id="2e19e-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2e19e-128">Namespace Name</span></span>

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

### <span data-ttu-id="2e19e-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="2e19e-129">-Queue</span></span>
<span data-ttu-id="2e19e-130">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="2e19e-130">Queue Name</span></span>

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

### <span data-ttu-id="2e19e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e19e-131">-ResourceGroupName</span></span>
<span data-ttu-id="2e19e-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2e19e-132">Resource Group Name</span></span>

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

### <span data-ttu-id="2e19e-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="2e19e-133">-Topic</span></span>
<span data-ttu-id="2e19e-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="2e19e-134">Topic Name</span></span>

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

### <span data-ttu-id="2e19e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e19e-135">CommonParameters</span></span>
<span data-ttu-id="2e19e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e19e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e19e-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e19e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e19e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e19e-138">INPUTS</span></span>

### <span data-ttu-id="2e19e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2e19e-139">System.String</span></span>

## <span data-ttu-id="2e19e-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e19e-140">OUTPUTS</span></span>

### <span data-ttu-id="2e19e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2e19e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2e19e-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e19e-142">NOTES</span></span>

## <span data-ttu-id="2e19e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e19e-143">RELATED LINKS</span></span>
