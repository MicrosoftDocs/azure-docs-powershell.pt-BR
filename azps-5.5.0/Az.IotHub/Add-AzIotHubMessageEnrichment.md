---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113778"
---
# <span data-ttu-id="4d203-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4d203-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="4d203-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d203-102">SYNOPSIS</span></span>
<span data-ttu-id="4d203-103">Cria um enriquecimento de mensagens para pontos de extremidade escolhidos em seu Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="4d203-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="4d203-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d203-104">SYNTAX</span></span>

### <span data-ttu-id="4d203-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d203-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d203-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d203-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d203-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d203-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d203-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d203-108">DESCRIPTION</span></span>
<span data-ttu-id="4d203-109">Adicione até 10 enriquecimentos de mensagens por Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="4d203-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="4d203-110">Elas são adicionadas como propriedades do aplicativo às mensagens enviadas para os pontos de extremidade escolhidos.</span><span class="sxs-lookup"><span data-stu-id="4d203-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="4d203-111">Para saber mais, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="4d203-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="4d203-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d203-112">EXAMPLES</span></span>

### <span data-ttu-id="4d203-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d203-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="4d203-114">Adicione um novo enriquecimento com a chave "newKey" e o valor "newValue".</span><span class="sxs-lookup"><span data-stu-id="4d203-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="4d203-115">Esse novo enriquecimento é aplicado aos pontos de extremidade "ponto de extremidade1" e "ponto de extremidade2".</span><span class="sxs-lookup"><span data-stu-id="4d203-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="4d203-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d203-116">PARAMETERS</span></span>

### <span data-ttu-id="4d203-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d203-117">-DefaultProfile</span></span>
<span data-ttu-id="4d203-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d203-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d203-119">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="4d203-119">-Endpoint</span></span>
<span data-ttu-id="4d203-120">Pontos de extremidade para aplicar enriquecimentos.</span><span class="sxs-lookup"><span data-stu-id="4d203-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="4d203-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d203-121">-InputObject</span></span>
<span data-ttu-id="4d203-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4d203-122">IotHub object</span></span>

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

### <span data-ttu-id="4d203-123">-Tecla</span><span class="sxs-lookup"><span data-stu-id="4d203-123">-Key</span></span>
<span data-ttu-id="4d203-124">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="4d203-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="4d203-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d203-125">-Name</span></span>
<span data-ttu-id="4d203-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="4d203-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4d203-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d203-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d203-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4d203-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4d203-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d203-129">-ResourceId</span></span>
<span data-ttu-id="4d203-130">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="4d203-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4d203-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="4d203-131">-Value</span></span>
<span data-ttu-id="4d203-132">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="4d203-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="4d203-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4d203-133">-Confirm</span></span>
<span data-ttu-id="4d203-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d203-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d203-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d203-135">-WhatIf</span></span>
<span data-ttu-id="4d203-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4d203-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d203-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d203-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d203-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d203-138">CommonParameters</span></span>
<span data-ttu-id="4d203-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d203-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d203-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d203-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d203-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d203-141">INPUTS</span></span>

### <span data-ttu-id="4d203-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4d203-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4d203-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4d203-143">System.String</span></span>

## <span data-ttu-id="4d203-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d203-144">OUTPUTS</span></span>

### <span data-ttu-id="4d203-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEntricmentMetadata</span><span class="sxs-lookup"><span data-stu-id="4d203-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="4d203-146">Notas</span><span class="sxs-lookup"><span data-stu-id="4d203-146">NOTES</span></span>

## <span data-ttu-id="4d203-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d203-147">RELATED LINKS</span></span>
