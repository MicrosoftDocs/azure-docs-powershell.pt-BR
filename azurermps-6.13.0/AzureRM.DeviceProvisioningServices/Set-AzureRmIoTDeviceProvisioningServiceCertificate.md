---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 5132d4c05b49ac4ff41933aa5c157697445cdbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429545"
---
# <span data-ttu-id="0453e-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="0453e-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="0453e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0453e-102">SYNOPSIS</span></span>
<span data-ttu-id="0453e-103">Verifique um certificado de serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="0453e-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0453e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0453e-104">SYNTAX</span></span>

### <span data-ttu-id="0453e-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0453e-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0453e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0453e-106">InputObjectSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0453e-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="0453e-107">ResourceIdSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0453e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0453e-108">DESCRIPTION</span></span>
<span data-ttu-id="0453e-109">Verifique um certificado carregando um certificado de verificação contendo o código de verificação obtido ao chamar o código de verificação de geração.</span><span class="sxs-lookup"><span data-stu-id="0453e-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="0453e-110">Esta é a última etapa no processo de prova de posse.</span><span class="sxs-lookup"><span data-stu-id="0453e-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="0453e-111">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="0453e-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="0453e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0453e-112">EXAMPLES</span></span>

### <span data-ttu-id="0453e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0453e-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0453e-114">Verifique a propriedade da chave privada "myCertificate".</span><span class="sxs-lookup"><span data-stu-id="0453e-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="0453e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0453e-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzureRmIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0453e-116">Verifique a propriedade da chave privada "myCertificate" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="0453e-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="0453e-117">OS</span><span class="sxs-lookup"><span data-stu-id="0453e-117">PARAMETERS</span></span>

### <span data-ttu-id="0453e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0453e-118">-CertificateName</span></span>
<span data-ttu-id="0453e-119">Nome do certificado do serviço de provisionamento de dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="0453e-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="0453e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0453e-120">-DefaultProfile</span></span>
<span data-ttu-id="0453e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0453e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0453e-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="0453e-122">-Etag</span></span>
<span data-ttu-id="0453e-123">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="0453e-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0453e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0453e-124">-InputObject</span></span>
<span data-ttu-id="0453e-125">Objeto do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0453e-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="0453e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="0453e-126">-Name</span></span>
<span data-ttu-id="0453e-127">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0453e-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0453e-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0453e-128">-Path</span></span>
<span data-ttu-id="0453e-129">base-64 representação do arquivo. cer de certificado. cer ou do caminho de arquivo. PEM do certificado X509</span><span class="sxs-lookup"><span data-stu-id="0453e-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="0453e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0453e-130">-ResourceGroupName</span></span>
<span data-ttu-id="0453e-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0453e-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0453e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0453e-132">-ResourceId</span></span>
<span data-ttu-id="0453e-133">ID do recurso do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="0453e-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="0453e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0453e-134">-Confirm</span></span>
<span data-ttu-id="0453e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0453e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0453e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0453e-136">-WhatIf</span></span>
<span data-ttu-id="0453e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0453e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0453e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0453e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0453e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0453e-139">CommonParameters</span></span>
<span data-ttu-id="0453e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0453e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0453e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0453e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0453e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0453e-142">INPUTS</span></span>

### <span data-ttu-id="0453e-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0453e-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="0453e-144">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0453e-144">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0453e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0453e-145">System.String</span></span>

## <span data-ttu-id="0453e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0453e-146">OUTPUTS</span></span>

### <span data-ttu-id="0453e-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0453e-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="0453e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0453e-148">NOTES</span></span>

## <span data-ttu-id="0453e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0453e-149">RELATED LINKS</span></span>
