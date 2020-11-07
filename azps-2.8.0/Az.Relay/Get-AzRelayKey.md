---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772640"
---
# <span data-ttu-id="f778d-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="f778d-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="f778d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f778d-102">SYNOPSIS</span></span>
<span data-ttu-id="f778d-103">Obtém as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f778d-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f778d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f778d-104">SYNTAX</span></span>

### <span data-ttu-id="f778d-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f778d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f778d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f778d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f778d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f778d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f778d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f778d-108">DESCRIPTION</span></span>
<span data-ttu-id="f778d-109">O cmdlet **Get-AzRelayKey** retorna as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f778d-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f778d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f778d-110">EXAMPLES</span></span>

### <span data-ttu-id="f778d-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="f778d-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="f778d-112">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f778d-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="f778d-113">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f778d-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="f778d-114">Cadeia de conexão primária e secundária para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f778d-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f778d-115">OS</span><span class="sxs-lookup"><span data-stu-id="f778d-115">PARAMETERS</span></span>

### <span data-ttu-id="f778d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f778d-116">-DefaultProfile</span></span>
<span data-ttu-id="f778d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f778d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f778d-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f778d-118">-HybridConnection</span></span>
<span data-ttu-id="f778d-119">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="f778d-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f778d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f778d-120">-Name</span></span>
<span data-ttu-id="f778d-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="f778d-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f778d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f778d-122">-Namespace</span></span>
<span data-ttu-id="f778d-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="f778d-123">Namespace Name.</span></span>

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

### <span data-ttu-id="f778d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f778d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f778d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f778d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f778d-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f778d-126">-WcfRelay</span></span>
<span data-ttu-id="f778d-127">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="f778d-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f778d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f778d-128">CommonParameters</span></span>
<span data-ttu-id="f778d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f778d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f778d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f778d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f778d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f778d-131">INPUTS</span></span>

### <span data-ttu-id="f778d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f778d-132">System.String</span></span>

## <span data-ttu-id="f778d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f778d-133">OUTPUTS</span></span>

### <span data-ttu-id="f778d-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f778d-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="f778d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f778d-135">NOTES</span></span>

## <span data-ttu-id="f778d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f778d-136">RELATED LINKS</span></span>