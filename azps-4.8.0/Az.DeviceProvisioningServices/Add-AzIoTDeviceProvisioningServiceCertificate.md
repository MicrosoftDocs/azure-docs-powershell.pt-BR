---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948305"
---
# <span data-ttu-id="d2192-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d2192-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d2192-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2192-102">SYNOPSIS</span></span>
<span data-ttu-id="d2192-103">Criar/atualizar um certificado de serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2192-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="d2192-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2192-104">SYNTAX</span></span>

### <span data-ttu-id="d2192-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2192-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2192-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2192-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2192-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="d2192-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2192-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2192-108">DESCRIPTION</span></span>
<span data-ttu-id="d2192-109">Carrega um novo certificado ou substituindo o certificado existente com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d2192-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="d2192-110">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d2192-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d2192-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2192-111">EXAMPLES</span></span>

### <span data-ttu-id="d2192-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2192-112">Example 1</span></span>
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

<span data-ttu-id="d2192-113">Carregar um arquivo CER de certificado de CA para um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2192-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="d2192-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2192-114">Example 2</span></span>
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

<span data-ttu-id="d2192-115">Atualiza um certificado de autoridade de certificação em um serviço de provisionamento de dispositivo Hub IoT carregando um novo arquivo CER.</span><span class="sxs-lookup"><span data-stu-id="d2192-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="d2192-116">OS</span><span class="sxs-lookup"><span data-stu-id="d2192-116">PARAMETERS</span></span>

### <span data-ttu-id="d2192-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d2192-117">-CertificateName</span></span>
<span data-ttu-id="d2192-118">Nome do certificado do serviço de provisionamento de dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="d2192-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="d2192-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2192-119">-DefaultProfile</span></span>
<span data-ttu-id="d2192-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2192-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2192-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="d2192-121">-Etag</span></span>
<span data-ttu-id="d2192-122">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="d2192-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="d2192-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2192-123">-InputObject</span></span>
<span data-ttu-id="d2192-124">Objeto do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="d2192-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="d2192-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2192-125">-Name</span></span>
<span data-ttu-id="d2192-126">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="d2192-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d2192-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d2192-127">-Path</span></span>
<span data-ttu-id="d2192-128">base-64 representação do arquivo. cer de certificado. cer ou do caminho de arquivo. PEM do certificado X509</span><span class="sxs-lookup"><span data-stu-id="d2192-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="d2192-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2192-129">-ResourceGroupName</span></span>
<span data-ttu-id="d2192-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d2192-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d2192-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2192-131">-ResourceId</span></span>
<span data-ttu-id="d2192-132">ID do recurso do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="d2192-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d2192-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2192-133">-Confirm</span></span>
<span data-ttu-id="d2192-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2192-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2192-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2192-135">-WhatIf</span></span>
<span data-ttu-id="d2192-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2192-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2192-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2192-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2192-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2192-138">CommonParameters</span></span>
<span data-ttu-id="d2192-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2192-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2192-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2192-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2192-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2192-141">INPUTS</span></span>

### <span data-ttu-id="d2192-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d2192-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="d2192-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d2192-143">System.String</span></span>

## <span data-ttu-id="d2192-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2192-144">OUTPUTS</span></span>

### <span data-ttu-id="d2192-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d2192-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="d2192-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2192-146">NOTES</span></span>

## <span data-ttu-id="d2192-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2192-147">RELATED LINKS</span></span>
