---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943819"
---
# <span data-ttu-id="5abf8-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="5abf8-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="5abf8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5abf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5abf8-103">Invocar um método de módulo de borda.</span><span class="sxs-lookup"><span data-stu-id="5abf8-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="5abf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5abf8-104">SYNTAX</span></span>

### <span data-ttu-id="5abf8-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5abf8-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5abf8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5abf8-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5abf8-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5abf8-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5abf8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5abf8-108">DESCRIPTION</span></span>
<span data-ttu-id="5abf8-109">Invocar um método de módulo de borda.</span><span class="sxs-lookup"><span data-stu-id="5abf8-109">Invoke an Edge module method.</span></span> <span data-ttu-id="5abf8-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5abf8-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="5abf8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5abf8-111">EXAMPLES</span></span>

### <span data-ttu-id="5abf8-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5abf8-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="5abf8-113">Invocar um método de módulo de borda.</span><span class="sxs-lookup"><span data-stu-id="5abf8-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="5abf8-114">OS</span><span class="sxs-lookup"><span data-stu-id="5abf8-114">PARAMETERS</span></span>

### <span data-ttu-id="5abf8-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="5abf8-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="5abf8-116">Número de segundos para esperar até que uma conexão seja feita com êxito.</span><span class="sxs-lookup"><span data-stu-id="5abf8-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="5abf8-117">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="5abf8-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abf8-118">-DefaultProfile</span></span>
<span data-ttu-id="5abf8-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5abf8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="5abf8-120">-DeviceId</span></span>
<span data-ttu-id="5abf8-121">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5abf8-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5abf8-122">-InputObject</span></span>
<span data-ttu-id="5abf8-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="5abf8-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5abf8-124">-IotHubName</span></span>
<span data-ttu-id="5abf8-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="5abf8-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-126">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="5abf8-126">-ModuleId</span></span>
<span data-ttu-id="5abf8-127">ID do módulo do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5abf8-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5abf8-128">-Name</span></span>
<span data-ttu-id="5abf8-129">O nome do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5abf8-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="5abf8-130">-Payload</span></span>
<span data-ttu-id="5abf8-131">A carga do método a ser invocado neste módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5abf8-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5abf8-132">-ResourceGroupName</span></span>
<span data-ttu-id="5abf8-133">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5abf8-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5abf8-134">-ResourceId</span></span>
<span data-ttu-id="5abf8-135">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="5abf8-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="5abf8-136">-ResponseTimeOut</span></span>
<span data-ttu-id="5abf8-137">Número de segundos para esperar até que um resultado seja recebido do método direto.</span><span class="sxs-lookup"><span data-stu-id="5abf8-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="5abf8-138">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="5abf8-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5abf8-139">-Confirm</span></span>
<span data-ttu-id="5abf8-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5abf8-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5abf8-141">-WhatIf</span></span>
<span data-ttu-id="5abf8-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5abf8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5abf8-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5abf8-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abf8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abf8-144">CommonParameters</span></span>
<span data-ttu-id="5abf8-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5abf8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5abf8-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5abf8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abf8-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5abf8-147">INPUTS</span></span>

### <span data-ttu-id="5abf8-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5abf8-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5abf8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5abf8-149">System.String</span></span>

## <span data-ttu-id="5abf8-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5abf8-150">OUTPUTS</span></span>

### <span data-ttu-id="5abf8-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="5abf8-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="5abf8-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5abf8-152">NOTES</span></span>

## <span data-ttu-id="5abf8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5abf8-153">RELATED LINKS</span></span>
