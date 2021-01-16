---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271423"
---
# <span data-ttu-id="1932d-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="1932d-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="1932d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1932d-102">SYNOPSIS</span></span>
<span data-ttu-id="1932d-103">Atualizar um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="1932d-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1932d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1932d-104">SYNTAX</span></span>

### <span data-ttu-id="1932d-105">ResourceUpdateSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1932d-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1932d-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="1932d-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1932d-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="1932d-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1932d-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="1932d-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1932d-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="1932d-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1932d-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="1932d-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1932d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1932d-111">DESCRIPTION</span></span>
<span data-ttu-id="1932d-112">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1932d-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1932d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1932d-113">EXAMPLES</span></span>

### <span data-ttu-id="1932d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1932d-114">Example 1</span></span>
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

<span data-ttu-id="1932d-115">Atualize a política de alocação para "geolatência" de um serviço de provisionamento de dispositivo Hub do Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="1932d-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="1932d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1932d-116">Example 2</span></span>
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

<span data-ttu-id="1932d-117">Adicionar marcas a um serviço de provisionamento de dispositivo Hub IoT do Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="1932d-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="1932d-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1932d-118">Example 3</span></span>
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

<span data-ttu-id="1932d-119">Excluir marca e adicionar novas marcas a um serviço de provisionamento de dispositivo Hub IoT do Azure "myiotdps" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="1932d-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="1932d-120">OS</span><span class="sxs-lookup"><span data-stu-id="1932d-120">PARAMETERS</span></span>

### <span data-ttu-id="1932d-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1932d-121">-AllocationPolicy</span></span>
<span data-ttu-id="1932d-122">Política de alocação do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="1932d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1932d-123">-DefaultProfile</span></span>
<span data-ttu-id="1932d-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1932d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1932d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1932d-125">-InputObject</span></span>
<span data-ttu-id="1932d-126">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1932d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1932d-127">-Name</span></span>
<span data-ttu-id="1932d-128">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1932d-129">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="1932d-129">-Reset</span></span>
<span data-ttu-id="1932d-130">Redefinir as marcas do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="1932d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1932d-131">-ResourceGroupName</span></span>
<span data-ttu-id="1932d-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1932d-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1932d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1932d-133">-ResourceId</span></span>
<span data-ttu-id="1932d-134">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1932d-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="1932d-135">-Tag</span></span>
<span data-ttu-id="1932d-136">Coleção de marcas do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="1932d-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="1932d-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1932d-137">-Confirm</span></span>
<span data-ttu-id="1932d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1932d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1932d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1932d-139">-WhatIf</span></span>
<span data-ttu-id="1932d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1932d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1932d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1932d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1932d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1932d-142">CommonParameters</span></span>
<span data-ttu-id="1932d-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1932d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1932d-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1932d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1932d-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1932d-145">INPUTS</span></span>

### <span data-ttu-id="1932d-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1932d-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1932d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1932d-147">System.String</span></span>

## <span data-ttu-id="1932d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1932d-148">OUTPUTS</span></span>

### <span data-ttu-id="1932d-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1932d-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="1932d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1932d-150">NOTES</span></span>

## <span data-ttu-id="1932d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1932d-151">RELATED LINKS</span></span>
