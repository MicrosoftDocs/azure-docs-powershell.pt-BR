---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427452"
---
# <span data-ttu-id="add54-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="add54-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="add54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="add54-102">SYNOPSIS</span></span>
<span data-ttu-id="add54-103">Obtém as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="add54-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="add54-104">SYNTAX</span></span>

### <span data-ttu-id="add54-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="add54-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add54-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="add54-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add54-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="add54-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add54-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="add54-108">DESCRIPTION</span></span>
<span data-ttu-id="add54-109">O cmdlet **Get-AzureRmRelayKey** retorna as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="add54-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="add54-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="add54-110">EXAMPLES</span></span>

### <span data-ttu-id="add54-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="add54-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="add54-112">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="add54-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="add54-113">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="add54-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="add54-114">Cadeia de conexão primária e secundária para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="add54-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="add54-115">OS</span><span class="sxs-lookup"><span data-stu-id="add54-115">PARAMETERS</span></span>

### <span data-ttu-id="add54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add54-116">-DefaultProfile</span></span>
<span data-ttu-id="add54-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="add54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add54-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="add54-118">-HybridConnection</span></span>
<span data-ttu-id="add54-119">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="add54-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add54-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="add54-120">-Name</span></span>
<span data-ttu-id="add54-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="add54-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add54-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="add54-122">-Namespace</span></span>
<span data-ttu-id="add54-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="add54-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add54-124">-ResourceGroupName</span></span>
<span data-ttu-id="add54-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="add54-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="add54-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="add54-126">-WcfRelay</span></span>
<span data-ttu-id="add54-127">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="add54-127">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add54-128">CommonParameters</span></span>
<span data-ttu-id="add54-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add54-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add54-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add54-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="add54-131">INPUTS</span></span>

### <span data-ttu-id="add54-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add54-132">-ResourceGroupName</span></span>
 <span data-ttu-id="add54-133">System. String</span><span class="sxs-lookup"><span data-stu-id="add54-133">System.String</span></span> 

### <span data-ttu-id="add54-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="add54-134">-NamespaceName</span></span>
 <span data-ttu-id="add54-135">System. String</span><span class="sxs-lookup"><span data-stu-id="add54-135">System.String</span></span> 
 

### <span data-ttu-id="add54-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="add54-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="add54-137">System. String</span><span class="sxs-lookup"><span data-stu-id="add54-137">System.String</span></span> 

### <span data-ttu-id="add54-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="add54-138">-WcfRelayName</span></span>
 <span data-ttu-id="add54-139">System. String</span><span class="sxs-lookup"><span data-stu-id="add54-139">System.String</span></span> 

### <span data-ttu-id="add54-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="add54-140">-Name</span></span>
 <span data-ttu-id="add54-141">System. String</span><span class="sxs-lookup"><span data-stu-id="add54-141">System.String</span></span>

## <span data-ttu-id="add54-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="add54-142">OUTPUTS</span></span>

### <span data-ttu-id="add54-143">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="add54-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="add54-144">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="add54-144">Example 1 - Namespace</span></span>
<span data-ttu-id="add54-145">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # = # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="add54-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="add54-146">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="add54-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="add54-147">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="add54-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="add54-148">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="add54-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="add54-149">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="add54-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="add54-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="add54-150">NOTES</span></span>

## <span data-ttu-id="add54-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="add54-151">RELATED LINKS</span></span>

