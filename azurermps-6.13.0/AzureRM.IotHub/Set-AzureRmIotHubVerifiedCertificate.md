---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440406"
---
# <span data-ttu-id="ccefb-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="ccefb-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="ccefb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccefb-102">SYNOPSIS</span></span>
<span data-ttu-id="ccefb-103">Verifica um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccefb-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccefb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccefb-104">SYNTAX</span></span>

### <span data-ttu-id="ccefb-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ccefb-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccefb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ccefb-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccefb-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ccefb-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccefb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccefb-108">DESCRIPTION</span></span>
<span data-ttu-id="ccefb-109">Verifica um certificado carregando um certificado de verificação contendo o código de verificação obtido pelo cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="ccefb-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="ccefb-110">Esta é a última etapa no processo de prova de posse.</span><span class="sxs-lookup"><span data-stu-id="ccefb-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="ccefb-111">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ccefb-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ccefb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccefb-112">EXAMPLES</span></span>

### <span data-ttu-id="ccefb-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ccefb-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="ccefb-114">Verifica a propriedade da chave privada do meu certificado.</span><span class="sxs-lookup"><span data-stu-id="ccefb-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="ccefb-115">OS</span><span class="sxs-lookup"><span data-stu-id="ccefb-115">PARAMETERS</span></span>

### <span data-ttu-id="ccefb-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ccefb-116">-CertificateName</span></span>
<span data-ttu-id="ccefb-117">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="ccefb-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="ccefb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccefb-118">-DefaultProfile</span></span>
<span data-ttu-id="ccefb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccefb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccefb-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="ccefb-120">-Etag</span></span>
<span data-ttu-id="ccefb-121">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="ccefb-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ccefb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccefb-122">-InputObject</span></span>
<span data-ttu-id="ccefb-123">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="ccefb-123">Certificate Object</span></span>

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

### <span data-ttu-id="ccefb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccefb-124">-Name</span></span>
<span data-ttu-id="ccefb-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="ccefb-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ccefb-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ccefb-126">-Path</span></span>
<span data-ttu-id="ccefb-127">base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="ccefb-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ccefb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccefb-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccefb-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ccefb-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ccefb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccefb-130">-ResourceId</span></span>
<span data-ttu-id="ccefb-131">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="ccefb-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="ccefb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ccefb-132">-Confirm</span></span>
<span data-ttu-id="ccefb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccefb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccefb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccefb-134">-WhatIf</span></span>
<span data-ttu-id="ccefb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ccefb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccefb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ccefb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccefb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccefb-137">CommonParameters</span></span>
<span data-ttu-id="ccefb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccefb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccefb-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccefb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccefb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccefb-140">INPUTS</span></span>

### <span data-ttu-id="ccefb-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ccefb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="ccefb-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ccefb-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ccefb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ccefb-143">System.String</span></span>

## <span data-ttu-id="ccefb-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccefb-144">OUTPUTS</span></span>

### <span data-ttu-id="ccefb-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ccefb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="ccefb-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccefb-146">NOTES</span></span>

## <span data-ttu-id="ccefb-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccefb-147">RELATED LINKS</span></span>
