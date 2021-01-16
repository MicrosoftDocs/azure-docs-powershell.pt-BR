---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260564"
---
# <span data-ttu-id="71527-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="71527-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="71527-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71527-102">SYNOPSIS</span></span>
<span data-ttu-id="71527-103">Atualizar um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="71527-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="71527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71527-104">SYNTAX</span></span>

### <span data-ttu-id="71527-105">ResourceUpdateSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71527-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71527-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="71527-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71527-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="71527-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71527-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="71527-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71527-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="71527-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71527-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="71527-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71527-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71527-111">DESCRIPTION</span></span>
<span data-ttu-id="71527-112">Para obter uma introdução ao serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="71527-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="71527-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71527-113">EXAMPLES</span></span>

### <span data-ttu-id="71527-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71527-114">Example 1</span></span>
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

<span data-ttu-id="71527-115">Atualize a política de alocação para "geolatência" de um serviço de provisionamento de dispositivo Hub do Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="71527-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="71527-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="71527-116">Example 2</span></span>
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

<span data-ttu-id="71527-117">Adicionar marcas a um serviço de provisionamento de dispositivo Hub IoT do Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="71527-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="71527-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="71527-118">Example 3</span></span>
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

<span data-ttu-id="71527-119">Excluir marca e adicionar novas marcas a um serviço de provisionamento de dispositivo Hub IoT do Azure "myiotdps" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="71527-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="71527-120">OS</span><span class="sxs-lookup"><span data-stu-id="71527-120">PARAMETERS</span></span>

### <span data-ttu-id="71527-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="71527-121">-AllocationPolicy</span></span>
<span data-ttu-id="71527-122">Política de alocação do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="71527-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71527-123">-DefaultProfile</span></span>
<span data-ttu-id="71527-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71527-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71527-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71527-125">-InputObject</span></span>
<span data-ttu-id="71527-126">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="71527-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="71527-127">-Name</span></span>
<span data-ttu-id="71527-128">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="71527-129">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="71527-129">-Reset</span></span>
<span data-ttu-id="71527-130">Redefinir as marcas do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="71527-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71527-131">-ResourceGroupName</span></span>
<span data-ttu-id="71527-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71527-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="71527-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71527-133">-ResourceId</span></span>
<span data-ttu-id="71527-134">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="71527-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="71527-135">-Tag</span></span>
<span data-ttu-id="71527-136">Coleção de marcas do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="71527-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="71527-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71527-137">-Confirm</span></span>
<span data-ttu-id="71527-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71527-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71527-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71527-139">-WhatIf</span></span>
<span data-ttu-id="71527-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71527-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71527-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71527-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71527-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71527-142">CommonParameters</span></span>
<span data-ttu-id="71527-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71527-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71527-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71527-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71527-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71527-145">INPUTS</span></span>

### <span data-ttu-id="71527-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="71527-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="71527-147">System. String</span><span class="sxs-lookup"><span data-stu-id="71527-147">System.String</span></span>

## <span data-ttu-id="71527-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71527-148">OUTPUTS</span></span>

### <span data-ttu-id="71527-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="71527-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="71527-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71527-150">NOTES</span></span>

## <span data-ttu-id="71527-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71527-151">RELATED LINKS</span></span>
