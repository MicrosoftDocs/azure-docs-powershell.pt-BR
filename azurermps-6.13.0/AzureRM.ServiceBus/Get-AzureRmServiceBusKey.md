---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427159"
---
# <span data-ttu-id="5a5a3-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="5a5a3-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="5a5a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5a3-103">Obtém as cadeias de conexão primária e secundária para o namespace ou a fila ou tópico ou o alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a5a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a5a3-104">SYNTAX</span></span>

### <span data-ttu-id="5a5a3-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a5a3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a5a3-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a5a3-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a5a3-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a5a3-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a5a3-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a5a3-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a5a3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a5a3-109">DESCRIPTION</span></span>
<span data-ttu-id="5a5a3-110">O cmdlet **Get-AzureRmServiceBusKey** retorna as cadeias de conexão primária e secundária para o namespace ou fila ou tópico ou alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="5a5a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a5a3-111">EXAMPLES</span></span>

### <span data-ttu-id="5a5a3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a5a3-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="5a5a3-113">Cadeia de conexão primária e secundária para o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="5a5a3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a5a3-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="5a5a3-115">Cadeia de conexão primária e secundária para a fila especificada.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="5a5a3-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5a5a3-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="5a5a3-117">Cadeia de conexão primária e secundária para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="5a5a3-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5a5a3-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="5a5a3-119">Cadeia de conexão primária e secundária para o namespace e o alias especificados.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="5a5a3-120">OS</span><span class="sxs-lookup"><span data-stu-id="5a5a3-120">PARAMETERS</span></span>

### <span data-ttu-id="5a5a3-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="5a5a3-121">-AliasName</span></span>
<span data-ttu-id="5a5a3-122">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="5a5a3-122">Alias Name</span></span>

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

### <span data-ttu-id="5a5a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5a3-123">-DefaultProfile</span></span>
<span data-ttu-id="5a5a3-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a5a3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a5a3-125">-Name</span></span>
<span data-ttu-id="5a5a3-126">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5a5a3-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5a5a3-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a5a3-127">-Namespace</span></span>
<span data-ttu-id="5a5a3-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="5a5a3-128">Namespace Name</span></span>

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

### <span data-ttu-id="5a5a3-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="5a5a3-129">-Queue</span></span>
<span data-ttu-id="5a5a3-130">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="5a5a3-130">Queue Name</span></span>

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

### <span data-ttu-id="5a5a3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5a3-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a5a3-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5a5a3-132">Resource Group Name</span></span>

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

### <span data-ttu-id="5a5a3-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="5a5a3-133">-Topic</span></span>
<span data-ttu-id="5a5a3-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="5a5a3-134">Topic Name</span></span>

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

### <span data-ttu-id="5a5a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5a3-135">CommonParameters</span></span>
<span data-ttu-id="5a5a3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a5a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5a3-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a5a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5a3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a5a3-138">INPUTS</span></span>

### <span data-ttu-id="5a5a3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a5a3-139">System.String</span></span>

## <span data-ttu-id="5a5a3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a5a3-140">OUTPUTS</span></span>

### <span data-ttu-id="5a5a3-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5a5a3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="5a5a3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a5a3-142">NOTES</span></span>

## <span data-ttu-id="5a5a3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a5a3-143">RELATED LINKS</span></span>
