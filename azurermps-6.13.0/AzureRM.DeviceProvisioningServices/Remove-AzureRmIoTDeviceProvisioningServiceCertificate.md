---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602946"
---
# <span data-ttu-id="9ae9e-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="9ae9e-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="9ae9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ae9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae9e-103">Excluir um certificado de serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ae9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ae9e-104">SYNTAX</span></span>

### <span data-ttu-id="9ae9e-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ae9e-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ae9e-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae9e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="9ae9e-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae9e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ae9e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae9e-109">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="9ae9e-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="9ae9e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ae9e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ae9e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ae9e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="9ae9e-112">Exclua "myCertificate" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9ae9e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ae9e-113">PARAMETERS</span></span>

### <span data-ttu-id="9ae9e-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9ae9e-114">-CertificateName</span></span>
<span data-ttu-id="9ae9e-115">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="9ae9e-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="9ae9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae9e-116">-DefaultProfile</span></span>
<span data-ttu-id="9ae9e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9e-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="9ae9e-118">-Etag</span></span>
<span data-ttu-id="9ae9e-119">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="9ae9e-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9ae9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ae9e-120">-InputObject</span></span>
<span data-ttu-id="9ae9e-121">Objeto do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9ae9e-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="9ae9e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ae9e-122">-Name</span></span>
<span data-ttu-id="9ae9e-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9ae9e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9ae9e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae9e-124">-PassThru</span></span>
<span data-ttu-id="9ae9e-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9ae9e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ae9e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae9e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ae9e-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9ae9e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ae9e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae9e-128">-ResourceId</span></span>
<span data-ttu-id="9ae9e-129">ID do recurso do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="9ae9e-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="9ae9e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ae9e-130">-Confirm</span></span>
<span data-ttu-id="9ae9e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae9e-132">-WhatIf</span></span>
<span data-ttu-id="9ae9e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae9e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae9e-135">CommonParameters</span></span>
<span data-ttu-id="9ae9e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae9e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae9e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae9e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ae9e-138">INPUTS</span></span>

### <span data-ttu-id="9ae9e-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="9ae9e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="9ae9e-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ae9e-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9ae9e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9ae9e-141">System.String</span></span>

## <span data-ttu-id="9ae9e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ae9e-142">OUTPUTS</span></span>

### <span data-ttu-id="9ae9e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ae9e-143">System.Boolean</span></span>

## <span data-ttu-id="9ae9e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ae9e-144">NOTES</span></span>

## <span data-ttu-id="9ae9e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ae9e-145">RELATED LINKS</span></span>
