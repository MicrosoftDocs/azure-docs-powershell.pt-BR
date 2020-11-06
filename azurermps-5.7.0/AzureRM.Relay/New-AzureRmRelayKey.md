---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432916"
---
# <span data-ttu-id="6ffab-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="6ffab-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="6ffab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ffab-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffab-103">Regenera as cadeias de conexão primária ou secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="6ffab-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ffab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ffab-104">SYNTAX</span></span>

### <span data-ttu-id="6ffab-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ffab-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffab-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ffab-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffab-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ffab-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ffab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ffab-108">DESCRIPTION</span></span>
<span data-ttu-id="6ffab-109">O cmdlet **New-AzureRmRelayKey** gera as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6ffab-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6ffab-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ffab-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffab-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="6ffab-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="6ffab-112">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6ffab-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="6ffab-113">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6ffab-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="6ffab-114">Regenera as cadeias de conexão primária ou secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6ffab-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6ffab-115">OS</span><span class="sxs-lookup"><span data-stu-id="6ffab-115">PARAMETERS</span></span>

### <span data-ttu-id="6ffab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffab-116">-DefaultProfile</span></span>
<span data-ttu-id="6ffab-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ffab-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6ffab-118">-HybridConnection</span></span>
<span data-ttu-id="6ffab-119">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="6ffab-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="6ffab-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ffab-120">-Name</span></span>
<span data-ttu-id="6ffab-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="6ffab-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6ffab-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ffab-122">-Namespace</span></span>
<span data-ttu-id="6ffab-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="6ffab-123">Namespace Name.</span></span>

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

### <span data-ttu-id="6ffab-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6ffab-124">-RegenerateKey</span></span>
<span data-ttu-id="6ffab-125">Regenerar chaves-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="6ffab-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffab-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ffab-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ffab-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ffab-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6ffab-128">-WcfRelay</span></span>
<span data-ttu-id="6ffab-129">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6ffab-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6ffab-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ffab-130">-Confirm</span></span>
<span data-ttu-id="6ffab-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffab-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffab-132">-WhatIf</span></span>
<span data-ttu-id="6ffab-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ffab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ffab-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ffab-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ffab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffab-135">CommonParameters</span></span>
<span data-ttu-id="6ffab-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffab-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffab-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffab-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ffab-138">INPUTS</span></span>

### <span data-ttu-id="6ffab-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="6ffab-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="6ffab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-140">System.String</span></span> 

### <span data-ttu-id="6ffab-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6ffab-141">-NamespaceName</span></span>
 <span data-ttu-id="6ffab-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-142">System.String</span></span> 
 

### <span data-ttu-id="6ffab-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="6ffab-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="6ffab-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-144">System.String</span></span> 

### <span data-ttu-id="6ffab-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="6ffab-145">-WcfRelayName</span></span>
 <span data-ttu-id="6ffab-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-146">System.String</span></span> 

### <span data-ttu-id="6ffab-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ffab-147">-Name</span></span>
 <span data-ttu-id="6ffab-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-148">System.String</span></span>

### <span data-ttu-id="6ffab-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="6ffab-149">-RegenerateKeys</span></span>
 <span data-ttu-id="6ffab-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffab-150">System.String</span></span>

## <span data-ttu-id="6ffab-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ffab-151">OUTPUTS</span></span>

### <span data-ttu-id="6ffab-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6ffab-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="6ffab-153">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="6ffab-153">Example 1 - Namespace</span></span>
<span data-ttu-id="6ffab-154">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # = # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6ffab-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="6ffab-155">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6ffab-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="6ffab-156">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6ffab-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="6ffab-157">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6ffab-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="6ffab-158">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # = # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # Create# # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6ffab-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="6ffab-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ffab-159">NOTES</span></span>

## <span data-ttu-id="6ffab-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ffab-160">RELATED LINKS</span></span>

