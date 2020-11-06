---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610714"
---
# <span data-ttu-id="18c13-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="18c13-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="18c13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18c13-102">SYNOPSIS</span></span>
<span data-ttu-id="18c13-103">Regenera a cadeia de caracteres de conexão primária ou secundária para a fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="18c13-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18c13-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18c13-105">DESCRIPTION</span></span>
<span data-ttu-id="18c13-106">O cmdlet **New-AzureRmServiceBusQueueKey** regenera as cadeias de conexão primárias ou secundárias para a fila do barramento do serviço especificado e a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="18c13-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="18c13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18c13-107">EXAMPLES</span></span>

### <span data-ttu-id="18c13-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18c13-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="18c13-109">Regenera a cadeia de caracteres de conexão principal para o namespace.</span><span class="sxs-lookup"><span data-stu-id="18c13-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="18c13-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18c13-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="18c13-111">Regenera a cadeia de conexão secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="18c13-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="18c13-112">OS</span><span class="sxs-lookup"><span data-stu-id="18c13-112">PARAMETERS</span></span>

### <span data-ttu-id="18c13-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="18c13-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="18c13-114">O nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="18c13-114">The authorization rule name.</span></span>

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

### <span data-ttu-id="18c13-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="18c13-115">-NamespaceName</span></span>
<span data-ttu-id="18c13-116">O nome do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="18c13-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c13-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="18c13-117">-QueueName</span></span>
<span data-ttu-id="18c13-118">O nome da fila do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="18c13-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c13-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="18c13-119">-RegenerateKeys</span></span>
<span data-ttu-id="18c13-120">Especifica se deve regenerar as chaves primárias ou secundárias.</span><span class="sxs-lookup"><span data-stu-id="18c13-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c13-121">-Resource</span><span class="sxs-lookup"><span data-stu-id="18c13-121">-ResourceGroup</span></span>
<span data-ttu-id="18c13-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18c13-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="18c13-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18c13-123">-Confirm</span></span>
<span data-ttu-id="18c13-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c13-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c13-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c13-125">-WhatIf</span></span>
<span data-ttu-id="18c13-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18c13-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c13-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18c13-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c13-128">CommonParameters</span></span>
<span data-ttu-id="18c13-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c13-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c13-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c13-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18c13-131">INPUTS</span></span>

### <span data-ttu-id="18c13-132">-Resource</span><span class="sxs-lookup"><span data-stu-id="18c13-132">-ResourceGroup</span></span>
 <span data-ttu-id="18c13-133">System. String</span><span class="sxs-lookup"><span data-stu-id="18c13-133">System.String</span></span>
 

### <span data-ttu-id="18c13-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="18c13-134">-NamespaceName</span></span>
 <span data-ttu-id="18c13-135">System. String</span><span class="sxs-lookup"><span data-stu-id="18c13-135">System.String</span></span>
 

### <span data-ttu-id="18c13-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="18c13-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="18c13-137">System. String</span><span class="sxs-lookup"><span data-stu-id="18c13-137">System.String</span></span>
 

### <span data-ttu-id="18c13-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="18c13-138">-QueueName</span></span>
 <span data-ttu-id="18c13-139">System. String</span><span class="sxs-lookup"><span data-stu-id="18c13-139">System.String</span></span>
 

### <span data-ttu-id="18c13-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="18c13-140">-RegenerateKeys</span></span>
 <span data-ttu-id="18c13-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18c13-141">System.String</span></span>

## <span data-ttu-id="18c13-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18c13-142">OUTPUTS</span></span>

### <span data-ttu-id="18c13-143">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="18c13-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="18c13-144">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey valor} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="18c13-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="18c13-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18c13-145">NOTES</span></span>

## <span data-ttu-id="18c13-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18c13-146">RELATED LINKS</span></span>

