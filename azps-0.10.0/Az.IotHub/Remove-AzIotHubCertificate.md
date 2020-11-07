---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 94df7d1870577711174dc4f810c74af528256cb0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775828"
---
# <span data-ttu-id="2a55a-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="2a55a-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="2a55a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a55a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a55a-103">Exclui um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a55a-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="2a55a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a55a-104">SYNTAX</span></span>

### <span data-ttu-id="2a55a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a55a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a55a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a55a-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a55a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="2a55a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a55a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a55a-108">DESCRIPTION</span></span>
<span data-ttu-id="2a55a-109">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2a55a-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2a55a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a55a-110">EXAMPLES</span></span>

### <span data-ttu-id="2a55a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a55a-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="2a55a-112">Exclui o meu certificado</span><span class="sxs-lookup"><span data-stu-id="2a55a-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="2a55a-113">OS</span><span class="sxs-lookup"><span data-stu-id="2a55a-113">PARAMETERS</span></span>

### <span data-ttu-id="2a55a-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2a55a-114">-CertificateName</span></span>
<span data-ttu-id="2a55a-115">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="2a55a-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="2a55a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a55a-116">-DefaultProfile</span></span>
<span data-ttu-id="2a55a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a55a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a55a-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="2a55a-118">-Etag</span></span>
<span data-ttu-id="2a55a-119">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="2a55a-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="2a55a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a55a-120">-InputObject</span></span>
<span data-ttu-id="2a55a-121">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="2a55a-121">Certificate Object</span></span>

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

### <span data-ttu-id="2a55a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a55a-122">-Name</span></span>
<span data-ttu-id="2a55a-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="2a55a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2a55a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a55a-124">-PassThru</span></span>
<span data-ttu-id="2a55a-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="2a55a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2a55a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a55a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a55a-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2a55a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2a55a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a55a-128">-ResourceId</span></span>
<span data-ttu-id="2a55a-129">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="2a55a-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="2a55a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a55a-130">-Confirm</span></span>
<span data-ttu-id="2a55a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a55a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a55a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a55a-132">-WhatIf</span></span>
<span data-ttu-id="2a55a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a55a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a55a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a55a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a55a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a55a-135">CommonParameters</span></span>
<span data-ttu-id="2a55a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a55a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a55a-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a55a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a55a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a55a-138">INPUTS</span></span>

### <span data-ttu-id="2a55a-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="2a55a-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="2a55a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2a55a-140">System.String</span></span>

## <span data-ttu-id="2a55a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a55a-141">OUTPUTS</span></span>

### <span data-ttu-id="2a55a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a55a-142">System.Boolean</span></span>

## <span data-ttu-id="2a55a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a55a-143">NOTES</span></span>

## <span data-ttu-id="2a55a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a55a-144">RELATED LINKS</span></span>
