---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440181"
---
# <span data-ttu-id="b4b27-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b4b27-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="b4b27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4b27-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b27-103">Cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b27-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4b27-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4b27-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b27-106">O cmdlet **New-AzureRmServiceBusNamespace** cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b27-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="b4b27-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="b4b27-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="b4b27-108">Esta operação é idempotente.</span><span class="sxs-lookup"><span data-stu-id="b4b27-108">This operation is idempotent.</span></span>

## <span data-ttu-id="b4b27-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4b27-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b27-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4b27-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="b4b27-111">Cria um novo namespace de barramento de serviço dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b4b27-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="b4b27-112">OS</span><span class="sxs-lookup"><span data-stu-id="b4b27-112">PARAMETERS</span></span>

### <span data-ttu-id="b4b27-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b4b27-113">-Location</span></span>
<span data-ttu-id="b4b27-114">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b27-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="b4b27-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b4b27-115">-NamespaceName</span></span>
<span data-ttu-id="b4b27-116">O nome do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b27-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="b4b27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b27-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4b27-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4b27-118">The resource group name.</span></span>

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

### <span data-ttu-id="b4b27-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4b27-119">-SkuName</span></span>
<span data-ttu-id="b4b27-120">O nome de SKU do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b4b27-120">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b27-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="b4b27-121">-Tag</span></span>
<span data-ttu-id="b4b27-122">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="b4b27-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="b4b27-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b4b27-123">For example:</span></span>

<span data-ttu-id="b4b27-124">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4b27-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b27-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4b27-125">-Confirm</span></span>
<span data-ttu-id="b4b27-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b27-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b27-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b27-127">-WhatIf</span></span>
<span data-ttu-id="b4b27-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4b27-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4b27-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4b27-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b27-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b27-130">CommonParameters</span></span>
<span data-ttu-id="b4b27-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b27-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b27-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b27-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b27-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4b27-133">INPUTS</span></span>

### <span data-ttu-id="b4b27-134">-Resource</span><span class="sxs-lookup"><span data-stu-id="b4b27-134">-ResourceGroup</span></span>
 <span data-ttu-id="b4b27-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b27-135">System.String</span></span>

### <span data-ttu-id="b4b27-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b4b27-136">-NamespaceName</span></span>
 <span data-ttu-id="b4b27-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b27-137">System.String</span></span>

### <span data-ttu-id="b4b27-138">-Local</span><span class="sxs-lookup"><span data-stu-id="b4b27-138">-Location</span></span>
 <span data-ttu-id="b4b27-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b27-139">System.String</span></span>

### <span data-ttu-id="b4b27-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4b27-140">-SkuName</span></span>
 <span data-ttu-id="b4b27-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b27-141">System.String</span></span>

### <span data-ttu-id="b4b27-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="b4b27-142">-Tag</span></span>
 <span data-ttu-id="b4b27-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4b27-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4b27-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4b27-144">OUTPUTS</span></span>

### <span data-ttu-id="b4b27-145">Microsoft. Azure. Commands. ServiceBus. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="b4b27-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="b4b27-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4b27-146">NOTES</span></span>

## <span data-ttu-id="b4b27-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4b27-147">RELATED LINKS</span></span>
