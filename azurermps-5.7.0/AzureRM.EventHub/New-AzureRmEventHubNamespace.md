---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432126"
---
# <span data-ttu-id="8b18c-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8b18c-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="8b18c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b18c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b18c-103">Cria um namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="8b18c-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b18c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b18c-104">SYNTAX</span></span>

### <span data-ttu-id="8b18c-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b18c-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b18c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b18c-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b18c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b18c-107">DESCRIPTION</span></span>
<span data-ttu-id="8b18c-108">O cmdlet New-AzureRmEventHubNamespace cria um novo namespace de hubs de eventos de tipo.</span><span class="sxs-lookup"><span data-stu-id="8b18c-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="8b18c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b18c-109">EXAMPLES</span></span>

### <span data-ttu-id="8b18c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b18c-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="8b18c-111">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8b18c-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8b18c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8b18c-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="8b18c-113">Cria um namespace de hubs de evento \` Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` e autoinflate são habilitados com MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="8b18c-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="8b18c-114">OS</span><span class="sxs-lookup"><span data-stu-id="8b18c-114">PARAMETERS</span></span>

### <span data-ttu-id="8b18c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b18c-115">-DefaultProfile</span></span>
<span data-ttu-id="8b18c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b18c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b18c-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="8b18c-117">-EnableAutoInflate</span></span>
<span data-ttu-id="8b18c-118">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="8b18c-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-119">-Local</span><span class="sxs-lookup"><span data-stu-id="8b18c-119">-Location</span></span>
<span data-ttu-id="8b18c-120">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="8b18c-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="8b18c-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="8b18c-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="8b18c-122">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="8b18c-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b18c-123">-Name</span></span>
<span data-ttu-id="8b18c-124">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="8b18c-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b18c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b18c-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8b18c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8b18c-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8b18c-127">-SkuCapacity</span></span>
<span data-ttu-id="8b18c-128">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="8b18c-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8b18c-129">-SkuName</span></span>
<span data-ttu-id="8b18c-130">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="8b18c-130">Namespace Sku Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="8b18c-131">-Tag</span></span>
<span data-ttu-id="8b18c-132">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b18c-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b18c-133">-Confirm</span></span>
<span data-ttu-id="8b18c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b18c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b18c-135">-WhatIf</span></span>
<span data-ttu-id="8b18c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b18c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b18c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b18c-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b18c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b18c-138">CommonParameters</span></span>
<span data-ttu-id="8b18c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b18c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8b18c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b18c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b18c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b18c-141">INPUTS</span></span>

### <span data-ttu-id="8b18c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8b18c-142">System.String</span></span>
<span data-ttu-id="8b18c-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b18c-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="8b18c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b18c-144">OUTPUTS</span></span>

### <span data-ttu-id="8b18c-145">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8b18c-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="8b18c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b18c-146">NOTES</span></span>

## <span data-ttu-id="8b18c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b18c-147">RELATED LINKS</span></span>
