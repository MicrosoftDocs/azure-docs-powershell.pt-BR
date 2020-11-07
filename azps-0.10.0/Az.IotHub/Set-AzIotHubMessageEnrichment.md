---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 4ecbbe9f37e4a2adf8d5ae5a06ef631d7a3b34cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775812"
---
# <span data-ttu-id="1bb4e-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1bb4e-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="1bb4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb4e-103">Atualize uma mensagem aprimorada no seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="1bb4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bb4e-104">SYNTAX</span></span>

### <span data-ttu-id="1bb4e-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1bb4e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb4e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1bb4e-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb4e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="1bb4e-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb4e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bb4e-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb4e-109">Para obter uma explicação detalhada dos aprimoramentos de mensagens no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="1bb4e-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="1bb4e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bb4e-110">EXAMPLES</span></span>

### <span data-ttu-id="1bb4e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bb4e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="1bb4e-112">Atualiza o valor de encompletamento para "UpdatedValue" para a chave "newKey".</span><span class="sxs-lookup"><span data-stu-id="1bb4e-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="1bb4e-113">Para obter uma explicação detalhada dos aprimoramentos de mensagens no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="1bb4e-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="1bb4e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1bb4e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="1bb4e-115">Atualiza o ponto de extremidade do encompletamento para "endpoint1, endpoint2, endpoint3" para a chave "newKey".</span><span class="sxs-lookup"><span data-stu-id="1bb4e-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="1bb4e-116">Para obter uma explicação detalhada dos aprimoramentos de mensagens no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="1bb4e-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="1bb4e-117">OS</span><span class="sxs-lookup"><span data-stu-id="1bb4e-117">PARAMETERS</span></span>

### <span data-ttu-id="1bb4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb4e-118">-DefaultProfile</span></span>
<span data-ttu-id="1bb4e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb4e-120">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="1bb4e-120">-Endpoint</span></span>
<span data-ttu-id="1bb4e-121">Ponto (s) para aplicar aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="1bb4e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb4e-122">-InputObject</span></span>
<span data-ttu-id="1bb4e-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1bb4e-123">IotHub Object</span></span>

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

### <span data-ttu-id="1bb4e-124">-Chave</span><span class="sxs-lookup"><span data-stu-id="1bb4e-124">-Key</span></span>
<span data-ttu-id="1bb4e-125">A chave do encompletamento.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="1bb4e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bb4e-126">-Name</span></span>
<span data-ttu-id="1bb4e-127">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="1bb4e-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1bb4e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb4e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1bb4e-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1bb4e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1bb4e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb4e-130">-ResourceId</span></span>
<span data-ttu-id="1bb4e-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1bb4e-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1bb4e-132">-Valor</span><span class="sxs-lookup"><span data-stu-id="1bb4e-132">-Value</span></span>
<span data-ttu-id="1bb4e-133">O valor do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="1bb4e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bb4e-134">-Confirm</span></span>
<span data-ttu-id="1bb4e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb4e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb4e-136">-WhatIf</span></span>
<span data-ttu-id="1bb4e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb4e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb4e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb4e-139">CommonParameters</span></span>
<span data-ttu-id="1bb4e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb4e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb4e-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb4e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb4e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bb4e-142">INPUTS</span></span>

### <span data-ttu-id="1bb4e-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1bb4e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1bb4e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb4e-144">System.String</span></span>

## <span data-ttu-id="1bb4e-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bb4e-145">OUTPUTS</span></span>

### <span data-ttu-id="1bb4e-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1bb4e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="1bb4e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bb4e-147">NOTES</span></span>

## <span data-ttu-id="1bb4e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bb4e-148">RELATED LINKS</span></span>