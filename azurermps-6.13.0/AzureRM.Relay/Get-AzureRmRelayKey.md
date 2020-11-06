---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 69f6b1bc50681bafe7a860dcebaa7616c8f14e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610857"
---
# <span data-ttu-id="dc28f-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="dc28f-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="dc28f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc28f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc28f-103">Obtém as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc28f-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc28f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc28f-104">SYNTAX</span></span>

### <span data-ttu-id="dc28f-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc28f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc28f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc28f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc28f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc28f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc28f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc28f-108">DESCRIPTION</span></span>
<span data-ttu-id="dc28f-109">O cmdlet **Get-AzureRmRelayKey** retorna as cadeias de conexão primária e secundária para as entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc28f-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dc28f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc28f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc28f-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="dc28f-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="dc28f-112">Exemplo 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc28f-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="dc28f-113">Exemplo 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc28f-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc28f-114">Cadeia de conexão primária e secundária para as entidades de retransmissão especificadas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc28f-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dc28f-115">OS</span><span class="sxs-lookup"><span data-stu-id="dc28f-115">PARAMETERS</span></span>

### <span data-ttu-id="dc28f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc28f-116">-DefaultProfile</span></span>
<span data-ttu-id="dc28f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc28f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc28f-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc28f-118">-HybridConnection</span></span>
<span data-ttu-id="dc28f-119">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="dc28f-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dc28f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc28f-120">-Name</span></span>
<span data-ttu-id="dc28f-121">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="dc28f-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="dc28f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc28f-122">-Namespace</span></span>
<span data-ttu-id="dc28f-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="dc28f-123">Namespace Name.</span></span>

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

### <span data-ttu-id="dc28f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc28f-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc28f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc28f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc28f-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc28f-126">-WcfRelay</span></span>
<span data-ttu-id="dc28f-127">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dc28f-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dc28f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc28f-128">CommonParameters</span></span>
<span data-ttu-id="dc28f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc28f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dc28f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc28f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc28f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc28f-131">INPUTS</span></span>

### <span data-ttu-id="dc28f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dc28f-132">System.String</span></span>


## <span data-ttu-id="dc28f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc28f-133">OUTPUTS</span></span>

### <span data-ttu-id="dc28f-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="dc28f-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="dc28f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc28f-135">NOTES</span></span>

## <span data-ttu-id="dc28f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc28f-136">RELATED LINKS</span></span>
