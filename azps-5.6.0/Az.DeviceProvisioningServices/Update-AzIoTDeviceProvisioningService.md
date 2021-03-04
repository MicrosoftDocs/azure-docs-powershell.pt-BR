---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889532"
---
# <span data-ttu-id="f4559-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="f4559-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="f4559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4559-102">SYNOPSIS</span></span>
<span data-ttu-id="f4559-103">Atualize um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f4559-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f4559-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4559-104">SYNTAX</span></span>

### <span data-ttu-id="f4559-105">ResourceUpdateSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4559-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4559-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f4559-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4559-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f4559-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4559-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f4559-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4559-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f4559-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4559-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f4559-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4559-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4559-111">DESCRIPTION</span></span>
<span data-ttu-id="f4559-112">Para uma introdução ao Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f4559-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f4559-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4559-113">EXAMPLES</span></span>

### <span data-ttu-id="f4559-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4559-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="f4559-115">Atualize a Política de Alocação para "GeoLatency" de um serviço de provisionamento de dispositivo do Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="f4559-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="f4559-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f4559-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="f4559-117">Adicione marcas a um serviço de provisionamento de dispositivo do Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="f4559-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="f4559-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f4559-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="f4559-119">Excluir Marca e adicionar novas marcas a um serviço de provisionamento de dispositivo do Azure IoT Hub "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4559-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="f4559-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4559-120">PARAMETERS</span></span>

### <span data-ttu-id="f4559-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="f4559-121">-AllocationPolicy</span></span>
<span data-ttu-id="f4559-122">Política de Alocação de Serviço de Provisionamento de Dispositivos IoT</span><span class="sxs-lookup"><span data-stu-id="f4559-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4559-123">-DefaultProfile</span></span>
<span data-ttu-id="f4559-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4559-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4559-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4559-125">-InputObject</span></span>
<span data-ttu-id="f4559-126">Objeto de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="f4559-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f4559-127">-Name</span></span>
<span data-ttu-id="f4559-128">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="f4559-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="f4559-129">-Reset</span></span>
<span data-ttu-id="f4559-130">Redefinir as marcas de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="f4559-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4559-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4559-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f4559-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4559-133">-ResourceId</span></span>
<span data-ttu-id="f4559-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="f4559-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4559-135">-Tag</span></span>
<span data-ttu-id="f4559-136">Coleção IoT Device Provisioning Service Tag</span><span class="sxs-lookup"><span data-stu-id="f4559-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4559-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4559-137">-Confirm</span></span>
<span data-ttu-id="f4559-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4559-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4559-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4559-139">-WhatIf</span></span>
<span data-ttu-id="f4559-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4559-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4559-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4559-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4559-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4559-142">CommonParameters</span></span>
<span data-ttu-id="f4559-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4559-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4559-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4559-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4559-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4559-145">INPUTS</span></span>

### <span data-ttu-id="f4559-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f4559-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f4559-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f4559-147">System.String</span></span>

## <span data-ttu-id="f4559-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4559-148">OUTPUTS</span></span>

### <span data-ttu-id="f4559-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f4559-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="f4559-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4559-150">NOTES</span></span>

## <span data-ttu-id="f4559-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4559-151">RELATED LINKS</span></span>
