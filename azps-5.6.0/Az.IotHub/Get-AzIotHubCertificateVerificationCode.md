---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 5cad5da87b15430c33d748250501862dae77a38e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889971"
---
# <span data-ttu-id="a7bc2-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="a7bc2-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="a7bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bc2-103">Gera um código de verificação para um certificado do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="a7bc2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7bc2-104">SYNTAX</span></span>

### <span data-ttu-id="a7bc2-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7bc2-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7bc2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7bc2-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7bc2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a7bc2-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7bc2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="a7bc2-109">Esse código de verificação é usado para concluir a etapa de prova de posse de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="a7bc2-110">Use este código de verificação como CN de um novo certificado assinado com a chave privada de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="a7bc2-111">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a7bc2-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a7bc2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-112">EXAMPLES</span></span>

### <span data-ttu-id="a7bc2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7bc2-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="a7bc2-114">Gera um código de verificação para MyCertificate</span><span class="sxs-lookup"><span data-stu-id="a7bc2-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="a7bc2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-115">PARAMETERS</span></span>

### <span data-ttu-id="a7bc2-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a7bc2-116">-CertificateName</span></span>
<span data-ttu-id="a7bc2-117">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="a7bc2-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a7bc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bc2-118">-DefaultProfile</span></span>
<span data-ttu-id="a7bc2-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bc2-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="a7bc2-120">-Etag</span></span>
<span data-ttu-id="a7bc2-121">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="a7bc2-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a7bc2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7bc2-122">-InputObject</span></span>
<span data-ttu-id="a7bc2-123">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="a7bc2-123">Certificate Object</span></span>

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

### <span data-ttu-id="a7bc2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7bc2-124">-Name</span></span>
<span data-ttu-id="a7bc2-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="a7bc2-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a7bc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7bc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7bc2-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a7bc2-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a7bc2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bc2-128">-ResourceId</span></span>
<span data-ttu-id="a7bc2-129">ID do Recurso de Certificado</span><span class="sxs-lookup"><span data-stu-id="a7bc2-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a7bc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bc2-130">CommonParameters</span></span>
<span data-ttu-id="a7bc2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bc2-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bc2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bc2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-133">INPUTS</span></span>

### <span data-ttu-id="a7bc2-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a7bc2-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="a7bc2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a7bc2-135">System.String</span></span>

## <span data-ttu-id="a7bc2-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-136">OUTPUTS</span></span>

### <span data-ttu-id="a7bc2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="a7bc2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="a7bc2-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7bc2-138">NOTES</span></span>

## <span data-ttu-id="a7bc2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7bc2-139">RELATED LINKS</span></span>
