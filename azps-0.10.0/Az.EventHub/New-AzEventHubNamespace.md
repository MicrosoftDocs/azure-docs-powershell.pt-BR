---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 592af2c1ecd26e3e744845ae24e8f9c71cf0b0f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775878"
---
# <span data-ttu-id="857a5-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="857a5-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="857a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="857a5-102">SYNOPSIS</span></span>
<span data-ttu-id="857a5-103">Cria um namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="857a5-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="857a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="857a5-104">SYNTAX</span></span>

### <span data-ttu-id="857a5-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="857a5-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="857a5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="857a5-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857a5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="857a5-107">DESCRIPTION</span></span>
<span data-ttu-id="857a5-108">O cmdlet New-AzEventHubNamespace cria um novo namespace de hubs de eventos de tipo.</span><span class="sxs-lookup"><span data-stu-id="857a5-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="857a5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="857a5-109">EXAMPLES</span></span>

### <span data-ttu-id="857a5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="857a5-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="857a5-111">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="857a5-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="857a5-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="857a5-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="857a5-113">Cria um namespace de hubs de evento \` Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` e autoinflate são habilitados com MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="857a5-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="857a5-114">Exemplo 3-namespace habilitado para Kafka</span><span class="sxs-lookup"><span data-stu-id="857a5-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="857a5-115">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` com Kafka e autoinflate habilitado.</span><span class="sxs-lookup"><span data-stu-id="857a5-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="857a5-116">OS</span><span class="sxs-lookup"><span data-stu-id="857a5-116">PARAMETERS</span></span>

### <span data-ttu-id="857a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857a5-117">-DefaultProfile</span></span>
<span data-ttu-id="857a5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="857a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857a5-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="857a5-119">-EnableAutoInflate</span></span>
<span data-ttu-id="857a5-120">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="857a5-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="857a5-121">-EnableKafka</span></span>
<span data-ttu-id="857a5-122">Habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="857a5-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-123">-Local</span><span class="sxs-lookup"><span data-stu-id="857a5-123">-Location</span></span>
<span data-ttu-id="857a5-124">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="857a5-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="857a5-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="857a5-126">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="857a5-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="857a5-127">-Name</span></span>
<span data-ttu-id="857a5-128">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="857a5-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="857a5-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="857a5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="857a5-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="857a5-131">-SkuCapacity</span></span>
<span data-ttu-id="857a5-132">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="857a5-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="857a5-133">-SkuName</span></span>
<span data-ttu-id="857a5-134">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="857a5-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="857a5-135">-Tag</span></span>
<span data-ttu-id="857a5-136">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="857a5-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="857a5-137">-Confirm</span></span>
<span data-ttu-id="857a5-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857a5-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857a5-139">-WhatIf</span></span>
<span data-ttu-id="857a5-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="857a5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857a5-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="857a5-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857a5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857a5-142">CommonParameters</span></span>
<span data-ttu-id="857a5-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857a5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857a5-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857a5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857a5-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="857a5-145">INPUTS</span></span>

### <span data-ttu-id="857a5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="857a5-146">System.String</span></span>

### <span data-ttu-id="857a5-147">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="857a5-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="857a5-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="857a5-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="857a5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="857a5-149">OUTPUTS</span></span>

### <span data-ttu-id="857a5-150">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="857a5-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="857a5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="857a5-151">NOTES</span></span>

## <span data-ttu-id="857a5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="857a5-152">RELATED LINKS</span></span>