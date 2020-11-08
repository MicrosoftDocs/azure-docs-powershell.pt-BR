---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115507"
---
# <span data-ttu-id="aef12-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="aef12-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="aef12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aef12-102">SYNOPSIS</span></span>
<span data-ttu-id="aef12-103">Gerar um código de verificação para um certificado de serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="aef12-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="aef12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aef12-104">SYNTAX</span></span>

### <span data-ttu-id="aef12-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="aef12-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aef12-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aef12-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef12-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="aef12-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef12-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aef12-108">DESCRIPTION</span></span>
<span data-ttu-id="aef12-109">Esse código de verificação é usado para concluir a etapa de prova de possessão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="aef12-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="aef12-110">Use esse código de verificação como o CN de um novo certificado assinado com a chave privada de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="aef12-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="aef12-111">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="aef12-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="aef12-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aef12-112">EXAMPLES</span></span>

### <span data-ttu-id="aef12-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aef12-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="aef12-114">Gere um código de verificação para "myCertificate".</span><span class="sxs-lookup"><span data-stu-id="aef12-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="aef12-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="aef12-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="aef12-116">Gere um código de verificação para "mycertification" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="aef12-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="aef12-117">OS</span><span class="sxs-lookup"><span data-stu-id="aef12-117">PARAMETERS</span></span>

### <span data-ttu-id="aef12-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="aef12-118">-CertificateName</span></span>
<span data-ttu-id="aef12-119">Nome do certificado do serviço de provisionamento de dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="aef12-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="aef12-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef12-120">-DefaultProfile</span></span>
<span data-ttu-id="aef12-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aef12-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef12-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="aef12-122">-Etag</span></span>
<span data-ttu-id="aef12-123">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="aef12-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="aef12-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef12-124">-InputObject</span></span>
<span data-ttu-id="aef12-125">Objeto do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="aef12-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="aef12-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="aef12-126">-Name</span></span>
<span data-ttu-id="aef12-127">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="aef12-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="aef12-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef12-128">-ResourceGroupName</span></span>
<span data-ttu-id="aef12-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aef12-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aef12-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aef12-130">-ResourceId</span></span>
<span data-ttu-id="aef12-131">ID do recurso do certificado do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="aef12-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="aef12-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aef12-132">-Confirm</span></span>
<span data-ttu-id="aef12-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef12-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef12-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef12-134">-WhatIf</span></span>
<span data-ttu-id="aef12-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aef12-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef12-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aef12-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef12-137">CommonParameters</span></span>
<span data-ttu-id="aef12-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef12-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef12-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef12-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aef12-140">INPUTS</span></span>

### <span data-ttu-id="aef12-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="aef12-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="aef12-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aef12-142">System.String</span></span>

## <span data-ttu-id="aef12-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aef12-143">OUTPUTS</span></span>

### <span data-ttu-id="aef12-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="aef12-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="aef12-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aef12-145">NOTES</span></span>

## <span data-ttu-id="aef12-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aef12-146">RELATED LINKS</span></span>
