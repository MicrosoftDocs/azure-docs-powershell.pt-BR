---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: f7f163326c0ade9b2837bd732eded2ea67731fea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892491"
---
# <span data-ttu-id="58e11-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="58e11-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="58e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e11-102">SYNOPSIS</span></span>
<span data-ttu-id="58e11-103">Exclua um enriquecimento de mensagens em seu hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="58e11-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="58e11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="58e11-104">SYNTAX</span></span>

### <span data-ttu-id="58e11-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="58e11-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e11-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58e11-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e11-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58e11-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e11-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="58e11-108">DESCRIPTION</span></span>
<span data-ttu-id="58e11-109">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="58e11-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="58e11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58e11-110">EXAMPLES</span></span>

### <span data-ttu-id="58e11-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58e11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="58e11-112">Exclui o enriquecimento de mensagens "newKey".</span><span class="sxs-lookup"><span data-stu-id="58e11-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="58e11-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="58e11-113">PARAMETERS</span></span>

### <span data-ttu-id="58e11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e11-114">-DefaultProfile</span></span>
<span data-ttu-id="58e11-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58e11-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e11-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e11-116">-InputObject</span></span>
<span data-ttu-id="58e11-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="58e11-117">IotHub object</span></span>

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

### <span data-ttu-id="58e11-118">-Key</span><span class="sxs-lookup"><span data-stu-id="58e11-118">-Key</span></span>
<span data-ttu-id="58e11-119">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="58e11-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="58e11-120">-Name</span><span class="sxs-lookup"><span data-stu-id="58e11-120">-Name</span></span>
<span data-ttu-id="58e11-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="58e11-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="58e11-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58e11-122">-PassThru</span></span>
<span data-ttu-id="58e11-123">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="58e11-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="58e11-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="58e11-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58e11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e11-125">-ResourceGroupName</span></span>
<span data-ttu-id="58e11-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="58e11-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58e11-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e11-127">-ResourceId</span></span>
<span data-ttu-id="58e11-128">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="58e11-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="58e11-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e11-129">-Confirm</span></span>
<span data-ttu-id="58e11-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58e11-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e11-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e11-131">-WhatIf</span></span>
<span data-ttu-id="58e11-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58e11-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e11-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58e11-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e11-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e11-134">CommonParameters</span></span>
<span data-ttu-id="58e11-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e11-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e11-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e11-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e11-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58e11-137">INPUTS</span></span>

### <span data-ttu-id="58e11-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="58e11-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58e11-139">System.String</span><span class="sxs-lookup"><span data-stu-id="58e11-139">System.String</span></span>

## <span data-ttu-id="58e11-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="58e11-140">OUTPUTS</span></span>

### <span data-ttu-id="58e11-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58e11-141">System.Boolean</span></span>

## <span data-ttu-id="58e11-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="58e11-142">NOTES</span></span>

## <span data-ttu-id="58e11-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58e11-143">RELATED LINKS</span></span>
