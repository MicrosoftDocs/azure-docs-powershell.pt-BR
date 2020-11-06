---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431901"
---
# <span data-ttu-id="8fdd3-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="8fdd3-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="8fdd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdd3-103">Cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fdd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fdd3-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fdd3-105">DESCRIPTION</span></span>
<span data-ttu-id="8fdd3-106">O cmdlet **New-AzureRmServiceBusNamespace** cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="8fdd3-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="8fdd3-108">Esta operação é idempotente.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-108">This operation is idempotent.</span></span>

## <span data-ttu-id="8fdd3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fdd3-109">EXAMPLES</span></span>

### <span data-ttu-id="8fdd3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fdd3-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="8fdd3-111">Cria um novo namespace de barramento de serviço dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="8fdd3-112">OS</span><span class="sxs-lookup"><span data-stu-id="8fdd3-112">PARAMETERS</span></span>

### <span data-ttu-id="8fdd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdd3-113">-DefaultProfile</span></span>
<span data-ttu-id="8fdd3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fdd3-115">-Local</span><span class="sxs-lookup"><span data-stu-id="8fdd3-115">-Location</span></span>
<span data-ttu-id="8fdd3-116">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fdd3-117">-Name</span></span>
<span data-ttu-id="8fdd3-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdd3-119">-ResourceGroupName</span></span>
<span data-ttu-id="8fdd3-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8fdd3-121">-SkuCapacity</span></span>
<span data-ttu-id="8fdd3-122">As unidades de throughput do namespace Premium do barramento do serviço, valores permitidos 1 ou 2 ou 4</span><span class="sxs-lookup"><span data-stu-id="8fdd3-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8fdd3-123">-SkuName</span></span>
<span data-ttu-id="8fdd3-124">O nome de SKU do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="8fdd3-125">-Tag</span></span>
<span data-ttu-id="8fdd3-126">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="8fdd3-127">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8fdd3-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fdd3-128">-Confirm</span></span>
<span data-ttu-id="8fdd3-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdd3-130">-WhatIf</span></span>
<span data-ttu-id="8fdd3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fdd3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdd3-133">CommonParameters</span></span>
<span data-ttu-id="8fdd3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdd3-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdd3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdd3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fdd3-136">INPUTS</span></span>

### <span data-ttu-id="8fdd3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8fdd3-137">System.String</span></span>

### <span data-ttu-id="8fdd3-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8fdd3-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8fdd3-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8fdd3-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8fdd3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fdd3-140">OUTPUTS</span></span>

### <span data-ttu-id="8fdd3-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8fdd3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8fdd3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fdd3-142">NOTES</span></span>

## <span data-ttu-id="8fdd3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fdd3-143">RELATED LINKS</span></span>
