---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440416"
---
# <span data-ttu-id="313f3-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="313f3-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="313f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="313f3-102">SYNOPSIS</span></span>
<span data-ttu-id="313f3-103">Gera um código de verificação para um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="313f3-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="313f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="313f3-104">SYNTAX</span></span>

### <span data-ttu-id="313f3-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="313f3-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="313f3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="313f3-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="313f3-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="313f3-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="313f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="313f3-108">DESCRIPTION</span></span>
<span data-ttu-id="313f3-109">Esse código de verificação é usado para concluir a etapa de prova de possessão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="313f3-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="313f3-110">Use esse código de verificação como o CN de um novo certificado assinado com a chave privada de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="313f3-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="313f3-111">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="313f3-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="313f3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="313f3-112">EXAMPLES</span></span>

### <span data-ttu-id="313f3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="313f3-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="313f3-114">Gera um código de verificação para mycertification</span><span class="sxs-lookup"><span data-stu-id="313f3-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="313f3-115">OS</span><span class="sxs-lookup"><span data-stu-id="313f3-115">PARAMETERS</span></span>

### <span data-ttu-id="313f3-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="313f3-116">-CertificateName</span></span>
<span data-ttu-id="313f3-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="313f3-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="313f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313f3-118">-DefaultProfile</span></span>
<span data-ttu-id="313f3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="313f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313f3-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="313f3-120">-Etag</span></span>
<span data-ttu-id="313f3-121">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="313f3-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="313f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313f3-122">-InputObject</span></span>
<span data-ttu-id="313f3-123">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="313f3-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="313f3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="313f3-124">-Name</span></span>
<span data-ttu-id="313f3-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="313f3-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="313f3-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="313f3-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313f3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="313f3-128">-ResourceId</span></span>
<span data-ttu-id="313f3-129">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="313f3-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="313f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313f3-130">CommonParameters</span></span>
<span data-ttu-id="313f3-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="313f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313f3-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="313f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313f3-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="313f3-133">INPUTS</span></span>

### <span data-ttu-id="313f3-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="313f3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="313f3-135">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="313f3-135">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="313f3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="313f3-136">System.String</span></span>

## <span data-ttu-id="313f3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="313f3-137">OUTPUTS</span></span>

### <span data-ttu-id="313f3-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="313f3-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="313f3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="313f3-139">NOTES</span></span>

## <span data-ttu-id="313f3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="313f3-140">RELATED LINKS</span></span>
