---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 4c3782496041be7328ede29fad5ab3818791a0be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886754"
---
# <span data-ttu-id="7a8a9-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="7a8a9-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="7a8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8a9-103">Invocar um método direto em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="7a8a9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a8a9-104">SYNTAX</span></span>

### <span data-ttu-id="7a8a9-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a8a9-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a8a9-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a8a9-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a8a9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a8a9-108">DESCRIPTION</span></span>
<span data-ttu-id="7a8a9-109">Invocar um método direto em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="7a8a9-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="7a8a9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-111">EXAMPLES</span></span>

### <span data-ttu-id="7a8a9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a8a9-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="7a8a9-113">Invocar um método de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-113">Invoke a device method.</span></span>

## <span data-ttu-id="7a8a9-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-114">PARAMETERS</span></span>

### <span data-ttu-id="7a8a9-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="7a8a9-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="7a8a9-116">Número de segundos para aguardar até que uma conexão seja feita com êxito.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="7a8a9-117">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-117">Default is 10.</span></span>

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

### <span data-ttu-id="7a8a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8a9-118">-DefaultProfile</span></span>
<span data-ttu-id="7a8a9-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8a9-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7a8a9-120">-DeviceId</span></span>
<span data-ttu-id="7a8a9-121">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-121">Target Device Id.</span></span>

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

### <span data-ttu-id="7a8a9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a8a9-122">-InputObject</span></span>
<span data-ttu-id="7a8a9-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7a8a9-123">IotHub object</span></span>

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

### <span data-ttu-id="7a8a9-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7a8a9-124">-IotHubName</span></span>
<span data-ttu-id="7a8a9-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="7a8a9-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7a8a9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7a8a9-126">-Name</span></span>
<span data-ttu-id="7a8a9-127">O nome do método a ser invocado neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7a8a9-128">-Carga</span><span class="sxs-lookup"><span data-stu-id="7a8a9-128">-Payload</span></span>
<span data-ttu-id="7a8a9-129">A carga do método a ser invocado neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7a8a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="7a8a9-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7a8a9-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a8a9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a8a9-132">-ResourceId</span></span>
<span data-ttu-id="7a8a9-133">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7a8a9-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7a8a9-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="7a8a9-134">-ResponseTimeOut</span></span>
<span data-ttu-id="7a8a9-135">Número de segundos para aguardar até que um resultado seja recebido do método direto.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="7a8a9-136">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-136">Default is 10.</span></span>

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

### <span data-ttu-id="7a8a9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a8a9-137">-Confirm</span></span>
<span data-ttu-id="7a8a9-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8a9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8a9-139">-WhatIf</span></span>
<span data-ttu-id="7a8a9-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8a9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8a9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8a9-142">CommonParameters</span></span>
<span data-ttu-id="7a8a9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8a9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8a9-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a8a9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8a9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-145">INPUTS</span></span>

### <span data-ttu-id="7a8a9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7a8a9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7a8a9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8a9-147">System.String</span></span>

## <span data-ttu-id="7a8a9-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-148">OUTPUTS</span></span>

### <span data-ttu-id="7a8a9-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="7a8a9-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="7a8a9-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a8a9-150">NOTES</span></span>

## <span data-ttu-id="7a8a9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a8a9-151">RELATED LINKS</span></span>
