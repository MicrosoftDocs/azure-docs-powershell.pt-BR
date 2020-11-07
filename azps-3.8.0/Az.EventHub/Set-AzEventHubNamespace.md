---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 5717728fa868094a5d1d170af948743d1b9e065b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777503"
---
# <span data-ttu-id="4ad44-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4ad44-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="4ad44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ad44-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad44-103">Atualiza o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="4ad44-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4ad44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ad44-104">SYNTAX</span></span>

### <span data-ttu-id="4ad44-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ad44-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ad44-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ad44-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ad44-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad44-108">O cmdlet Set-AzEventHubNamespace atualiza as propriedades do namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="4ad44-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4ad44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ad44-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad44-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ad44-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="4ad44-111">Atualiza as marcas do namespace \` Mynamespacename \` a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4ad44-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="4ad44-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ad44-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="4ad44-113">Atualiza o estado do namespace \` Mynamespacename \` com autoinflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="4ad44-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="4ad44-114">OS</span><span class="sxs-lookup"><span data-stu-id="4ad44-114">PARAMETERS</span></span>

### <span data-ttu-id="4ad44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad44-115">-DefaultProfile</span></span>
<span data-ttu-id="4ad44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad44-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="4ad44-117">-EnableAutoInflate</span></span>
<span data-ttu-id="4ad44-118">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="4ad44-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="4ad44-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="4ad44-119">-EnableKafka</span></span>
<span data-ttu-id="4ad44-120">Habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="4ad44-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="4ad44-121">-Local</span><span class="sxs-lookup"><span data-stu-id="4ad44-121">-Location</span></span>
<span data-ttu-id="4ad44-122">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="4ad44-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="4ad44-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="4ad44-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="4ad44-124">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="4ad44-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad44-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ad44-125">-Name</span></span>
<span data-ttu-id="4ad44-126">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="4ad44-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="4ad44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad44-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ad44-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ad44-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="4ad44-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4ad44-129">-SkuCapacity</span></span>
<span data-ttu-id="4ad44-130">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="4ad44-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="4ad44-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4ad44-131">-SkuName</span></span>
<span data-ttu-id="4ad44-132">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="4ad44-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="4ad44-133">-Estado</span><span class="sxs-lookup"><span data-stu-id="4ad44-133">-State</span></span>
<span data-ttu-id="4ad44-134">Desabilitar/habilitar namespace.</span><span class="sxs-lookup"><span data-stu-id="4ad44-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad44-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="4ad44-135">-Tag</span></span>
<span data-ttu-id="4ad44-136">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ad44-136">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad44-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ad44-137">-Confirm</span></span>
<span data-ttu-id="4ad44-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad44-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad44-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad44-139">-WhatIf</span></span>
<span data-ttu-id="4ad44-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ad44-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad44-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ad44-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad44-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad44-142">CommonParameters</span></span>
<span data-ttu-id="4ad44-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad44-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad44-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad44-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad44-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ad44-145">INPUTS</span></span>

### <span data-ttu-id="4ad44-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad44-146">System.String</span></span>

### <span data-ttu-id="4ad44-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4ad44-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4ad44-148">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. Namespacestate, Microsoft. Azure. PowerShell. cmdlets. EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4ad44-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ad44-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ad44-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ad44-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ad44-150">OUTPUTS</span></span>

### <span data-ttu-id="4ad44-151">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4ad44-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4ad44-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ad44-152">NOTES</span></span>

## <span data-ttu-id="4ad44-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ad44-153">RELATED LINKS</span></span>
