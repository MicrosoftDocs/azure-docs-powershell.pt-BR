---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115335"
---
# <span data-ttu-id="471f9-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="471f9-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="471f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="471f9-102">SYNOPSIS</span></span>
<span data-ttu-id="471f9-103">Atualize um serviço de provisionamento de dispositivo do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="471f9-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="471f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="471f9-104">SYNTAX</span></span>

### <span data-ttu-id="471f9-105">ResourceUpdateSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="471f9-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471f9-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="471f9-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471f9-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="471f9-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="471f9-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="471f9-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471f9-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="471f9-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471f9-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="471f9-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="471f9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="471f9-111">DESCRIPTION</span></span>
<span data-ttu-id="471f9-112">Para uma introdução ao Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="471f9-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="471f9-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="471f9-113">EXAMPLES</span></span>

### <span data-ttu-id="471f9-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="471f9-114">Example 1</span></span>
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

<span data-ttu-id="471f9-115">Atualize a Política de Alocação para "GeoLatency" de um serviço de provisionamento de dispositivos do Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="471f9-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="471f9-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="471f9-116">Example 2</span></span>
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

<span data-ttu-id="471f9-117">Adicione marcas a um serviço de provisionamento de dispositivos do Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="471f9-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="471f9-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="471f9-118">Example 3</span></span>
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

<span data-ttu-id="471f9-119">Exclua a marca e adicione novas marcas a um serviço de provisionamento de dispositivos do Azure IoT Hub "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="471f9-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="471f9-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="471f9-120">PARAMETERS</span></span>

### <span data-ttu-id="471f9-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="471f9-121">-AllocationPolicy</span></span>
<span data-ttu-id="471f9-122">Política de Alocação de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="471f9-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="471f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471f9-123">-DefaultProfile</span></span>
<span data-ttu-id="471f9-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="471f9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="471f9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="471f9-125">-InputObject</span></span>
<span data-ttu-id="471f9-126">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="471f9-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="471f9-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="471f9-127">-Name</span></span>
<span data-ttu-id="471f9-128">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="471f9-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="471f9-129">-Redefinir</span><span class="sxs-lookup"><span data-stu-id="471f9-129">-Reset</span></span>
<span data-ttu-id="471f9-130">Redefinir marcas de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="471f9-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="471f9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471f9-131">-ResourceGroupName</span></span>
<span data-ttu-id="471f9-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="471f9-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="471f9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="471f9-133">-ResourceId</span></span>
<span data-ttu-id="471f9-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="471f9-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="471f9-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="471f9-135">-Tag</span></span>
<span data-ttu-id="471f9-136">Conjunto de marca de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="471f9-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="471f9-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="471f9-137">-Confirm</span></span>
<span data-ttu-id="471f9-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="471f9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="471f9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="471f9-139">-WhatIf</span></span>
<span data-ttu-id="471f9-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="471f9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="471f9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="471f9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="471f9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471f9-142">CommonParameters</span></span>
<span data-ttu-id="471f9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471f9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471f9-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471f9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471f9-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="471f9-145">INPUTS</span></span>

### <span data-ttu-id="471f9-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="471f9-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="471f9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="471f9-147">System.String</span></span>

## <span data-ttu-id="471f9-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="471f9-148">OUTPUTS</span></span>

### <span data-ttu-id="471f9-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="471f9-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="471f9-150">Notas</span><span class="sxs-lookup"><span data-stu-id="471f9-150">NOTES</span></span>

## <span data-ttu-id="471f9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="471f9-151">RELATED LINKS</span></span>
