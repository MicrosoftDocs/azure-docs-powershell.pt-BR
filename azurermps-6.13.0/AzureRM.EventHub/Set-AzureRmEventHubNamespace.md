---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431956"
---
# <span data-ttu-id="43f5d-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="43f5d-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="43f5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="43f5d-103">Atualiza o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="43f5d-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43f5d-104">SYNTAX</span></span>

### <span data-ttu-id="43f5d-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="43f5d-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43f5d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="43f5d-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f5d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="43f5d-108">O cmdlet Set-AzureRmEventHubNamespace atualiza as propriedades do namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="43f5d-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="43f5d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="43f5d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43f5d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="43f5d-111">Atualiza o estado do namespace \` Mynamespacename \` a ser criado.</span><span class="sxs-lookup"><span data-stu-id="43f5d-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="43f5d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="43f5d-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="43f5d-113">Atualiza o estado do namespace \` Mynamespacename \` com autoinflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="43f5d-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="43f5d-114">OS</span><span class="sxs-lookup"><span data-stu-id="43f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="43f5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f5d-115">-DefaultProfile</span></span>
<span data-ttu-id="43f5d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43f5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43f5d-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="43f5d-117">-EnableAutoInflate</span></span>
<span data-ttu-id="43f5d-118">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="43f5d-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="43f5d-119">-Local</span><span class="sxs-lookup"><span data-stu-id="43f5d-119">-Location</span></span>
<span data-ttu-id="43f5d-120">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="43f5d-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="43f5d-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="43f5d-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="43f5d-122">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="43f5d-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="43f5d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="43f5d-123">-Name</span></span>
<span data-ttu-id="43f5d-124">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="43f5d-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="43f5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="43f5d-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43f5d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="43f5d-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="43f5d-127">-SkuCapacity</span></span>
<span data-ttu-id="43f5d-128">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="43f5d-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="43f5d-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="43f5d-129">-SkuName</span></span>
<span data-ttu-id="43f5d-130">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="43f5d-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="43f5d-131">-Estado</span><span class="sxs-lookup"><span data-stu-id="43f5d-131">-State</span></span>
<span data-ttu-id="43f5d-132">Desabilitar/habilitar namespace.</span><span class="sxs-lookup"><span data-stu-id="43f5d-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="43f5d-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="43f5d-133">-Tag</span></span>
<span data-ttu-id="43f5d-134">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="43f5d-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="43f5d-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43f5d-135">-Confirm</span></span>
<span data-ttu-id="43f5d-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f5d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f5d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f5d-137">-WhatIf</span></span>
<span data-ttu-id="43f5d-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43f5d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f5d-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43f5d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f5d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f5d-140">CommonParameters</span></span>
<span data-ttu-id="43f5d-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f5d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f5d-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f5d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f5d-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43f5d-143">INPUTS</span></span>

### <span data-ttu-id="43f5d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="43f5d-144">System.String</span></span>

### <span data-ttu-id="43f5d-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="43f5d-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="43f5d-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. Namespacestate, Microsoft. Azure. Commands. EventHub, Version = 0.6.7.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43f5d-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="43f5d-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="43f5d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="43f5d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43f5d-148">OUTPUTS</span></span>

### <span data-ttu-id="43f5d-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="43f5d-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="43f5d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43f5d-150">NOTES</span></span>

## <span data-ttu-id="43f5d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43f5d-151">RELATED LINKS</span></span>
