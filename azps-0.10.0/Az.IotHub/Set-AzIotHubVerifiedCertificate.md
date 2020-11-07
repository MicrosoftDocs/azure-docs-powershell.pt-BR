---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 17149af8eb279f95631aafc50d3c0b21857fec98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776685"
---
# <span data-ttu-id="9f111-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="9f111-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="9f111-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f111-102">SYNOPSIS</span></span>
<span data-ttu-id="9f111-103">Verifica um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f111-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="9f111-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f111-104">SYNTAX</span></span>

### <span data-ttu-id="9f111-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f111-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f111-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f111-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f111-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="9f111-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f111-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f111-108">DESCRIPTION</span></span>
<span data-ttu-id="9f111-109">Verifica um certificado carregando um certificado de verificação contendo o código de verificação obtido pelo cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="9f111-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="9f111-110">Esta é a última etapa no processo de prova de posse.</span><span class="sxs-lookup"><span data-stu-id="9f111-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="9f111-111">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="9f111-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="9f111-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f111-112">EXAMPLES</span></span>

### <span data-ttu-id="9f111-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f111-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="9f111-114">Verifica a propriedade da chave privada do meu certificado.</span><span class="sxs-lookup"><span data-stu-id="9f111-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="9f111-115">OS</span><span class="sxs-lookup"><span data-stu-id="9f111-115">PARAMETERS</span></span>

### <span data-ttu-id="9f111-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9f111-116">-CertificateName</span></span>
<span data-ttu-id="9f111-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="9f111-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="9f111-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f111-118">-DefaultProfile</span></span>
<span data-ttu-id="9f111-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f111-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f111-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="9f111-120">-Etag</span></span>
<span data-ttu-id="9f111-121">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="9f111-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9f111-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f111-122">-InputObject</span></span>
<span data-ttu-id="9f111-123">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="9f111-123">Certificate Object</span></span>

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

### <span data-ttu-id="9f111-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f111-124">-Name</span></span>
<span data-ttu-id="9f111-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="9f111-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9f111-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9f111-126">-Path</span></span>
<span data-ttu-id="9f111-127">base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="9f111-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9f111-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f111-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f111-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f111-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9f111-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f111-130">-ResourceId</span></span>
<span data-ttu-id="9f111-131">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="9f111-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="9f111-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f111-132">-Confirm</span></span>
<span data-ttu-id="9f111-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f111-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f111-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f111-134">-WhatIf</span></span>
<span data-ttu-id="9f111-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f111-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f111-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f111-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f111-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f111-137">CommonParameters</span></span>
<span data-ttu-id="9f111-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f111-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f111-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f111-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f111-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f111-140">INPUTS</span></span>

### <span data-ttu-id="9f111-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="9f111-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="9f111-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9f111-142">System.String</span></span>

## <span data-ttu-id="9f111-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f111-143">OUTPUTS</span></span>

### <span data-ttu-id="9f111-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="9f111-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="9f111-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f111-145">NOTES</span></span>

## <span data-ttu-id="9f111-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f111-146">RELATED LINKS</span></span>