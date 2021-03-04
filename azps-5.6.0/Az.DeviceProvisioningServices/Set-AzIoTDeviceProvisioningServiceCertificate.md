---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 1678202d02f25ea8ffa2ed14a859aaf5965776b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889537"
---
# <span data-ttu-id="897a5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="897a5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="897a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897a5-102">SYNOPSIS</span></span>
<span data-ttu-id="897a5-103">Verifique um certificado do Serviço de Provisionamento de Dispositivo de Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="897a5-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="897a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="897a5-104">SYNTAX</span></span>

### <span data-ttu-id="897a5-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="897a5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="897a5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="897a5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897a5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="897a5-108">DESCRIPTION</span></span>
<span data-ttu-id="897a5-109">Verifique um certificado carregando um certificado de verificação contendo o código de verificação obtido chamando generate-verification-code.</span><span class="sxs-lookup"><span data-stu-id="897a5-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="897a5-110">Esta é a última etapa do processo de prova de posse.</span><span class="sxs-lookup"><span data-stu-id="897a5-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="897a5-111">Para uma explicação detalhada dos certificados de AC no Serviço de Provisionamento de Dispositivos de Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="897a5-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="897a5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="897a5-112">EXAMPLES</span></span>

### <span data-ttu-id="897a5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="897a5-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

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

<span data-ttu-id="897a5-114">Verifique a propriedade da chave privada "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="897a5-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="897a5-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="897a5-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

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

<span data-ttu-id="897a5-116">Verifique a propriedade da chave privada "mycertificate" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="897a5-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="897a5-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="897a5-117">PARAMETERS</span></span>

### <span data-ttu-id="897a5-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="897a5-118">-CertificateName</span></span>
<span data-ttu-id="897a5-119">Nome do certificado de serviço de provisionamento de dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="897a5-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="897a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897a5-120">-DefaultProfile</span></span>
<span data-ttu-id="897a5-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="897a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897a5-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="897a5-122">-Etag</span></span>
<span data-ttu-id="897a5-123">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="897a5-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="897a5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="897a5-124">-InputObject</span></span>
<span data-ttu-id="897a5-125">Objeto de certificado de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="897a5-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="897a5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="897a5-126">-Name</span></span>
<span data-ttu-id="897a5-127">Nome do Serviço de Provisionamento de DispositivoS IoT</span><span class="sxs-lookup"><span data-stu-id="897a5-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="897a5-128">-Path</span><span class="sxs-lookup"><span data-stu-id="897a5-128">-Path</span></span>
<span data-ttu-id="897a5-129">representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem</span><span class="sxs-lookup"><span data-stu-id="897a5-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="897a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897a5-130">-ResourceGroupName</span></span>
<span data-ttu-id="897a5-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="897a5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="897a5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="897a5-132">-ResourceId</span></span>
<span data-ttu-id="897a5-133">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="897a5-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="897a5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="897a5-134">-Confirm</span></span>
<span data-ttu-id="897a5-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897a5-136">-WhatIf</span></span>
<span data-ttu-id="897a5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="897a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="897a5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="897a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897a5-139">CommonParameters</span></span>
<span data-ttu-id="897a5-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897a5-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="897a5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897a5-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="897a5-142">INPUTS</span></span>

### <span data-ttu-id="897a5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="897a5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="897a5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="897a5-144">System.String</span></span>

## <span data-ttu-id="897a5-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="897a5-145">OUTPUTS</span></span>

### <span data-ttu-id="897a5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="897a5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="897a5-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="897a5-147">NOTES</span></span>

## <span data-ttu-id="897a5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="897a5-148">RELATED LINKS</span></span>
