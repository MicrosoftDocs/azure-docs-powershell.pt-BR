---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 9cf6f5a86107e35bb29a9a6dc0b0a02e0e84c47f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776723"
---
# <span data-ttu-id="ffabf-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="ffabf-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="ffabf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffabf-102">SYNOPSIS</span></span>
<span data-ttu-id="ffabf-103">Criar/atualizar um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffabf-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="ffabf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffabf-104">SYNTAX</span></span>

### <span data-ttu-id="ffabf-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffabf-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffabf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ffabf-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffabf-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ffabf-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffabf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffabf-108">DESCRIPTION</span></span>
<span data-ttu-id="ffabf-109">Carrega um novo certificado ou substituindo o certificado existente com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ffabf-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="ffabf-110">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ffabf-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ffabf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffabf-111">EXAMPLES</span></span>

### <span data-ttu-id="ffabf-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ffabf-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="ffabf-113">Carrega um arquivo CER do certificado da CA em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ffabf-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="ffabf-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ffabf-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="ffabf-115">Atualiza um certificado de autoridade de certificação em um hub IoT carregando um novo arquivo CER.</span><span class="sxs-lookup"><span data-stu-id="ffabf-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="ffabf-116">OS</span><span class="sxs-lookup"><span data-stu-id="ffabf-116">PARAMETERS</span></span>

### <span data-ttu-id="ffabf-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ffabf-117">-CertificateName</span></span>
<span data-ttu-id="ffabf-118">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="ffabf-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="ffabf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffabf-119">-DefaultProfile</span></span>
<span data-ttu-id="ffabf-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffabf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffabf-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="ffabf-121">-Etag</span></span>
<span data-ttu-id="ffabf-122">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="ffabf-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ffabf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffabf-123">-InputObject</span></span>
<span data-ttu-id="ffabf-124">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="ffabf-124">Certificate Object</span></span>

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

### <span data-ttu-id="ffabf-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffabf-125">-Name</span></span>
<span data-ttu-id="ffabf-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="ffabf-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ffabf-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ffabf-127">-Path</span></span>
<span data-ttu-id="ffabf-128">base-64 representação do arquivo X509 de certificado. cer ou do caminho de arquivo. PEM.</span><span class="sxs-lookup"><span data-stu-id="ffabf-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ffabf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffabf-129">-ResourceGroupName</span></span>
<span data-ttu-id="ffabf-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ffabf-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ffabf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffabf-131">-ResourceId</span></span>
<span data-ttu-id="ffabf-132">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="ffabf-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="ffabf-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffabf-133">-Confirm</span></span>
<span data-ttu-id="ffabf-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffabf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffabf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffabf-135">-WhatIf</span></span>
<span data-ttu-id="ffabf-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffabf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffabf-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffabf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffabf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffabf-138">CommonParameters</span></span>
<span data-ttu-id="ffabf-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffabf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffabf-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffabf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffabf-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffabf-141">INPUTS</span></span>

### <span data-ttu-id="ffabf-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ffabf-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="ffabf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ffabf-143">System.String</span></span>

## <span data-ttu-id="ffabf-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffabf-144">OUTPUTS</span></span>

### <span data-ttu-id="ffabf-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ffabf-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="ffabf-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffabf-146">NOTES</span></span>

## <span data-ttu-id="ffabf-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffabf-147">RELATED LINKS</span></span>