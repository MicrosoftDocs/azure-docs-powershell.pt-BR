---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 2e024d3b82b6e553aa40bd6e570a848645538e11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891357"
---
# <span data-ttu-id="1be39-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1be39-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="1be39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be39-102">SYNOPSIS</span></span>
<span data-ttu-id="1be39-103">Cria um enriquecimento de mensagens para pontos de extremidade escolhidos em seu Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="1be39-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="1be39-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1be39-104">SYNTAX</span></span>

### <span data-ttu-id="1be39-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1be39-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be39-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1be39-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be39-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1be39-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be39-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1be39-108">DESCRIPTION</span></span>
<span data-ttu-id="1be39-109">Adicione até 10 enriquecimentos de mensagens por Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="1be39-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="1be39-110">Elas são adicionadas como propriedades de aplicativo a mensagens enviadas para os pontos de extremidade escolhidos.</span><span class="sxs-lookup"><span data-stu-id="1be39-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="1be39-111">Para saber mais, confira https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="1be39-111">To know more, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="1be39-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1be39-112">EXAMPLES</span></span>

### <span data-ttu-id="1be39-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1be39-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="1be39-114">Adicione um novo enriquecimento com a chave "newKey" e o valor "newValue".</span><span class="sxs-lookup"><span data-stu-id="1be39-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="1be39-115">Esse novo enriquecimento é aplicado aos pontos de extremidade "endpoint1" e "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="1be39-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="1be39-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1be39-116">PARAMETERS</span></span>

### <span data-ttu-id="1be39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be39-117">-DefaultProfile</span></span>
<span data-ttu-id="1be39-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1be39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be39-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="1be39-119">-Endpoint</span></span>
<span data-ttu-id="1be39-120">Pontos de extremidade para aplicar enriquecimentos.</span><span class="sxs-lookup"><span data-stu-id="1be39-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1be39-121">-InputObject</span></span>
<span data-ttu-id="1be39-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1be39-122">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-123">-Key</span><span class="sxs-lookup"><span data-stu-id="1be39-123">-Key</span></span>
<span data-ttu-id="1be39-124">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="1be39-124">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1be39-125">-Name</span></span>
<span data-ttu-id="1be39-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1be39-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be39-127">-ResourceGroupName</span></span>
<span data-ttu-id="1be39-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1be39-128">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1be39-129">-ResourceId</span></span>
<span data-ttu-id="1be39-130">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1be39-130">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-131">-Value</span><span class="sxs-lookup"><span data-stu-id="1be39-131">-Value</span></span>
<span data-ttu-id="1be39-132">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="1be39-132">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be39-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1be39-133">-Confirm</span></span>
<span data-ttu-id="1be39-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be39-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be39-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be39-135">-WhatIf</span></span>
<span data-ttu-id="1be39-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1be39-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be39-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1be39-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be39-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be39-138">CommonParameters</span></span>
<span data-ttu-id="1be39-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be39-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be39-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be39-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be39-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1be39-141">INPUTS</span></span>

### <span data-ttu-id="1be39-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1be39-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1be39-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1be39-143">System.String</span></span>

## <span data-ttu-id="1be39-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1be39-144">OUTPUTS</span></span>

### <span data-ttu-id="1be39-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1be39-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="1be39-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="1be39-146">NOTES</span></span>

## <span data-ttu-id="1be39-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1be39-147">RELATED LINKS</span></span>
