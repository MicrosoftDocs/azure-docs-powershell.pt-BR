---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 7bf54ade1d8299c539bd64ad947840b2c97d0d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891190"
---
# <span data-ttu-id="fd0d4-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="fd0d4-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="fd0d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0d4-103">Exclui um certificado do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="fd0d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fd0d4-104">SYNTAX</span></span>

### <span data-ttu-id="fd0d4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd0d4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd0d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd0d4-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd0d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd0d4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd0d4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fd0d4-108">DESCRIPTION</span></span>
<span data-ttu-id="fd0d4-109">Para uma explicação detalhada dos certificados de AC no Hub do Azure IoT, consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="fd0d4-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="fd0d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="fd0d4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd0d4-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="fd0d4-112">Exclui MyCertificate</span><span class="sxs-lookup"><span data-stu-id="fd0d4-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="fd0d4-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-113">PARAMETERS</span></span>

### <span data-ttu-id="fd0d4-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="fd0d4-114">-CertificateName</span></span>
<span data-ttu-id="fd0d4-115">Nome do Certificado</span><span class="sxs-lookup"><span data-stu-id="fd0d4-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="fd0d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd0d4-116">-DefaultProfile</span></span>
<span data-ttu-id="fd0d4-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd0d4-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="fd0d4-118">-Etag</span></span>
<span data-ttu-id="fd0d4-119">Etag do Certificado</span><span class="sxs-lookup"><span data-stu-id="fd0d4-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="fd0d4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd0d4-120">-InputObject</span></span>
<span data-ttu-id="fd0d4-121">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="fd0d4-121">Certificate Object</span></span>

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

### <span data-ttu-id="fd0d4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd0d4-122">-Name</span></span>
<span data-ttu-id="fd0d4-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="fd0d4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd0d4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd0d4-124">-PassThru</span></span>
<span data-ttu-id="fd0d4-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fd0d4-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd0d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd0d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd0d4-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fd0d4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd0d4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd0d4-128">-ResourceId</span></span>
<span data-ttu-id="fd0d4-129">ID do Recurso de Certificado</span><span class="sxs-lookup"><span data-stu-id="fd0d4-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="fd0d4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd0d4-130">-Confirm</span></span>
<span data-ttu-id="fd0d4-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd0d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd0d4-132">-WhatIf</span></span>
<span data-ttu-id="fd0d4-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd0d4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd0d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0d4-135">CommonParameters</span></span>
<span data-ttu-id="fd0d4-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd0d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0d4-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd0d4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0d4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-138">INPUTS</span></span>

### <span data-ttu-id="fd0d4-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="fd0d4-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="fd0d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fd0d4-140">System.String</span></span>

## <span data-ttu-id="fd0d4-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-141">OUTPUTS</span></span>

### <span data-ttu-id="fd0d4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd0d4-142">System.Boolean</span></span>

## <span data-ttu-id="fd0d4-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="fd0d4-143">NOTES</span></span>

## <span data-ttu-id="fd0d4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd0d4-144">RELATED LINKS</span></span>
