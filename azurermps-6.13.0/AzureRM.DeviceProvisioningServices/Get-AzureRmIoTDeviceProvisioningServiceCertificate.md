---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426359"
---
# <span data-ttu-id="bbd72-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd72-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="bbd72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbd72-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd72-103">Lista todos os certificados ou um determinado certificado contido em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bbd72-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbd72-104">SYNTAX</span></span>

### <span data-ttu-id="bbd72-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bbd72-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbd72-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bbd72-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbd72-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="bbd72-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd72-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbd72-108">DESCRIPTION</span></span>
<span data-ttu-id="bbd72-109">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="bbd72-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="bbd72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbd72-110">EXAMPLES</span></span>

### <span data-ttu-id="bbd72-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bbd72-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="bbd72-112">Mostrar detalhes sobre "myCertificate" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd72-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="bbd72-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bbd72-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="bbd72-114">Liste todos os certificados em "myiotdps" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbd72-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="bbd72-115">OS</span><span class="sxs-lookup"><span data-stu-id="bbd72-115">PARAMETERS</span></span>

### <span data-ttu-id="bbd72-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bbd72-116">-CertificateName</span></span>
<span data-ttu-id="bbd72-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="bbd72-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="bbd72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd72-118">-DefaultProfile</span></span>
<span data-ttu-id="bbd72-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd72-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd72-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="bbd72-120">-DpsObject</span></span>
<span data-ttu-id="bbd72-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="bbd72-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd72-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbd72-122">-Name</span></span>
<span data-ttu-id="bbd72-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="bbd72-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bbd72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd72-124">-ResourceGroupName</span></span>
<span data-ttu-id="bbd72-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bbd72-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bbd72-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd72-126">-ResourceId</span></span>
<span data-ttu-id="bbd72-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="bbd72-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bbd72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd72-128">CommonParameters</span></span>
<span data-ttu-id="bbd72-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd72-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd72-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbd72-131">INPUTS</span></span>

### <span data-ttu-id="bbd72-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="bbd72-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="bbd72-133">Parâmetros: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbd72-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="bbd72-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd72-134">System.String</span></span>

## <span data-ttu-id="bbd72-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbd72-135">OUTPUTS</span></span>

### <span data-ttu-id="bbd72-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="bbd72-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="bbd72-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbd72-137">NOTES</span></span>

## <span data-ttu-id="bbd72-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbd72-138">RELATED LINKS</span></span>