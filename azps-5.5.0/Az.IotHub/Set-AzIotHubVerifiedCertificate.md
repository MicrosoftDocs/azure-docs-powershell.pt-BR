---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113120"
---
# <span data-ttu-id="cc820-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="cc820-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="cc820-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc820-102">SYNOPSIS</span></span>
<span data-ttu-id="cc820-103">Verifica um certificado do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc820-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="cc820-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc820-104">SYNTAX</span></span>

### <span data-ttu-id="cc820-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc820-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc820-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc820-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc820-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cc820-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc820-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc820-108">DESCRIPTION</span></span>
<span data-ttu-id="cc820-109">Verifica um certificado carregando um certificado de verificação contendo o código de verificação obtido pelo cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="cc820-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="cc820-110">Esta é a última etapa na prova do processo de prova de prova.</span><span class="sxs-lookup"><span data-stu-id="cc820-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="cc820-111">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="cc820-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="cc820-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cc820-112">EXAMPLES</span></span>

### <span data-ttu-id="cc820-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc820-113">Example 1</span></span>
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

<span data-ttu-id="cc820-114">Verifica a propriedade da chave privada MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="cc820-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="cc820-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc820-115">PARAMETERS</span></span>

### <span data-ttu-id="cc820-116">-Nomedo Certificado</span><span class="sxs-lookup"><span data-stu-id="cc820-116">-CertificateName</span></span>
<span data-ttu-id="cc820-117">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="cc820-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="cc820-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc820-118">-DefaultProfile</span></span>
<span data-ttu-id="cc820-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cc820-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc820-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="cc820-120">-Etag</span></span>
<span data-ttu-id="cc820-121">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="cc820-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="cc820-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc820-122">-InputObject</span></span>
<span data-ttu-id="cc820-123">Objeto certificate</span><span class="sxs-lookup"><span data-stu-id="cc820-123">Certificate Object</span></span>

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

### <span data-ttu-id="cc820-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc820-124">-Name</span></span>
<span data-ttu-id="cc820-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="cc820-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cc820-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="cc820-126">-Path</span></span>
<span data-ttu-id="cc820-127">representação de base 64 do arquivo .cer de certificado X509 ou do caminho de arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="cc820-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="cc820-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc820-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc820-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cc820-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cc820-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc820-130">-ResourceId</span></span>
<span data-ttu-id="cc820-131">ID do Recurso de Certificado</span><span class="sxs-lookup"><span data-stu-id="cc820-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="cc820-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cc820-132">-Confirm</span></span>
<span data-ttu-id="cc820-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc820-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc820-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc820-134">-WhatIf</span></span>
<span data-ttu-id="cc820-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cc820-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc820-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc820-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc820-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc820-137">CommonParameters</span></span>
<span data-ttu-id="cc820-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc820-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc820-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc820-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc820-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="cc820-140">INPUTS</span></span>

### <span data-ttu-id="cc820-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="cc820-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="cc820-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cc820-142">System.String</span></span>

## <span data-ttu-id="cc820-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="cc820-143">OUTPUTS</span></span>

### <span data-ttu-id="cc820-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="cc820-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="cc820-145">Notas</span><span class="sxs-lookup"><span data-stu-id="cc820-145">NOTES</span></span>

## <span data-ttu-id="cc820-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc820-146">RELATED LINKS</span></span>
