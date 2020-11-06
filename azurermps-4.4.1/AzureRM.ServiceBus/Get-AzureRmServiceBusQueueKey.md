---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433003"
---
# <span data-ttu-id="8cad2-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="8cad2-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="8cad2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cad2-102">SYNOPSIS</span></span>
<span data-ttu-id="8cad2-103">Obtém as cadeias de conexão primária e secundária para a fila de barramento de serviço específica.</span><span class="sxs-lookup"><span data-stu-id="8cad2-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cad2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cad2-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cad2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cad2-105">DESCRIPTION</span></span>
<span data-ttu-id="8cad2-106">O cmdlet **Get-AzureRmServiceBusQueueKey** retorna as cadeias de conexão primária e secundária para a fila de barramento de serviço específica.</span><span class="sxs-lookup"><span data-stu-id="8cad2-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="8cad2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cad2-107">EXAMPLES</span></span>

### <span data-ttu-id="8cad2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cad2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="8cad2-109">Retorna as cadeias de conexão primária e secundária para a fila do barramento do serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="8cad2-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="8cad2-110">OS</span><span class="sxs-lookup"><span data-stu-id="8cad2-110">PARAMETERS</span></span>

### <span data-ttu-id="8cad2-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="8cad2-111">-ResourceGroup</span></span>
<span data-ttu-id="8cad2-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cad2-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cad2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cad2-113">-DefaultProfile</span></span>
<span data-ttu-id="8cad2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cad2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cad2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cad2-115">-Name</span></span>
<span data-ttu-id="8cad2-116">Nome de AuthorizationRule da fila do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8cad2-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cad2-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cad2-117">-Namespace</span></span>
<span data-ttu-id="8cad2-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8cad2-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cad2-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="8cad2-119">-Queue</span></span>
<span data-ttu-id="8cad2-120">Nome da fila do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8cad2-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cad2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cad2-121">CommonParameters</span></span>
<span data-ttu-id="8cad2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cad2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cad2-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cad2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cad2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cad2-124">INPUTS</span></span>

### <span data-ttu-id="8cad2-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="8cad2-125">-ResourceGroup</span></span>
 <span data-ttu-id="8cad2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8cad2-126">System.String</span></span>
 

### <span data-ttu-id="8cad2-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8cad2-127">-NamespaceName</span></span>
 <span data-ttu-id="8cad2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8cad2-128">System.String</span></span>
 

### <span data-ttu-id="8cad2-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="8cad2-129">-QueueName</span></span>
 <span data-ttu-id="8cad2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8cad2-130">System.String</span></span>
 

### <span data-ttu-id="8cad2-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="8cad2-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="8cad2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8cad2-132">System.String</span></span>

## <span data-ttu-id="8cad2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cad2-133">OUTPUTS</span></span>

### <span data-ttu-id="8cad2-134">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="8cad2-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="8cad2-135">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey valor} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8cad2-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="8cad2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cad2-136">NOTES</span></span>

## <span data-ttu-id="8cad2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cad2-137">RELATED LINKS</span></span>

