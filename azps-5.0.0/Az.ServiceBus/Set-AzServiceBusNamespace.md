---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116713"
---
# <span data-ttu-id="99f16-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="99f16-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="99f16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99f16-102">SYNOPSIS</span></span>
<span data-ttu-id="99f16-103">Atualiza a descrição de um namespace de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="99f16-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="99f16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f16-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99f16-105">DESCRIPTION</span></span>
<span data-ttu-id="99f16-106">O cmdlet **set-AzServiceBusNamespace** atualiza a descrição do namespace de barramento de serviço especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99f16-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="99f16-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99f16-107">EXAMPLES</span></span>

### <span data-ttu-id="99f16-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99f16-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="99f16-109">Atualiza o namespace de barramento do serviço com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="99f16-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="99f16-110">OS</span><span class="sxs-lookup"><span data-stu-id="99f16-110">PARAMETERS</span></span>

### <span data-ttu-id="99f16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f16-111">-DefaultProfile</span></span>
<span data-ttu-id="99f16-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99f16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99f16-113">-Local</span><span class="sxs-lookup"><span data-stu-id="99f16-113">-Location</span></span>
<span data-ttu-id="99f16-114">O local do namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="99f16-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="99f16-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="99f16-115">-Name</span></span>
<span data-ttu-id="99f16-116">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="99f16-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="99f16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f16-117">-ResourceGroupName</span></span>
<span data-ttu-id="99f16-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99f16-118">The resource group name.</span></span>

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

### <span data-ttu-id="99f16-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="99f16-119">-SkuCapacity</span></span>
<span data-ttu-id="99f16-120">Namespace da capacidade SKU.</span><span class="sxs-lookup"><span data-stu-id="99f16-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="99f16-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="99f16-121">-SkuName</span></span>
<span data-ttu-id="99f16-122">O nome do SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="99f16-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="99f16-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="99f16-123">-Tag</span></span>
<span data-ttu-id="99f16-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="99f16-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="99f16-125">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="99f16-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99f16-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99f16-126">-Confirm</span></span>
<span data-ttu-id="99f16-127">Atualiza o namespace de barramento do serviço com as informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="99f16-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="99f16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f16-128">-WhatIf</span></span>
<span data-ttu-id="99f16-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99f16-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f16-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99f16-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f16-131">CommonParameters</span></span>
<span data-ttu-id="99f16-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f16-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f16-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f16-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99f16-134">INPUTS</span></span>

### <span data-ttu-id="99f16-135">System. String</span><span class="sxs-lookup"><span data-stu-id="99f16-135">System.String</span></span>

### <span data-ttu-id="99f16-136">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="99f16-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="99f16-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99f16-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="99f16-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99f16-138">OUTPUTS</span></span>

### <span data-ttu-id="99f16-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="99f16-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="99f16-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99f16-140">NOTES</span></span>

## <span data-ttu-id="99f16-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99f16-141">RELATED LINKS</span></span>
