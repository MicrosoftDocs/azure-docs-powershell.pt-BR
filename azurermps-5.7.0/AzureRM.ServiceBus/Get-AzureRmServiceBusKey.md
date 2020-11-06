---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: da2794fc390ecce13c466fc4ff2d2efb92205a8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428765"
---
# <span data-ttu-id="bdcc9-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="bdcc9-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="bdcc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcc9-103">Obtém as cadeias de conexão primária e secundária para o namespace ou a fila ou tópico ou o alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdcc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdcc9-104">SYNTAX</span></span>

### <span data-ttu-id="bdcc9-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdcc9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdcc9-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdcc9-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdcc9-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdcc9-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdcc9-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdcc9-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdcc9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdcc9-109">DESCRIPTION</span></span>
<span data-ttu-id="bdcc9-110">O cmdlet **Get-AzureRmServiceBusKey** retorna as cadeias de conexão primária e secundária para o namespace ou fila ou tópico ou alias (configurações de GeoDR) fornecido.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="bdcc9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdcc9-111">EXAMPLES</span></span>

### <span data-ttu-id="bdcc9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdcc9-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="bdcc9-113">Cadeia de conexão primária e secundária para o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="bdcc9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bdcc9-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="bdcc9-115">Cadeia de conexão primária e secundária para a fila especificada.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="bdcc9-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bdcc9-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="bdcc9-117">Cadeia de conexão primária e secundária para o tópico especificado.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="bdcc9-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bdcc9-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="bdcc9-119">Cadeia de conexão primária e secundária para o namespace e o alias especificados.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="bdcc9-120">OS</span><span class="sxs-lookup"><span data-stu-id="bdcc9-120">PARAMETERS</span></span>

### <span data-ttu-id="bdcc9-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="bdcc9-121">-AliasName</span></span>
<span data-ttu-id="bdcc9-122">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="bdcc9-122">Alias Name</span></span>

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

### <span data-ttu-id="bdcc9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcc9-123">-DefaultProfile</span></span>
<span data-ttu-id="bdcc9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdcc9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdcc9-125">-Name</span></span>
<span data-ttu-id="bdcc9-126">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdcc9-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcc9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bdcc9-127">-Namespace</span></span>
<span data-ttu-id="bdcc9-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="bdcc9-128">Namespace Name</span></span>

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

### <span data-ttu-id="bdcc9-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="bdcc9-129">-Queue</span></span>
<span data-ttu-id="bdcc9-130">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="bdcc9-130">Queue Name</span></span>

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

### <span data-ttu-id="bdcc9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcc9-131">-ResourceGroupName</span></span>
<span data-ttu-id="bdcc9-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bdcc9-132">Resource Group Name</span></span>

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

### <span data-ttu-id="bdcc9-133">-Tópico</span><span class="sxs-lookup"><span data-stu-id="bdcc9-133">-Topic</span></span>
<span data-ttu-id="bdcc9-134">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="bdcc9-134">Topic Name</span></span>

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

### <span data-ttu-id="bdcc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcc9-135">CommonParameters</span></span>
<span data-ttu-id="bdcc9-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bdcc9-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdcc9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcc9-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdcc9-138">INPUTS</span></span>

### <span data-ttu-id="bdcc9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bdcc9-139">System.String</span></span>


## <span data-ttu-id="bdcc9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdcc9-140">OUTPUTS</span></span>

### <span data-ttu-id="bdcc9-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="bdcc9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="bdcc9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdcc9-142">NOTES</span></span>

## <span data-ttu-id="bdcc9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdcc9-143">RELATED LINKS</span></span>
