---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111906"
---
# <span data-ttu-id="7604b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="7604b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="7604b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7604b-102">SYNOPSIS</span></span>
<span data-ttu-id="7604b-103">Gere um código de verificação para um certificado do Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7604b-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="7604b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7604b-104">SYNTAX</span></span>

### <span data-ttu-id="7604b-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7604b-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7604b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7604b-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7604b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7604b-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7604b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7604b-108">DESCRIPTION</span></span>
<span data-ttu-id="7604b-109">Esse código de verificação é usado para concluir a prova de etapa de confirmação de um certificado.</span><span class="sxs-lookup"><span data-stu-id="7604b-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="7604b-110">Use este código de verificação como o CN de um novo certificado assinado com a chave privada de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="7604b-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="7604b-111">Para uma explicação detalhada dos certificados de AC no Serviço de Provisionamento de Dispositivo do Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="7604b-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7604b-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7604b-112">EXAMPLES</span></span>

### <span data-ttu-id="7604b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7604b-113">Example 1</span></span>
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

<span data-ttu-id="7604b-114">Gere um código de verificação para "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="7604b-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="7604b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7604b-115">Example 2</span></span>
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

<span data-ttu-id="7604b-116">Gere um código de verificação para "mycertificate" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="7604b-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="7604b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7604b-117">PARAMETERS</span></span>

### <span data-ttu-id="7604b-118">-Nomedo Certificado</span><span class="sxs-lookup"><span data-stu-id="7604b-118">-CertificateName</span></span>
<span data-ttu-id="7604b-119">Nome do certificado de serviço de provisionamento de dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="7604b-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="7604b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7604b-120">-DefaultProfile</span></span>
<span data-ttu-id="7604b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7604b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7604b-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="7604b-122">-Etag</span></span>
<span data-ttu-id="7604b-123">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="7604b-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7604b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7604b-124">-InputObject</span></span>
<span data-ttu-id="7604b-125">Objeto de certificado de serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7604b-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="7604b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7604b-126">-Name</span></span>
<span data-ttu-id="7604b-127">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="7604b-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7604b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7604b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7604b-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7604b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7604b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7604b-130">-ResourceId</span></span>
<span data-ttu-id="7604b-131">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="7604b-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7604b-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7604b-132">-Confirm</span></span>
<span data-ttu-id="7604b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7604b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7604b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7604b-134">-WhatIf</span></span>
<span data-ttu-id="7604b-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7604b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7604b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7604b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7604b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7604b-137">CommonParameters</span></span>
<span data-ttu-id="7604b-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7604b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7604b-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7604b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7604b-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="7604b-140">INPUTS</span></span>

### <span data-ttu-id="7604b-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7604b-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="7604b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7604b-142">System.String</span></span>

## <span data-ttu-id="7604b-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="7604b-143">OUTPUTS</span></span>

### <span data-ttu-id="7604b-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="7604b-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="7604b-145">Notas</span><span class="sxs-lookup"><span data-stu-id="7604b-145">NOTES</span></span>

## <span data-ttu-id="7604b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7604b-146">RELATED LINKS</span></span>
