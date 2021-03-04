---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: ea2362fc779ada8faf62c863ccffb9e58e078b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889931"
---
# <span data-ttu-id="57ada-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="57ada-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="57ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ada-102">SYNOPSIS</span></span>
<span data-ttu-id="57ada-103">Invocar um método de módulo de Borda.</span><span class="sxs-lookup"><span data-stu-id="57ada-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="57ada-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57ada-104">SYNTAX</span></span>

### <span data-ttu-id="57ada-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57ada-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57ada-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57ada-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57ada-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="57ada-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57ada-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57ada-108">DESCRIPTION</span></span>
<span data-ttu-id="57ada-109">Invocar um método de módulo de Borda.</span><span class="sxs-lookup"><span data-stu-id="57ada-109">Invoke an Edge module method.</span></span> <span data-ttu-id="57ada-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods mais informações.</span><span class="sxs-lookup"><span data-stu-id="57ada-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="57ada-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57ada-111">EXAMPLES</span></span>

### <span data-ttu-id="57ada-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57ada-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="57ada-113">Invocar um método de módulo de Borda.</span><span class="sxs-lookup"><span data-stu-id="57ada-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="57ada-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57ada-114">PARAMETERS</span></span>

### <span data-ttu-id="57ada-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="57ada-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="57ada-116">Número de segundos para aguardar até que uma conexão seja feita com êxito.</span><span class="sxs-lookup"><span data-stu-id="57ada-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="57ada-117">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="57ada-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ada-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ada-118">-DefaultProfile</span></span>
<span data-ttu-id="57ada-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57ada-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ada-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="57ada-120">-DeviceId</span></span>
<span data-ttu-id="57ada-121">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="57ada-121">Target Device Id.</span></span>

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

### <span data-ttu-id="57ada-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ada-122">-InputObject</span></span>
<span data-ttu-id="57ada-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="57ada-123">IotHub object</span></span>

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

### <span data-ttu-id="57ada-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="57ada-124">-IotHubName</span></span>
<span data-ttu-id="57ada-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="57ada-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="57ada-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="57ada-126">-ModuleId</span></span>
<span data-ttu-id="57ada-127">ID do módulo do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="57ada-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ada-128">-Name</span><span class="sxs-lookup"><span data-stu-id="57ada-128">-Name</span></span>
<span data-ttu-id="57ada-129">O nome do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57ada-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="57ada-130">-Carga</span><span class="sxs-lookup"><span data-stu-id="57ada-130">-Payload</span></span>
<span data-ttu-id="57ada-131">A carga do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57ada-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="57ada-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ada-132">-ResourceGroupName</span></span>
<span data-ttu-id="57ada-133">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="57ada-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="57ada-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57ada-134">-ResourceId</span></span>
<span data-ttu-id="57ada-135">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="57ada-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="57ada-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="57ada-136">-ResponseTimeOut</span></span>
<span data-ttu-id="57ada-137">Número de segundos para aguardar até que um resultado seja recebido do método direto.</span><span class="sxs-lookup"><span data-stu-id="57ada-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="57ada-138">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="57ada-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ada-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57ada-139">-Confirm</span></span>
<span data-ttu-id="57ada-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ada-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ada-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ada-141">-WhatIf</span></span>
<span data-ttu-id="57ada-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57ada-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ada-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57ada-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ada-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ada-144">CommonParameters</span></span>
<span data-ttu-id="57ada-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ada-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ada-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ada-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ada-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57ada-147">INPUTS</span></span>

### <span data-ttu-id="57ada-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="57ada-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="57ada-149">System.String</span><span class="sxs-lookup"><span data-stu-id="57ada-149">System.String</span></span>

## <span data-ttu-id="57ada-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57ada-150">OUTPUTS</span></span>

### <span data-ttu-id="57ada-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="57ada-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="57ada-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="57ada-152">NOTES</span></span>

## <span data-ttu-id="57ada-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57ada-153">RELATED LINKS</span></span>
