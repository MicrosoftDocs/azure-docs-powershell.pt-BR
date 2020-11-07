---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 4434802f1025e24bb249ee503ed2267e9187a2c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778170"
---
# <span data-ttu-id="05776-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="05776-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="05776-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05776-102">SYNOPSIS</span></span>
<span data-ttu-id="05776-103">Obtém as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="05776-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="05776-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05776-104">SYNTAX</span></span>

### <span data-ttu-id="05776-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="05776-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05776-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="05776-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05776-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="05776-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05776-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05776-108">DESCRIPTION</span></span>
<span data-ttu-id="05776-109">O cmdlet **Get-AzRelayKey** retorna as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="05776-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="05776-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05776-110">EXAMPLES</span></span>

### <span data-ttu-id="05776-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="05776-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="05776-112">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="05776-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="05776-113">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="05776-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="05776-114">Cadeia de conexão primária e secundária para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="05776-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="05776-115">OS</span><span class="sxs-lookup"><span data-stu-id="05776-115">PARAMETERS</span></span>

### <span data-ttu-id="05776-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05776-116">-DefaultProfile</span></span>
<span data-ttu-id="05776-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05776-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05776-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="05776-118">-HybridConnection</span></span>
<span data-ttu-id="05776-119">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="05776-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="05776-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="05776-120">-Name</span></span>
<span data-ttu-id="05776-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="05776-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="05776-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="05776-122">-Namespace</span></span>
<span data-ttu-id="05776-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="05776-123">Namespace Name.</span></span>

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

### <span data-ttu-id="05776-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05776-124">-ResourceGroupName</span></span>
<span data-ttu-id="05776-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05776-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="05776-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="05776-126">-WcfRelay</span></span>
<span data-ttu-id="05776-127">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="05776-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="05776-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05776-128">CommonParameters</span></span>
<span data-ttu-id="05776-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05776-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05776-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05776-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05776-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05776-131">INPUTS</span></span>

### <span data-ttu-id="05776-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05776-132">System.String</span></span>

## <span data-ttu-id="05776-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05776-133">OUTPUTS</span></span>

### <span data-ttu-id="05776-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="05776-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="05776-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05776-135">NOTES</span></span>

## <span data-ttu-id="05776-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05776-136">RELATED LINKS</span></span>
