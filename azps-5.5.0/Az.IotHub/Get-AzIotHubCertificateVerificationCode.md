---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114823"
---
# <span data-ttu-id="b73e8-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="b73e8-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="b73e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b73e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b73e8-103">Gera um código de verificação para um certificado do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="b73e8-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="b73e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b73e8-104">SYNTAX</span></span>

### <span data-ttu-id="b73e8-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b73e8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b73e8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b73e8-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b73e8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b73e8-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b73e8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b73e8-108">DESCRIPTION</span></span>
<span data-ttu-id="b73e8-109">Esse código de verificação é usado para concluir a prova de etapa de confirmação de um certificado.</span><span class="sxs-lookup"><span data-stu-id="b73e8-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="b73e8-110">Use este código de verificação como o CN de um novo certificado assinado com a chave privada de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="b73e8-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="b73e8-111">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b73e8-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b73e8-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b73e8-112">EXAMPLES</span></span>

### <span data-ttu-id="b73e8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b73e8-113">Example 1</span></span>
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

<span data-ttu-id="b73e8-114">Gera um código de verificação para o MyCertificate</span><span class="sxs-lookup"><span data-stu-id="b73e8-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="b73e8-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b73e8-115">PARAMETERS</span></span>

### <span data-ttu-id="b73e8-116">-Nomedo Certificado</span><span class="sxs-lookup"><span data-stu-id="b73e8-116">-CertificateName</span></span>
<span data-ttu-id="b73e8-117">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="b73e8-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="b73e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73e8-118">-DefaultProfile</span></span>
<span data-ttu-id="b73e8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b73e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b73e8-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="b73e8-120">-Etag</span></span>
<span data-ttu-id="b73e8-121">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="b73e8-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b73e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b73e8-122">-InputObject</span></span>
<span data-ttu-id="b73e8-123">Objeto certificate</span><span class="sxs-lookup"><span data-stu-id="b73e8-123">Certificate Object</span></span>

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

### <span data-ttu-id="b73e8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b73e8-124">-Name</span></span>
<span data-ttu-id="b73e8-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="b73e8-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b73e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="b73e8-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b73e8-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b73e8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b73e8-128">-ResourceId</span></span>
<span data-ttu-id="b73e8-129">ID do Recurso de Certificado</span><span class="sxs-lookup"><span data-stu-id="b73e8-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b73e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73e8-130">CommonParameters</span></span>
<span data-ttu-id="b73e8-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73e8-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b73e8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73e8-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="b73e8-133">INPUTS</span></span>

### <span data-ttu-id="b73e8-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b73e8-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b73e8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b73e8-135">System.String</span></span>

## <span data-ttu-id="b73e8-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="b73e8-136">OUTPUTS</span></span>

### <span data-ttu-id="b73e8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="b73e8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="b73e8-138">Notas</span><span class="sxs-lookup"><span data-stu-id="b73e8-138">NOTES</span></span>

## <span data-ttu-id="b73e8-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b73e8-139">RELATED LINKS</span></span>
