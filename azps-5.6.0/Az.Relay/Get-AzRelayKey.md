---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: ca477e278ef28cd2fce17578d55782f3ab610954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891730"
---
# <span data-ttu-id="a357f-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="a357f-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="a357f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a357f-102">SYNOPSIS</span></span>
<span data-ttu-id="a357f-103">Obtém as cadeias de caracteres de conexão primárias e secundárias para as entidades Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a357f-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a357f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a357f-104">SYNTAX</span></span>

### <span data-ttu-id="a357f-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a357f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a357f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a357f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a357f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a357f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a357f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a357f-108">DESCRIPTION</span></span>
<span data-ttu-id="a357f-109">O cmdlet **Get-AzRelayKey** retorna as cadeias de caracteres de conexão primárias e secundárias para as entidades Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a357f-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a357f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a357f-110">EXAMPLES</span></span>

### <span data-ttu-id="a357f-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="a357f-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="a357f-112">Exemplo 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a357f-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="a357f-113">Exemplo 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a357f-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="a357f-114">Cadeia de conexão primária e secundária para as entidades relay especificadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a357f-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a357f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a357f-115">PARAMETERS</span></span>

### <span data-ttu-id="a357f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a357f-116">-DefaultProfile</span></span>
<span data-ttu-id="a357f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a357f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a357f-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a357f-118">-HybridConnection</span></span>
<span data-ttu-id="a357f-119">Nome de HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="a357f-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="a357f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a357f-120">-Name</span></span>
<span data-ttu-id="a357f-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a357f-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a357f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a357f-122">-Namespace</span></span>
<span data-ttu-id="a357f-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a357f-123">Namespace Name.</span></span>

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

### <span data-ttu-id="a357f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a357f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a357f-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a357f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a357f-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a357f-126">-WcfRelay</span></span>
<span data-ttu-id="a357f-127">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="a357f-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a357f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a357f-128">CommonParameters</span></span>
<span data-ttu-id="a357f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a357f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a357f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a357f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a357f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a357f-131">INPUTS</span></span>

### <span data-ttu-id="a357f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a357f-132">System.String</span></span>

## <span data-ttu-id="a357f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a357f-133">OUTPUTS</span></span>

### <span data-ttu-id="a357f-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a357f-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="a357f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a357f-135">NOTES</span></span>

## <span data-ttu-id="a357f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a357f-136">RELATED LINKS</span></span>
