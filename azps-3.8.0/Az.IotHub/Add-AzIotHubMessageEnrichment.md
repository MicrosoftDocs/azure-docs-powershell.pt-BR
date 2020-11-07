---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777358"
---
# <span data-ttu-id="29ab4-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="29ab4-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="29ab4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="29ab4-103">Cria uma mensagem aprimorada para pontos de extremidade escolhidos em seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="29ab4-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="29ab4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29ab4-104">SYNTAX</span></span>

### <span data-ttu-id="29ab4-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="29ab4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ab4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29ab4-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29ab4-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="29ab4-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ab4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29ab4-108">DESCRIPTION</span></span>
<span data-ttu-id="29ab4-109">Adicione até 10 mensagens de aprimoramento por Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="29ab4-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="29ab4-110">Elas são adicionadas como propriedades do aplicativo às mensagens enviadas a pontos de extremidade escolhidos.</span><span class="sxs-lookup"><span data-stu-id="29ab4-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="29ab4-111">Para saber mais, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="29ab4-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="29ab4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29ab4-112">EXAMPLES</span></span>

### <span data-ttu-id="29ab4-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29ab4-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="29ab4-114">Adicione uma nova enriquecimento com a chave "newKey" e o valor "newValue".</span><span class="sxs-lookup"><span data-stu-id="29ab4-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="29ab4-115">Esta nova enriquecimento é aplicada a pontos de extremidade "endpoint1" e "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="29ab4-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="29ab4-116">OS</span><span class="sxs-lookup"><span data-stu-id="29ab4-116">PARAMETERS</span></span>

### <span data-ttu-id="29ab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ab4-117">-DefaultProfile</span></span>
<span data-ttu-id="29ab4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29ab4-119">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="29ab4-119">-Endpoint</span></span>
<span data-ttu-id="29ab4-120">Ponto (s) para aplicar aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="29ab4-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="29ab4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29ab4-121">-InputObject</span></span>
<span data-ttu-id="29ab4-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="29ab4-122">IotHub object</span></span>

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

### <span data-ttu-id="29ab4-123">-Chave</span><span class="sxs-lookup"><span data-stu-id="29ab4-123">-Key</span></span>
<span data-ttu-id="29ab4-124">A chave do encompletamento.</span><span class="sxs-lookup"><span data-stu-id="29ab4-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="29ab4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="29ab4-125">-Name</span></span>
<span data-ttu-id="29ab4-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="29ab4-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="29ab4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ab4-127">-ResourceGroupName</span></span>
<span data-ttu-id="29ab4-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="29ab4-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29ab4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ab4-129">-ResourceId</span></span>
<span data-ttu-id="29ab4-130">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="29ab4-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="29ab4-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="29ab4-131">-Value</span></span>
<span data-ttu-id="29ab4-132">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="29ab4-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="29ab4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29ab4-133">-Confirm</span></span>
<span data-ttu-id="29ab4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29ab4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ab4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ab4-135">-WhatIf</span></span>
<span data-ttu-id="29ab4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29ab4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ab4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29ab4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ab4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ab4-138">CommonParameters</span></span>
<span data-ttu-id="29ab4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ab4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ab4-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ab4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ab4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29ab4-141">INPUTS</span></span>

### <span data-ttu-id="29ab4-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="29ab4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="29ab4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="29ab4-143">System.String</span></span>

## <span data-ttu-id="29ab4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29ab4-144">OUTPUTS</span></span>

### <span data-ttu-id="29ab4-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="29ab4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="29ab4-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29ab4-146">NOTES</span></span>

## <span data-ttu-id="29ab4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29ab4-147">RELATED LINKS</span></span>
