---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 05c275448ffecb006c8a23de36fcd7f33397af4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892963"
---
# <span data-ttu-id="601a6-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="601a6-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="601a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="601a6-102">SYNOPSIS</span></span>
<span data-ttu-id="601a6-103">Criar/atualizar um certificado do Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="601a6-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="601a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="601a6-104">SYNTAX</span></span>

### <span data-ttu-id="601a6-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="601a6-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="601a6-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="601a6-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="601a6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="601a6-108">DESCRIPTION</span></span>
<span data-ttu-id="601a6-109">Carrega um novo certificado ou para substituir o certificado existente pelo mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="601a6-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="601a6-110">Para uma explicação detalhada dos certificados de AC no Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="601a6-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="601a6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="601a6-111">EXAMPLES</span></span>

### <span data-ttu-id="601a6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="601a6-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="601a6-113">Carregue um arquivo CER de certificado de CA em um serviço de provisionamento de dispositivo do Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="601a6-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="601a6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="601a6-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="601a6-115">Atualiza um certificado ca em um serviço de provisionamento de dispositivo de hub IoT carregando um novo arquivo CER.</span><span class="sxs-lookup"><span data-stu-id="601a6-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="601a6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="601a6-116">PARAMETERS</span></span>

### <span data-ttu-id="601a6-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="601a6-117">-CertificateName</span></span>
<span data-ttu-id="601a6-118">Nome do certificado de serviço de provisionamento de dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="601a6-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="601a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601a6-119">-DefaultProfile</span></span>
<span data-ttu-id="601a6-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="601a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601a6-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="601a6-121">-Etag</span></span>
<span data-ttu-id="601a6-122">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="601a6-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="601a6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="601a6-123">-InputObject</span></span>
<span data-ttu-id="601a6-124">Objeto de certificado de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="601a6-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="601a6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="601a6-125">-Name</span></span>
<span data-ttu-id="601a6-126">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="601a6-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="601a6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="601a6-127">-Path</span></span>
<span data-ttu-id="601a6-128">representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem</span><span class="sxs-lookup"><span data-stu-id="601a6-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601a6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601a6-129">-ResourceGroupName</span></span>
<span data-ttu-id="601a6-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="601a6-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="601a6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="601a6-131">-ResourceId</span></span>
<span data-ttu-id="601a6-132">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="601a6-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="601a6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="601a6-133">-Confirm</span></span>
<span data-ttu-id="601a6-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="601a6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="601a6-135">-WhatIf</span></span>
<span data-ttu-id="601a6-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="601a6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="601a6-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="601a6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601a6-138">CommonParameters</span></span>
<span data-ttu-id="601a6-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601a6-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601a6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601a6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="601a6-141">INPUTS</span></span>

### <span data-ttu-id="601a6-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="601a6-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="601a6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="601a6-143">System.String</span></span>

## <span data-ttu-id="601a6-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="601a6-144">OUTPUTS</span></span>

### <span data-ttu-id="601a6-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="601a6-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="601a6-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="601a6-146">NOTES</span></span>

## <span data-ttu-id="601a6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="601a6-147">RELATED LINKS</span></span>
