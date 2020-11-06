---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610460"
---
# <span data-ttu-id="b953e-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b953e-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="b953e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b953e-102">SYNOPSIS</span></span>
<span data-ttu-id="b953e-103">Atualiza a descrição de um namespace de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="b953e-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b953e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b953e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b953e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b953e-105">DESCRIPTION</span></span>
<span data-ttu-id="b953e-106">O cmdlet **set-AzureRmServiceBusNamespace** atualiza a descrição do namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b953e-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="b953e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b953e-107">EXAMPLES</span></span>

### <span data-ttu-id="b953e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b953e-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="b953e-109">Atualiza o namespace de barramento do serviço com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="b953e-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="b953e-110">OS</span><span class="sxs-lookup"><span data-stu-id="b953e-110">PARAMETERS</span></span>

### <span data-ttu-id="b953e-111">-Local</span><span class="sxs-lookup"><span data-stu-id="b953e-111">-Location</span></span>
<span data-ttu-id="b953e-112">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b953e-112">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="b953e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b953e-113">-ResourceGroupName</span></span>
<span data-ttu-id="b953e-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b953e-114">The resource group name.</span></span>

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

### <span data-ttu-id="b953e-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b953e-115">-SkuCapacity</span></span>
<span data-ttu-id="b953e-116">Namespace da capacidade SKU.</span><span class="sxs-lookup"><span data-stu-id="b953e-116">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="b953e-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b953e-117">-SkuName</span></span>
<span data-ttu-id="b953e-118">O nome do SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="b953e-118">The namespace SKU name.</span></span>

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

### <span data-ttu-id="b953e-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="b953e-119">-Tag</span></span>
<span data-ttu-id="b953e-120">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b953e-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b953e-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b953e-121">For example:</span></span>

<span data-ttu-id="b953e-122">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b953e-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b953e-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b953e-123">-Confirm</span></span>
<span data-ttu-id="b953e-124">Atualiza o namespace de barramento do serviço com as informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="b953e-124">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="b953e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b953e-125">-WhatIf</span></span>
<span data-ttu-id="b953e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b953e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b953e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b953e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b953e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b953e-128">-DefaultProfile</span></span>
<span data-ttu-id="b953e-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b953e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b953e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="b953e-130">-Name</span></span>
<span data-ttu-id="b953e-131">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="b953e-131">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="b953e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b953e-132">CommonParameters</span></span>
<span data-ttu-id="b953e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b953e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b953e-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b953e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b953e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b953e-135">INPUTS</span></span>

### <span data-ttu-id="b953e-136">-Resource</span><span class="sxs-lookup"><span data-stu-id="b953e-136">-ResourceGroup</span></span>
 <span data-ttu-id="b953e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b953e-137">System.String</span></span>

### <span data-ttu-id="b953e-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b953e-138">-NamespaceName</span></span>
 <span data-ttu-id="b953e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b953e-139">System.String</span></span>

### <span data-ttu-id="b953e-140">-Local</span><span class="sxs-lookup"><span data-stu-id="b953e-140">-Location</span></span>
 <span data-ttu-id="b953e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b953e-141">System.String</span></span>

### <span data-ttu-id="b953e-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b953e-142">-SkuName</span></span>
 <span data-ttu-id="b953e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b953e-143">System.String</span></span>

### <span data-ttu-id="b953e-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="b953e-144">-Tag</span></span>
 <span data-ttu-id="b953e-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b953e-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b953e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b953e-146">OUTPUTS</span></span>

### <span data-ttu-id="b953e-147">Microsoft. Azure. Commands. ServiceBus. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="b953e-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="b953e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b953e-148">NOTES</span></span>
## <span data-ttu-id="b953e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b953e-149">RELATED LINKS</span></span>

## <span data-ttu-id="b953e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b953e-150">RELATED LINKS</span></span>

