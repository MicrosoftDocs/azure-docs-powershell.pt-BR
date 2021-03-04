---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 6e03e6dcf5cce193452fd03cee1f48bc387335c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887730"
---
# <span data-ttu-id="d62de-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d62de-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="d62de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62de-102">SYNOPSIS</span></span>
<span data-ttu-id="d62de-103">Excluir módulos(s) em um dispositivo de IoT de destino em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="d62de-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d62de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d62de-104">SYNTAX</span></span>

### <span data-ttu-id="d62de-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d62de-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d62de-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d62de-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d62de-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d62de-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62de-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d62de-108">DESCRIPTION</span></span>
<span data-ttu-id="d62de-109">Excluir módulos(s) em um dispositivo de IoT de destino em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="d62de-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d62de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d62de-110">EXAMPLES</span></span>

### <span data-ttu-id="d62de-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d62de-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="d62de-112">Exclua um módulo de dispositivo Iot.</span><span class="sxs-lookup"><span data-stu-id="d62de-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="d62de-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d62de-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="d62de-114">Exclua todos os módulos de dispositivo Iot.</span><span class="sxs-lookup"><span data-stu-id="d62de-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="d62de-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d62de-115">PARAMETERS</span></span>

### <span data-ttu-id="d62de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62de-116">-DefaultProfile</span></span>
<span data-ttu-id="d62de-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d62de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d62de-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d62de-118">-DeviceId</span></span>
<span data-ttu-id="d62de-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d62de-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d62de-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d62de-120">-InputObject</span></span>
<span data-ttu-id="d62de-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="d62de-121">IotHub object</span></span>

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

### <span data-ttu-id="d62de-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d62de-122">-IotHubName</span></span>
<span data-ttu-id="d62de-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="d62de-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d62de-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="d62de-124">-ModuleId</span></span>
<span data-ttu-id="d62de-125">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="d62de-125">Target Module Id.</span></span>

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

### <span data-ttu-id="d62de-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d62de-126">-PassThru</span></span>
<span data-ttu-id="d62de-127">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="d62de-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="d62de-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d62de-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d62de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62de-129">-ResourceGroupName</span></span>
<span data-ttu-id="d62de-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d62de-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d62de-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d62de-131">-ResourceId</span></span>
<span data-ttu-id="d62de-132">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="d62de-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d62de-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d62de-133">-Confirm</span></span>
<span data-ttu-id="d62de-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62de-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62de-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62de-135">-WhatIf</span></span>
<span data-ttu-id="d62de-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d62de-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d62de-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d62de-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62de-138">CommonParameters</span></span>
<span data-ttu-id="d62de-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62de-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62de-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62de-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d62de-141">INPUTS</span></span>

### <span data-ttu-id="d62de-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d62de-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d62de-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d62de-143">System.String</span></span>

## <span data-ttu-id="d62de-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d62de-144">OUTPUTS</span></span>

### <span data-ttu-id="d62de-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d62de-145">System.Boolean</span></span>

## <span data-ttu-id="d62de-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="d62de-146">NOTES</span></span>

## <span data-ttu-id="d62de-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d62de-147">RELATED LINKS</span></span>
