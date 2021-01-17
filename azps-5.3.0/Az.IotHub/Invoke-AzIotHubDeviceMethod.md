---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433628"
---
# <span data-ttu-id="a7da4-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="a7da4-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="a7da4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7da4-102">SYNOPSIS</span></span>
<span data-ttu-id="a7da4-103">Invocar um método direto em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7da4-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="a7da4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7da4-104">SYNTAX</span></span>

### <span data-ttu-id="a7da4-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7da4-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7da4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7da4-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7da4-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="a7da4-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7da4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7da4-108">DESCRIPTION</span></span>
<span data-ttu-id="a7da4-109">Invocar um método direto em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7da4-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="a7da4-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a7da4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="a7da4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7da4-111">EXAMPLES</span></span>

### <span data-ttu-id="a7da4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7da4-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="a7da4-113">Invocar um método de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7da4-113">Invoke a device method.</span></span>

## <span data-ttu-id="a7da4-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7da4-114">PARAMETERS</span></span>

### <span data-ttu-id="a7da4-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="a7da4-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="a7da4-116">Número de segundos para esperar até que uma conexão seja feita com êxito.</span><span class="sxs-lookup"><span data-stu-id="a7da4-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="a7da4-117">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a7da4-117">Default is 10.</span></span>

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

### <span data-ttu-id="a7da4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7da4-118">-DefaultProfile</span></span>
<span data-ttu-id="a7da4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7da4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7da4-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="a7da4-120">-DeviceId</span></span>
<span data-ttu-id="a7da4-121">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a7da4-121">Target Device Id.</span></span>

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

### <span data-ttu-id="a7da4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7da4-122">-InputObject</span></span>
<span data-ttu-id="a7da4-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a7da4-123">IotHub object</span></span>

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

### <span data-ttu-id="a7da4-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a7da4-124">-IotHubName</span></span>
<span data-ttu-id="a7da4-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a7da4-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a7da4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7da4-126">-Name</span></span>
<span data-ttu-id="a7da4-127">O nome do método a ser invocado nesse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7da4-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="a7da4-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="a7da4-128">-Payload</span></span>
<span data-ttu-id="a7da4-129">A carga do método a ser invocado nesse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7da4-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="a7da4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7da4-130">-ResourceGroupName</span></span>
<span data-ttu-id="a7da4-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a7da4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a7da4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7da4-132">-ResourceId</span></span>
<span data-ttu-id="a7da4-133">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="a7da4-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a7da4-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="a7da4-134">-ResponseTimeOut</span></span>
<span data-ttu-id="a7da4-135">Número de segundos para esperar até que um resultado seja recebido do método direto.</span><span class="sxs-lookup"><span data-stu-id="a7da4-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="a7da4-136">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a7da4-136">Default is 10.</span></span>

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

### <span data-ttu-id="a7da4-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7da4-137">-Confirm</span></span>
<span data-ttu-id="a7da4-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7da4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7da4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7da4-139">-WhatIf</span></span>
<span data-ttu-id="a7da4-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7da4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7da4-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7da4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7da4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7da4-142">CommonParameters</span></span>
<span data-ttu-id="a7da4-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7da4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7da4-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7da4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7da4-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7da4-145">INPUTS</span></span>

### <span data-ttu-id="a7da4-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a7da4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a7da4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a7da4-147">System.String</span></span>

## <span data-ttu-id="a7da4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7da4-148">OUTPUTS</span></span>

### <span data-ttu-id="a7da4-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="a7da4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="a7da4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7da4-150">NOTES</span></span>

## <span data-ttu-id="a7da4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7da4-151">RELATED LINKS</span></span>
