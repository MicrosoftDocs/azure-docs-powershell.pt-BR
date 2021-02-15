---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118783"
---
# <span data-ttu-id="0b89e-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="0b89e-101">New-AzRelayKey</span></span>

## <span data-ttu-id="0b89e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b89e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b89e-103">Regenera as cadeias de conexão primárias ou secundárias para as entidades de Retransmissão determinadas (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="0b89e-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="0b89e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b89e-104">SYNTAX</span></span>

### <span data-ttu-id="0b89e-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b89e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b89e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b89e-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b89e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b89e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b89e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b89e-108">DESCRIPTION</span></span>
<span data-ttu-id="0b89e-109">O cmdlet **New-AzRelayKey** gera as cadeias de conexão primárias e secundárias para as entidades de Retransmissão determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="0b89e-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="0b89e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b89e-110">EXAMPLES</span></span>

### <span data-ttu-id="0b89e-111">Exemplo 1 - Namespace</span><span class="sxs-lookup"><span data-stu-id="0b89e-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-112">Regenera as cadeias de conexão primárias ou secundárias para a entidade Relay-Namespace determinada.</span><span class="sxs-lookup"><span data-stu-id="0b89e-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="0b89e-113">Exemplo 1.1 - Namespace KeyValue Fornecido</span><span class="sxs-lookup"><span data-stu-id="0b89e-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-114">gera as cadeias de conexão primárias ou secundárias para a entidade Relay-Namespace com o Valor de Chave Fornecido</span><span class="sxs-lookup"><span data-stu-id="0b89e-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="0b89e-115">Exemplo 2 - WcfRelay</span><span class="sxs-lookup"><span data-stu-id="0b89e-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-116">Regenera as cadeias de conexão primárias ou secundárias para a entidade Relay-WcfRelay determinada.</span><span class="sxs-lookup"><span data-stu-id="0b89e-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="0b89e-117">Exemplo 2.1 - WcfRelay KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="0b89e-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-118">gera as cadeias de conexão primárias ou secundárias para a entidade Relay-WcfRelay com o Valor de Chave Fornecido</span><span class="sxs-lookup"><span data-stu-id="0b89e-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="0b89e-119">Exemplo 3 - HybridConnection</span><span class="sxs-lookup"><span data-stu-id="0b89e-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-120">Regenera as cadeias de conexão primárias ou secundárias para as entidades de Retransmissão determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="0b89e-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="0b89e-121">Exemplo 3.1 - HybridConnection KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="0b89e-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="0b89e-122">gera as cadeias de conexão primárias ou secundárias para a entidade Relay-HybridConnection com o Valor de Chave Fornecido</span><span class="sxs-lookup"><span data-stu-id="0b89e-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="0b89e-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b89e-123">PARAMETERS</span></span>

### <span data-ttu-id="0b89e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b89e-124">-DefaultProfile</span></span>
<span data-ttu-id="0b89e-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b89e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b89e-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="0b89e-126">-HybridConnection</span></span>
<span data-ttu-id="0b89e-127">Nome da Conexão Híbrida.</span><span class="sxs-lookup"><span data-stu-id="0b89e-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="0b89e-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="0b89e-128">-KeyValue</span></span>
<span data-ttu-id="0b89e-129">Uma chave de 256 bits codificada com base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="0b89e-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="0b89e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b89e-130">-Name</span></span>
<span data-ttu-id="0b89e-131">Nome de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="0b89e-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="0b89e-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b89e-132">-Namespace</span></span>
<span data-ttu-id="0b89e-133">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="0b89e-133">Namespace Name.</span></span>

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

### <span data-ttu-id="0b89e-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="0b89e-134">-RegenerateKey</span></span>
<span data-ttu-id="0b89e-135">Chaves de regeneração - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="0b89e-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="0b89e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b89e-136">-ResourceGroupName</span></span>
<span data-ttu-id="0b89e-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b89e-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="0b89e-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="0b89e-138">-WcfRelay</span></span>
<span data-ttu-id="0b89e-139">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="0b89e-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="0b89e-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0b89e-140">-Confirm</span></span>
<span data-ttu-id="0b89e-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b89e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b89e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b89e-142">-WhatIf</span></span>
<span data-ttu-id="0b89e-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0b89e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b89e-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b89e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b89e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b89e-145">CommonParameters</span></span>
<span data-ttu-id="0b89e-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b89e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b89e-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b89e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b89e-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b89e-148">INPUTS</span></span>

### <span data-ttu-id="0b89e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0b89e-149">System.String</span></span>

## <span data-ttu-id="0b89e-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b89e-150">OUTPUTS</span></span>

### <span data-ttu-id="0b89e-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="0b89e-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="0b89e-152">Notas</span><span class="sxs-lookup"><span data-stu-id="0b89e-152">NOTES</span></span>

## <span data-ttu-id="0b89e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b89e-153">RELATED LINKS</span></span>
