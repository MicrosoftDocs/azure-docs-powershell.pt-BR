---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117138"
---
# <span data-ttu-id="23b34-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23b34-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="23b34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23b34-102">SYNOPSIS</span></span>
<span data-ttu-id="23b34-103">Obtém uma descrição da regra de autorização especificada para um determinado Namespace ou Fila ou Tópico ou Alias (Configurações geodr).</span><span class="sxs-lookup"><span data-stu-id="23b34-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="23b34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b34-104">SYNTAX</span></span>

### <span data-ttu-id="23b34-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23b34-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23b34-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23b34-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23b34-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23b34-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23b34-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="23b34-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23b34-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="23b34-109">DESCRIPTION</span></span>
<span data-ttu-id="23b34-110">O cmdlet **Get-AzServiceBusAuthorizationRule** obtém a descrição da regra de autorização especificada no namespace ou fila ou tópico ou alias (configurações geodr).</span><span class="sxs-lookup"><span data-stu-id="23b34-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="23b34-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23b34-111">EXAMPLES</span></span>

### <span data-ttu-id="23b34-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23b34-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="23b34-113">Retorna a descrição da regra de autorização especificada para um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="23b34-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="23b34-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="23b34-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="23b34-115">Retorna a descrição da regra de autorização especificada para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="23b34-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="23b34-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="23b34-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="23b34-117">Retorna a descrição da regra de autorização especificada para um tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="23b34-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="23b34-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="23b34-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="23b34-119">Retorna a descrição da regra de autorização especificada para um namespace e alias especificados.</span><span class="sxs-lookup"><span data-stu-id="23b34-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="23b34-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b34-120">PARAMETERS</span></span>

### <span data-ttu-id="23b34-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="23b34-121">-AliasName</span></span>
<span data-ttu-id="23b34-122">Nome da configuração geodr</span><span class="sxs-lookup"><span data-stu-id="23b34-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="23b34-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b34-123">-DefaultProfile</span></span>
<span data-ttu-id="23b34-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23b34-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b34-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="23b34-125">-Name</span></span>
<span data-ttu-id="23b34-126">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23b34-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="23b34-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23b34-127">-Namespace</span></span>
<span data-ttu-id="23b34-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="23b34-128">Namespace Name</span></span>

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

### <span data-ttu-id="23b34-129">-Fila</span><span class="sxs-lookup"><span data-stu-id="23b34-129">-Queue</span></span>
<span data-ttu-id="23b34-130">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="23b34-130">Queue Name</span></span>

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

### <span data-ttu-id="23b34-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b34-131">-ResourceGroupName</span></span>
<span data-ttu-id="23b34-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="23b34-132">Resource Group Name</span></span>

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

### <span data-ttu-id="23b34-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="23b34-133">-Topic</span></span>
<span data-ttu-id="23b34-134">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="23b34-134">Topic Name</span></span>

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

### <span data-ttu-id="23b34-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b34-135">CommonParameters</span></span>
<span data-ttu-id="23b34-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b34-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b34-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b34-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b34-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="23b34-138">INPUTS</span></span>

### <span data-ttu-id="23b34-139">System.String</span><span class="sxs-lookup"><span data-stu-id="23b34-139">System.String</span></span>

## <span data-ttu-id="23b34-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="23b34-140">OUTPUTS</span></span>

### <span data-ttu-id="23b34-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="23b34-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="23b34-142">Notas</span><span class="sxs-lookup"><span data-stu-id="23b34-142">NOTES</span></span>

## <span data-ttu-id="23b34-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23b34-143">RELATED LINKS</span></span>
