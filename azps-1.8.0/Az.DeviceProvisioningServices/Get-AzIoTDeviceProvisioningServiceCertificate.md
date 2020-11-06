---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: ab7d28c80f87eaf0220ead80e2c7fd76d3d2483b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600926"
---
# <span data-ttu-id="48f3a-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="48f3a-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="48f3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="48f3a-103">Lista todos os certificados ou um determinado certificado contido em um serviço de provisionamento de dispositivo Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="48f3a-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="48f3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48f3a-104">SYNTAX</span></span>

### <span data-ttu-id="48f3a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="48f3a-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48f3a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="48f3a-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48f3a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="48f3a-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48f3a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48f3a-108">DESCRIPTION</span></span>
<span data-ttu-id="48f3a-109">Para obter uma explicação detalhada dos certificados de CA no serviço de provisionamento de dispositivo Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="48f3a-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="48f3a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48f3a-110">EXAMPLES</span></span>

### <span data-ttu-id="48f3a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48f3a-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="48f3a-112">Mostrar detalhes sobre "myCertificate" em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="48f3a-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="48f3a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="48f3a-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="48f3a-114">Liste todos os certificados em "myiotdps" usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="48f3a-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="48f3a-115">OS</span><span class="sxs-lookup"><span data-stu-id="48f3a-115">PARAMETERS</span></span>

### <span data-ttu-id="48f3a-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="48f3a-116">-CertificateName</span></span>
<span data-ttu-id="48f3a-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="48f3a-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="48f3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f3a-118">-DefaultProfile</span></span>
<span data-ttu-id="48f3a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48f3a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48f3a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="48f3a-120">-DpsObject</span></span>
<span data-ttu-id="48f3a-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="48f3a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="48f3a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="48f3a-122">-Name</span></span>
<span data-ttu-id="48f3a-123">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="48f3a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="48f3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="48f3a-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="48f3a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="48f3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48f3a-126">-ResourceId</span></span>
<span data-ttu-id="48f3a-127">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="48f3a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="48f3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f3a-128">CommonParameters</span></span>
<span data-ttu-id="48f3a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f3a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f3a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f3a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48f3a-131">INPUTS</span></span>

### <span data-ttu-id="48f3a-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="48f3a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="48f3a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="48f3a-133">System.String</span></span>

## <span data-ttu-id="48f3a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48f3a-134">OUTPUTS</span></span>

### <span data-ttu-id="48f3a-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="48f3a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="48f3a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48f3a-136">NOTES</span></span>

## <span data-ttu-id="48f3a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48f3a-137">RELATED LINKS</span></span>
