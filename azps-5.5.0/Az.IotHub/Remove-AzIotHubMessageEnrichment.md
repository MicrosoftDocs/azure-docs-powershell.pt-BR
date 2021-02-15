---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114821"
---
# <span data-ttu-id="3fa94-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3fa94-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="3fa94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fa94-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa94-103">Exclua um enriquecimento de mensagens no hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="3fa94-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="3fa94-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa94-104">SYNTAX</span></span>

### <span data-ttu-id="3fa94-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3fa94-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa94-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fa94-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa94-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3fa94-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa94-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa94-108">DESCRIPTION</span></span>
<span data-ttu-id="3fa94-109">Para uma explicação detalhada dos enriquecimentos de mensagens no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3fa94-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3fa94-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3fa94-110">EXAMPLES</span></span>

### <span data-ttu-id="3fa94-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3fa94-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="3fa94-112">Exclui o enriquecimento de mensagens "newKey".</span><span class="sxs-lookup"><span data-stu-id="3fa94-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="3fa94-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fa94-113">PARAMETERS</span></span>

### <span data-ttu-id="3fa94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa94-114">-DefaultProfile</span></span>
<span data-ttu-id="3fa94-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa94-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa94-116">-InputObject</span></span>
<span data-ttu-id="3fa94-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3fa94-117">IotHub object</span></span>

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

### <span data-ttu-id="3fa94-118">-Tecla</span><span class="sxs-lookup"><span data-stu-id="3fa94-118">-Key</span></span>
<span data-ttu-id="3fa94-119">A chave do enriquecimento.</span><span class="sxs-lookup"><span data-stu-id="3fa94-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="3fa94-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fa94-120">-Name</span></span>
<span data-ttu-id="3fa94-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="3fa94-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3fa94-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa94-122">-PassThru</span></span>
<span data-ttu-id="3fa94-123">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="3fa94-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="3fa94-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="3fa94-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fa94-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa94-125">-ResourceGroupName</span></span>
<span data-ttu-id="3fa94-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3fa94-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3fa94-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa94-127">-ResourceId</span></span>
<span data-ttu-id="3fa94-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="3fa94-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3fa94-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3fa94-129">-Confirm</span></span>
<span data-ttu-id="3fa94-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fa94-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa94-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa94-131">-WhatIf</span></span>
<span data-ttu-id="3fa94-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3fa94-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa94-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fa94-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa94-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa94-134">CommonParameters</span></span>
<span data-ttu-id="3fa94-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa94-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa94-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa94-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa94-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="3fa94-137">INPUTS</span></span>

### <span data-ttu-id="3fa94-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3fa94-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3fa94-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3fa94-139">System.String</span></span>

## <span data-ttu-id="3fa94-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="3fa94-140">OUTPUTS</span></span>

### <span data-ttu-id="3fa94-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fa94-141">System.Boolean</span></span>

## <span data-ttu-id="3fa94-142">Notas</span><span class="sxs-lookup"><span data-stu-id="3fa94-142">NOTES</span></span>

## <span data-ttu-id="3fa94-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fa94-143">RELATED LINKS</span></span>
