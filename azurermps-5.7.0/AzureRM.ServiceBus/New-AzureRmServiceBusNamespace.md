---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431613"
---
# <span data-ttu-id="cfe81-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="cfe81-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="cfe81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfe81-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe81-103">Cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="cfe81-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfe81-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfe81-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe81-106">O cmdlet **New-AzureRmServiceBusNamespace** cria um novo namespace de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="cfe81-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="cfe81-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="cfe81-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="cfe81-108">Esta operação é idempotente.</span><span class="sxs-lookup"><span data-stu-id="cfe81-108">This operation is idempotent.</span></span>

## <span data-ttu-id="cfe81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfe81-109">EXAMPLES</span></span>

### <span data-ttu-id="cfe81-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfe81-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="cfe81-111">Cria um novo namespace de barramento de serviço dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cfe81-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="cfe81-112">OS</span><span class="sxs-lookup"><span data-stu-id="cfe81-112">PARAMETERS</span></span>

### <span data-ttu-id="cfe81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe81-113">-DefaultProfile</span></span>
<span data-ttu-id="cfe81-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe81-115">-Local</span><span class="sxs-lookup"><span data-stu-id="cfe81-115">-Location</span></span>
<span data-ttu-id="cfe81-116">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="cfe81-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="cfe81-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfe81-117">-Name</span></span>
<span data-ttu-id="cfe81-118">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="cfe81-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe81-119">-ResourceGroupName</span></span>
<span data-ttu-id="cfe81-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfe81-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe81-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfe81-121">-SkuName</span></span>
<span data-ttu-id="cfe81-122">O nome de SKU do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="cfe81-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="cfe81-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="cfe81-123">-Tag</span></span>
<span data-ttu-id="cfe81-124">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="cfe81-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="cfe81-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cfe81-125">For example:</span></span>

<span data-ttu-id="cfe81-126">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cfe81-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfe81-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfe81-127">-Confirm</span></span>
<span data-ttu-id="cfe81-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe81-129">-WhatIf</span></span>
<span data-ttu-id="cfe81-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfe81-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfe81-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfe81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe81-132">CommonParameters</span></span>
<span data-ttu-id="cfe81-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe81-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe81-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfe81-135">INPUTS</span></span>

### <span data-ttu-id="cfe81-136">-Resource</span><span class="sxs-lookup"><span data-stu-id="cfe81-136">-ResourceGroup</span></span>
 <span data-ttu-id="cfe81-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe81-137">System.String</span></span>

### <span data-ttu-id="cfe81-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="cfe81-138">-NamespaceName</span></span>
 <span data-ttu-id="cfe81-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe81-139">System.String</span></span>

### <span data-ttu-id="cfe81-140">-Local</span><span class="sxs-lookup"><span data-stu-id="cfe81-140">-Location</span></span>
 <span data-ttu-id="cfe81-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe81-141">System.String</span></span>

### <span data-ttu-id="cfe81-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfe81-142">-SkuName</span></span>
 <span data-ttu-id="cfe81-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe81-143">System.String</span></span>

### <span data-ttu-id="cfe81-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="cfe81-144">-Tag</span></span>
 <span data-ttu-id="cfe81-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfe81-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfe81-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfe81-146">OUTPUTS</span></span>

### <span data-ttu-id="cfe81-147">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cfe81-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cfe81-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfe81-148">NOTES</span></span>

## <span data-ttu-id="cfe81-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfe81-149">RELATED LINKS</span></span>

