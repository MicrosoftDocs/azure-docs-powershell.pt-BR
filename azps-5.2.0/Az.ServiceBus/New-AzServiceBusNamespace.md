---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260288"
---
# <span data-ttu-id="597f2-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="597f2-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="597f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="597f2-102">SYNOPSIS</span></span>
<span data-ttu-id="597f2-103">Cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="597f2-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="597f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="597f2-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="597f2-105">DESCRIPTION</span></span>
<span data-ttu-id="597f2-106">O cmdlet **New-AzServiceBusNamespace** cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="597f2-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="597f2-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="597f2-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="597f2-108">Esta operação é idempotente.</span><span class="sxs-lookup"><span data-stu-id="597f2-108">This operation is idempotent.</span></span>

## <span data-ttu-id="597f2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="597f2-109">EXAMPLES</span></span>

### <span data-ttu-id="597f2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="597f2-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="597f2-111">Cria um novo namespace de barramento de serviço dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="597f2-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="597f2-112">OS</span><span class="sxs-lookup"><span data-stu-id="597f2-112">PARAMETERS</span></span>

### <span data-ttu-id="597f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597f2-113">-DefaultProfile</span></span>
<span data-ttu-id="597f2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="597f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597f2-115">-Local</span><span class="sxs-lookup"><span data-stu-id="597f2-115">-Location</span></span>
<span data-ttu-id="597f2-116">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="597f2-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="597f2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="597f2-117">-Name</span></span>
<span data-ttu-id="597f2-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="597f2-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="597f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="597f2-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="597f2-120">The resource group name.</span></span>

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

### <span data-ttu-id="597f2-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="597f2-121">-SkuCapacity</span></span>
<span data-ttu-id="597f2-122">As unidades de throughput do namespace Premium do barramento do serviço, valores permitidos 1 ou 2 ou 4</span><span class="sxs-lookup"><span data-stu-id="597f2-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="597f2-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="597f2-123">-SkuName</span></span>
<span data-ttu-id="597f2-124">O nome de SKU do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="597f2-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="597f2-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="597f2-125">-Tag</span></span>
<span data-ttu-id="597f2-126">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="597f2-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="597f2-127">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="597f2-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="597f2-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="597f2-128">-Confirm</span></span>
<span data-ttu-id="597f2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597f2-130">-WhatIf</span></span>
<span data-ttu-id="597f2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="597f2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="597f2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="597f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597f2-133">CommonParameters</span></span>
<span data-ttu-id="597f2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597f2-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597f2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597f2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="597f2-136">INPUTS</span></span>

### <span data-ttu-id="597f2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="597f2-137">System.String</span></span>

### <span data-ttu-id="597f2-138">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="597f2-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="597f2-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="597f2-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="597f2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="597f2-140">OUTPUTS</span></span>

### <span data-ttu-id="597f2-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="597f2-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="597f2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="597f2-142">NOTES</span></span>

## <span data-ttu-id="597f2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="597f2-143">RELATED LINKS</span></span>
