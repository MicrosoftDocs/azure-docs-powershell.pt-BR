---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 7796dae8d9eac66c3dd5b8fa22ed92c2c3c0b232
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891373"
---
# <span data-ttu-id="b1fcb-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fcb-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="b1fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fcb-103">Criar/atualizar um certificado do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="b1fcb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b1fcb-104">SYNTAX</span></span>

### <span data-ttu-id="b1fcb-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1fcb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1fcb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1fcb-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1fcb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1fcb-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1fcb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b1fcb-108">DESCRIPTION</span></span>
<span data-ttu-id="b1fcb-109">Carrega um novo certificado ou para substituir o certificado existente pelo mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="b1fcb-110">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="b1fcb-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="b1fcb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-111">EXAMPLES</span></span>

### <span data-ttu-id="b1fcb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1fcb-112">Example 1</span></span>
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

<span data-ttu-id="b1fcb-113">Carrega um arquivo CER de certificado da CA em um hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="b1fcb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b1fcb-114">Example 2</span></span>
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

<span data-ttu-id="b1fcb-115">Atualiza um certificado ca em um hub IoT carregando um novo arquivo CER.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="b1fcb-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-116">PARAMETERS</span></span>

### <span data-ttu-id="b1fcb-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b1fcb-117">-CertificateName</span></span>
<span data-ttu-id="b1fcb-118">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="b1fcb-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="b1fcb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fcb-119">-DefaultProfile</span></span>
<span data-ttu-id="b1fcb-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1fcb-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="b1fcb-121">-Etag</span></span>
<span data-ttu-id="b1fcb-122">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="b1fcb-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b1fcb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1fcb-123">-InputObject</span></span>
<span data-ttu-id="b1fcb-124">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="b1fcb-124">Certificate Object</span></span>

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

### <span data-ttu-id="b1fcb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b1fcb-125">-Name</span></span>
<span data-ttu-id="b1fcb-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="b1fcb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b1fcb-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b1fcb-127">-Path</span></span>
<span data-ttu-id="b1fcb-128">representação base-64 do arquivo .cer do certificado X509 ou do caminho do arquivo .pem.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="b1fcb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fcb-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1fcb-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b1fcb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b1fcb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1fcb-131">-ResourceId</span></span>
<span data-ttu-id="b1fcb-132">ID do Recurso de Certificado</span><span class="sxs-lookup"><span data-stu-id="b1fcb-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="b1fcb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1fcb-133">-Confirm</span></span>
<span data-ttu-id="b1fcb-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fcb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fcb-135">-WhatIf</span></span>
<span data-ttu-id="b1fcb-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fcb-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fcb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fcb-138">CommonParameters</span></span>
<span data-ttu-id="b1fcb-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fcb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fcb-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fcb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fcb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-141">INPUTS</span></span>

### <span data-ttu-id="b1fcb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b1fcb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="b1fcb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b1fcb-143">System.String</span></span>

## <span data-ttu-id="b1fcb-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-144">OUTPUTS</span></span>

### <span data-ttu-id="b1fcb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="b1fcb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="b1fcb-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="b1fcb-146">NOTES</span></span>

## <span data-ttu-id="b1fcb-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1fcb-147">RELATED LINKS</span></span>
