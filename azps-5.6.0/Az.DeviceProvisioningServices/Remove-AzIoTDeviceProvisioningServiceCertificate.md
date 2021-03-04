---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: fdf6e61b972b2d78db96f88bea502e2d1a4a5865
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885907"
---
# <span data-ttu-id="4c6ac-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="4c6ac-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="4c6ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6ac-103">Exclua um certificado do Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="4c6ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c6ac-104">SYNTAX</span></span>

### <span data-ttu-id="4c6ac-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c6ac-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c6ac-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c6ac-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c6ac-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c6ac-108">DESCRIPTION</span></span>
<span data-ttu-id="4c6ac-109">Para uma explicação detalhada dos certificados de AC no Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="4c6ac-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="4c6ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-110">EXAMPLES</span></span>

### <span data-ttu-id="4c6ac-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c6ac-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="4c6ac-112">Exclua "mycertificate" em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4c6ac-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-113">PARAMETERS</span></span>

### <span data-ttu-id="4c6ac-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4c6ac-114">-CertificateName</span></span>
<span data-ttu-id="4c6ac-115">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="4c6ac-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6ac-116">-DefaultProfile</span></span>
<span data-ttu-id="4c6ac-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c6ac-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="4c6ac-118">-Etag</span></span>
<span data-ttu-id="4c6ac-119">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="4c6ac-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c6ac-120">-InputObject</span></span>
<span data-ttu-id="4c6ac-121">Objeto de certificado de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="4c6ac-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4c6ac-122">-Name</span></span>
<span data-ttu-id="4c6ac-123">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="4c6ac-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4c6ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c6ac-124">-PassThru</span></span>
<span data-ttu-id="4c6ac-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4c6ac-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4c6ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c6ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c6ac-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4c6ac-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4c6ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c6ac-128">-ResourceId</span></span>
<span data-ttu-id="4c6ac-129">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="4c6ac-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="4c6ac-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c6ac-130">-Confirm</span></span>
<span data-ttu-id="4c6ac-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c6ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6ac-132">-WhatIf</span></span>
<span data-ttu-id="4c6ac-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c6ac-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c6ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6ac-135">CommonParameters</span></span>
<span data-ttu-id="4c6ac-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6ac-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c6ac-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6ac-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-138">INPUTS</span></span>

### <span data-ttu-id="4c6ac-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4c6ac-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="4c6ac-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4c6ac-140">System.String</span></span>

## <span data-ttu-id="4c6ac-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-141">OUTPUTS</span></span>

### <span data-ttu-id="4c6ac-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c6ac-142">System.Boolean</span></span>

## <span data-ttu-id="4c6ac-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c6ac-143">NOTES</span></span>

## <span data-ttu-id="4c6ac-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c6ac-144">RELATED LINKS</span></span>
