---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602940"
---
# <span data-ttu-id="bc414-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="bc414-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="bc414-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc414-102">SYNOPSIS</span></span>
<span data-ttu-id="bc414-103">Cria um namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="bc414-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc414-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc414-104">SYNTAX</span></span>

### <span data-ttu-id="bc414-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc414-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc414-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc414-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc414-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc414-107">DESCRIPTION</span></span>
<span data-ttu-id="bc414-108">O cmdlet New-AzureRmEventHubNamespace cria um novo namespace de hubs de eventos de tipo.</span><span class="sxs-lookup"><span data-stu-id="bc414-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="bc414-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc414-109">EXAMPLES</span></span>

### <span data-ttu-id="bc414-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc414-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="bc414-111">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="bc414-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bc414-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bc414-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="bc414-113">Cria um namespace de hubs de evento \` Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` e autoinflate são habilitados com MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="bc414-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="bc414-114">Exemplo 3-namespace habilitado para Kafka</span><span class="sxs-lookup"><span data-stu-id="bc414-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="bc414-115">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` com Kafka e autoinflate habilitado.</span><span class="sxs-lookup"><span data-stu-id="bc414-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="bc414-116">OS</span><span class="sxs-lookup"><span data-stu-id="bc414-116">PARAMETERS</span></span>

### <span data-ttu-id="bc414-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc414-117">-DefaultProfile</span></span>
<span data-ttu-id="bc414-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc414-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc414-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="bc414-119">-EnableAutoInflate</span></span>
<span data-ttu-id="bc414-120">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="bc414-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="bc414-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="bc414-121">-EnableKafka</span></span>
<span data-ttu-id="bc414-122">Habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="bc414-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="bc414-123">-Local</span><span class="sxs-lookup"><span data-stu-id="bc414-123">-Location</span></span>
<span data-ttu-id="bc414-124">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="bc414-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="bc414-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="bc414-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="bc414-126">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="bc414-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="bc414-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc414-127">-Name</span></span>
<span data-ttu-id="bc414-128">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="bc414-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="bc414-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc414-129">-ResourceGroupName</span></span>
<span data-ttu-id="bc414-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bc414-130">Resource Group Name</span></span>

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

### <span data-ttu-id="bc414-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bc414-131">-SkuCapacity</span></span>
<span data-ttu-id="bc414-132">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="bc414-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="bc414-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bc414-133">-SkuName</span></span>
<span data-ttu-id="bc414-134">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="bc414-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="bc414-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="bc414-135">-Tag</span></span>
<span data-ttu-id="bc414-136">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc414-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="bc414-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc414-137">-Confirm</span></span>
<span data-ttu-id="bc414-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc414-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc414-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc414-139">-WhatIf</span></span>
<span data-ttu-id="bc414-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc414-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc414-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc414-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc414-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc414-142">CommonParameters</span></span>
<span data-ttu-id="bc414-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc414-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bc414-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc414-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc414-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc414-145">INPUTS</span></span>


## <span data-ttu-id="bc414-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc414-146">OUTPUTS</span></span>

### <span data-ttu-id="bc414-147">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bc414-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="bc414-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc414-148">NOTES</span></span>

## <span data-ttu-id="bc414-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc414-149">RELATED LINKS</span></span>
