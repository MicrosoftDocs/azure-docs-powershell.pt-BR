---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: fa3e46db14c7bba17ba87813285d0f7b119dc6c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596291"
---
# <span data-ttu-id="2a067-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2a067-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="2a067-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a067-102">SYNOPSIS</span></span>
<span data-ttu-id="2a067-103">Cria uma mensagem aprimorada para pontos de extremidade escolhidos em seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2a067-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="2a067-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a067-104">SYNTAX</span></span>

### <span data-ttu-id="2a067-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a067-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a067-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a067-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a067-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="2a067-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a067-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a067-108">DESCRIPTION</span></span>
<span data-ttu-id="2a067-109">Adicione até 10 mensagens de aprimoramento por Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2a067-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="2a067-110">Elas são adicionadas como propriedades do aplicativo às mensagens enviadas a pontos de extremidade escolhidos.</span><span class="sxs-lookup"><span data-stu-id="2a067-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="2a067-111">Para saber mais, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="2a067-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="2a067-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a067-112">EXAMPLES</span></span>

### <span data-ttu-id="2a067-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a067-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="2a067-114">Adicione uma nova enriquecimento com a chave "newKey" e o valor "newValue".</span><span class="sxs-lookup"><span data-stu-id="2a067-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="2a067-115">Esta nova enriquecimento é aplicada a pontos de extremidade "endpoint1" e "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="2a067-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="2a067-116">OS</span><span class="sxs-lookup"><span data-stu-id="2a067-116">PARAMETERS</span></span>

### <span data-ttu-id="2a067-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a067-117">-DefaultProfile</span></span>
<span data-ttu-id="2a067-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a067-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a067-119">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="2a067-119">-Endpoint</span></span>
<span data-ttu-id="2a067-120">Ponto (s) para aplicar aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="2a067-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="2a067-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a067-121">-InputObject</span></span>
<span data-ttu-id="2a067-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="2a067-122">IotHub object</span></span>

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

### <span data-ttu-id="2a067-123">-Chave</span><span class="sxs-lookup"><span data-stu-id="2a067-123">-Key</span></span>
<span data-ttu-id="2a067-124">A chave do encompletamento.</span><span class="sxs-lookup"><span data-stu-id="2a067-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="2a067-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a067-125">-Name</span></span>
<span data-ttu-id="2a067-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="2a067-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2a067-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a067-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a067-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2a067-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2a067-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a067-129">-ResourceId</span></span>
<span data-ttu-id="2a067-130">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="2a067-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2a067-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="2a067-131">-Value</span></span>
<span data-ttu-id="2a067-132">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="2a067-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="2a067-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a067-133">-Confirm</span></span>
<span data-ttu-id="2a067-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a067-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a067-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a067-135">-WhatIf</span></span>
<span data-ttu-id="2a067-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a067-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a067-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a067-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a067-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a067-138">CommonParameters</span></span>
<span data-ttu-id="2a067-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a067-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a067-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a067-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a067-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a067-141">INPUTS</span></span>

### <span data-ttu-id="2a067-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2a067-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2a067-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2a067-143">System.String</span></span>

## <span data-ttu-id="2a067-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a067-144">OUTPUTS</span></span>

### <span data-ttu-id="2a067-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2a067-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="2a067-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a067-146">NOTES</span></span>

## <span data-ttu-id="2a067-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a067-147">RELATED LINKS</span></span>
