---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433165"
---
# <span data-ttu-id="785d1-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="785d1-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="785d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="785d1-102">SYNOPSIS</span></span>
<span data-ttu-id="785d1-103">Obtém as cadeias de conexão primária e secundária para o namespace ou a fila ou tópico ou o alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="785d1-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="785d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="785d1-104">SYNTAX</span></span>

### <span data-ttu-id="785d1-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="785d1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="785d1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="785d1-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="785d1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="785d1-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="785d1-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="785d1-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785d1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="785d1-109">DESCRIPTION</span></span>
<span data-ttu-id="785d1-110">O cmdlet **Get-AzServiceBusKey** retorna as cadeias de conexão primária e secundária para o namespace ou fila ou tópico ou alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="785d1-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="785d1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="785d1-111">EXAMPLES</span></span>

### <span data-ttu-id="785d1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="785d1-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="785d1-113">Cadeia de conexão primária e secundária para o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="785d1-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="785d1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="785d1-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="785d1-115">Cadeia de conexão primária e secundária para a fila especificada.</span><span class="sxs-lookup"><span data-stu-id="785d1-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="785d1-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="785d1-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="785d1-117">Cadeia de conexão primária e secundária para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="785d1-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="785d1-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="785d1-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="785d1-119">Cadeia de conexão primária e secundária para o namespace e o alias especificados.</span><span class="sxs-lookup"><span data-stu-id="785d1-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="785d1-120">OS</span><span class="sxs-lookup"><span data-stu-id="785d1-120">PARAMETERS</span></span>

### <span data-ttu-id="785d1-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="785d1-121">-AliasName</span></span>
<span data-ttu-id="785d1-122">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="785d1-122">Alias Name</span></span>

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

### <span data-ttu-id="785d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785d1-123">-DefaultProfile</span></span>
<span data-ttu-id="785d1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="785d1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="785d1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="785d1-125">-Name</span></span>
<span data-ttu-id="785d1-126">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="785d1-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785d1-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="785d1-127">-Namespace</span></span>
<span data-ttu-id="785d1-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="785d1-128">Namespace Name</span></span>

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

### <span data-ttu-id="785d1-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="785d1-129">-Queue</span></span>
<span data-ttu-id="785d1-130">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="785d1-130">Queue Name</span></span>

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

### <span data-ttu-id="785d1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785d1-131">-ResourceGroupName</span></span>
<span data-ttu-id="785d1-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="785d1-132">Resource Group Name</span></span>

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

### <span data-ttu-id="785d1-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="785d1-133">-Topic</span></span>
<span data-ttu-id="785d1-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="785d1-134">Topic Name</span></span>

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

### <span data-ttu-id="785d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785d1-135">CommonParameters</span></span>
<span data-ttu-id="785d1-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785d1-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785d1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785d1-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="785d1-138">INPUTS</span></span>

### <span data-ttu-id="785d1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="785d1-139">System.String</span></span>

## <span data-ttu-id="785d1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="785d1-140">OUTPUTS</span></span>

### <span data-ttu-id="785d1-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="785d1-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="785d1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="785d1-142">NOTES</span></span>

## <span data-ttu-id="785d1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="785d1-143">RELATED LINKS</span></span>
