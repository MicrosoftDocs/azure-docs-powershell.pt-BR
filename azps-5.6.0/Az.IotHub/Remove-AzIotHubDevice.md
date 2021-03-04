---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 15a8f9aa8ed3c0746b402b29967999d395794fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892637"
---
# <span data-ttu-id="79b36-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="79b36-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="79b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b36-102">SYNOPSIS</span></span>
<span data-ttu-id="79b36-103">Exclua um dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="79b36-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="79b36-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79b36-104">SYNTAX</span></span>

### <span data-ttu-id="79b36-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79b36-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b36-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79b36-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79b36-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b36-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79b36-108">DESCRIPTION</span></span>
<span data-ttu-id="79b36-109">Exclua todos os dispositivos ou um dispositivo específico de um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="79b36-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="79b36-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79b36-110">EXAMPLES</span></span>

### <span data-ttu-id="79b36-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79b36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="79b36-112">Exclua todos os dispositivos Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="79b36-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="79b36-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="79b36-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="79b36-114">Exclua um dispositivo Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="79b36-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="79b36-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79b36-115">PARAMETERS</span></span>

### <span data-ttu-id="79b36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b36-116">-DefaultProfile</span></span>
<span data-ttu-id="79b36-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79b36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b36-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="79b36-118">-DeviceId</span></span>
<span data-ttu-id="79b36-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="79b36-119">Target Device Id.</span></span>

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

### <span data-ttu-id="79b36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79b36-120">-InputObject</span></span>
<span data-ttu-id="79b36-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="79b36-121">IotHub object</span></span>

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

### <span data-ttu-id="79b36-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="79b36-122">-IotHubName</span></span>
<span data-ttu-id="79b36-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="79b36-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="79b36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79b36-124">-PassThru</span></span>
<span data-ttu-id="79b36-125">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="79b36-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="79b36-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="79b36-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="79b36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b36-127">-ResourceGroupName</span></span>
<span data-ttu-id="79b36-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="79b36-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="79b36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b36-129">-ResourceId</span></span>
<span data-ttu-id="79b36-130">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="79b36-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="79b36-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b36-131">-Confirm</span></span>
<span data-ttu-id="79b36-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b36-133">-WhatIf</span></span>
<span data-ttu-id="79b36-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79b36-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b36-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79b36-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b36-136">CommonParameters</span></span>
<span data-ttu-id="79b36-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b36-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b36-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b36-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79b36-139">INPUTS</span></span>

### <span data-ttu-id="79b36-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="79b36-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="79b36-141">System.String</span><span class="sxs-lookup"><span data-stu-id="79b36-141">System.String</span></span>

## <span data-ttu-id="79b36-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79b36-142">OUTPUTS</span></span>

### <span data-ttu-id="79b36-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79b36-143">System.Boolean</span></span>

## <span data-ttu-id="79b36-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="79b36-144">NOTES</span></span>

## <span data-ttu-id="79b36-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79b36-145">RELATED LINKS</span></span>
