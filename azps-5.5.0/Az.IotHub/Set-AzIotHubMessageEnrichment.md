---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111842"
---
# <span data-ttu-id="29d49-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="29d49-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="29d49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29d49-102">SYNOPSIS</span></span>
<span data-ttu-id="29d49-103">Atualize o enriquecimento de mensagens em seu hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="29d49-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="29d49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29d49-104">SYNTAX</span></span>

### <span data-ttu-id="29d49-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29d49-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d49-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29d49-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d49-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29d49-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d49-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="29d49-108">DESCRIPTION</span></span>
<span data-ttu-id="29d49-109">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="29d49-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="29d49-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29d49-110">EXAMPLES</span></span>

### <span data-ttu-id="29d49-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29d49-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="29d49-112">Atualiza o valor do enriquecimento para "updatedValue" para a chave "newKey".</span><span class="sxs-lookup"><span data-stu-id="29d49-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="29d49-113">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="29d49-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="29d49-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29d49-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="29d49-115">Atualiza o ponto de extremidade do enriquecimento para "ponto de extremidade1, ponto de extremidade2, ponto de extremidade3" para a chave "newKey".</span><span class="sxs-lookup"><span data-stu-id="29d49-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="29d49-116">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="29d49-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="29d49-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29d49-117">PARAMETERS</span></span>

### <span data-ttu-id="29d49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d49-118">-DefaultProfile</span></span>
<span data-ttu-id="29d49-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29d49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d49-120">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="29d49-120">-Endpoint</span></span>
<span data-ttu-id="29d49-121">Pontos de extremidade para aplicar enriquecimentos.</span><span class="sxs-lookup"><span data-stu-id="29d49-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d49-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29d49-122">-InputObject</span></span>
<span data-ttu-id="29d49-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="29d49-123">IotHub Object</span></span>

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

### <span data-ttu-id="29d49-124">-Tecla</span><span class="sxs-lookup"><span data-stu-id="29d49-124">-Key</span></span>
<span data-ttu-id="29d49-125">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="29d49-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="29d49-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="29d49-126">-Name</span></span>
<span data-ttu-id="29d49-127">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="29d49-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="29d49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d49-128">-ResourceGroupName</span></span>
<span data-ttu-id="29d49-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="29d49-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29d49-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29d49-130">-ResourceId</span></span>
<span data-ttu-id="29d49-131">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="29d49-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="29d49-132">-Valor</span><span class="sxs-lookup"><span data-stu-id="29d49-132">-Value</span></span>
<span data-ttu-id="29d49-133">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="29d49-133">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d49-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="29d49-134">-Confirm</span></span>
<span data-ttu-id="29d49-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29d49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d49-136">-WhatIf</span></span>
<span data-ttu-id="29d49-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="29d49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d49-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29d49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d49-139">CommonParameters</span></span>
<span data-ttu-id="29d49-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d49-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d49-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d49-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="29d49-142">INPUTS</span></span>

### <span data-ttu-id="29d49-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="29d49-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="29d49-144">System.String</span><span class="sxs-lookup"><span data-stu-id="29d49-144">System.String</span></span>

## <span data-ttu-id="29d49-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="29d49-145">OUTPUTS</span></span>

### <span data-ttu-id="29d49-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEntricmentMetadata</span><span class="sxs-lookup"><span data-stu-id="29d49-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="29d49-147">Notas</span><span class="sxs-lookup"><span data-stu-id="29d49-147">NOTES</span></span>

## <span data-ttu-id="29d49-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29d49-148">RELATED LINKS</span></span>
