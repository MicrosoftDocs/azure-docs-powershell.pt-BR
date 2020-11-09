---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283814"
---
# <span data-ttu-id="6b2ae-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="6b2ae-101">New-AzRelayKey</span></span>

## <span data-ttu-id="6b2ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2ae-103">Regenera as cadeias de conexão primária ou secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="6b2ae-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="6b2ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b2ae-104">SYNTAX</span></span>

### <span data-ttu-id="6b2ae-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b2ae-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b2ae-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b2ae-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b2ae-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b2ae-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b2ae-108">DESCRIPTION</span></span>
<span data-ttu-id="6b2ae-109">O cmdlet **New-AzRelayKey** gera as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6b2ae-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6b2ae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="6b2ae-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="6b2ae-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-112">Regenera as cadeias de conexão primária ou secundária para a entidade Relay-Namespace específica.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="6b2ae-113">Exemplo 1,1-valor de namespace fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-114">gera as cadeias de conexão primária ou secundária para a entidade Relay-Namespace especificada com o valor de chave fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="6b2ae-115">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6b2ae-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-116">Regenera as cadeias de conexão primária ou secundária para a entidade Relay-WcfRelay específica.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="6b2ae-117">Exemplo 2,1-valor WcfRelay fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-118">gera as cadeias de conexão primária ou secundária para a entidade Relay-WcfRelay especificada com o valor de chave fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="6b2ae-119">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6b2ae-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-120">Regenera as cadeias de conexão primária ou secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6b2ae-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="6b2ae-121">Exemplo 3,1-valor HybridConnection fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="6b2ae-122">gera as cadeias de conexão primária ou secundária para a entidade Relay-HybridConnection especificada com o valor de chave fornecido</span><span class="sxs-lookup"><span data-stu-id="6b2ae-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="6b2ae-123">OS</span><span class="sxs-lookup"><span data-stu-id="6b2ae-123">PARAMETERS</span></span>

### <span data-ttu-id="6b2ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2ae-124">-DefaultProfile</span></span>
<span data-ttu-id="6b2ae-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b2ae-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6b2ae-126">-HybridConnection</span></span>
<span data-ttu-id="6b2ae-127">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-127">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="6b2ae-128">-KeyValue</span></span>
<span data-ttu-id="6b2ae-129">Uma chave de 256 bits codificada em base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b2ae-130">-Name</span></span>
<span data-ttu-id="6b2ae-131">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-131">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6b2ae-132">-Namespace</span></span>
<span data-ttu-id="6b2ae-133">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6b2ae-134">-RegenerateKey</span></span>
<span data-ttu-id="6b2ae-135">Regenerar chaves-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2ae-136">-ResourceGroupName</span></span>
<span data-ttu-id="6b2ae-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="6b2ae-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6b2ae-138">-WcfRelay</span></span>
<span data-ttu-id="6b2ae-139">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-139">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b2ae-140">-Confirm</span></span>
<span data-ttu-id="6b2ae-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2ae-142">-WhatIf</span></span>
<span data-ttu-id="6b2ae-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2ae-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2ae-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2ae-145">CommonParameters</span></span>
<span data-ttu-id="6b2ae-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2ae-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2ae-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2ae-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2ae-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b2ae-148">INPUTS</span></span>

### <span data-ttu-id="6b2ae-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6b2ae-149">System.String</span></span>

## <span data-ttu-id="6b2ae-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b2ae-150">OUTPUTS</span></span>

### <span data-ttu-id="6b2ae-151">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6b2ae-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="6b2ae-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b2ae-152">NOTES</span></span>

## <span data-ttu-id="6b2ae-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b2ae-153">RELATED LINKS</span></span>
