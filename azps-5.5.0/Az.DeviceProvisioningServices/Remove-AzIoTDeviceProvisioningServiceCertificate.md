---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113215"
---
# <span data-ttu-id="fe923-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="fe923-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="fe923-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe923-102">SYNOPSIS</span></span>
<span data-ttu-id="fe923-103">Exclua um certificado do Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fe923-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="fe923-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe923-104">SYNTAX</span></span>

### <span data-ttu-id="fe923-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe923-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe923-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe923-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe923-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe923-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe923-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe923-108">DESCRIPTION</span></span>
<span data-ttu-id="fe923-109">Para uma explicação detalhada dos certificados de AC no Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="fe923-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="fe923-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe923-110">EXAMPLES</span></span>

### <span data-ttu-id="fe923-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe923-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="fe923-112">Exclua "meucertificar" em um serviço de provisionamento de dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fe923-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fe923-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe923-113">PARAMETERS</span></span>

### <span data-ttu-id="fe923-114">-Nomedo Certificado</span><span class="sxs-lookup"><span data-stu-id="fe923-114">-CertificateName</span></span>
<span data-ttu-id="fe923-115">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="fe923-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="fe923-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe923-116">-DefaultProfile</span></span>
<span data-ttu-id="fe923-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe923-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe923-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="fe923-118">-Etag</span></span>
<span data-ttu-id="fe923-119">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="fe923-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="fe923-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe923-120">-InputObject</span></span>
<span data-ttu-id="fe923-121">Objeto de certificado de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="fe923-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="fe923-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe923-122">-Name</span></span>
<span data-ttu-id="fe923-123">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="fe923-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fe923-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe923-124">-PassThru</span></span>
<span data-ttu-id="fe923-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fe923-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fe923-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe923-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe923-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fe923-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fe923-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe923-128">-ResourceId</span></span>
<span data-ttu-id="fe923-129">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="fe923-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="fe923-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fe923-130">-Confirm</span></span>
<span data-ttu-id="fe923-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe923-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe923-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe923-132">-WhatIf</span></span>
<span data-ttu-id="fe923-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fe923-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe923-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe923-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe923-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe923-135">CommonParameters</span></span>
<span data-ttu-id="fe923-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe923-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe923-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe923-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe923-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe923-138">INPUTS</span></span>

### <span data-ttu-id="fe923-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="fe923-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="fe923-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fe923-140">System.String</span></span>

## <span data-ttu-id="fe923-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe923-141">OUTPUTS</span></span>

### <span data-ttu-id="fe923-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe923-142">System.Boolean</span></span>

## <span data-ttu-id="fe923-143">Notas</span><span class="sxs-lookup"><span data-stu-id="fe923-143">NOTES</span></span>

## <span data-ttu-id="fe923-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe923-144">RELATED LINKS</span></span>
