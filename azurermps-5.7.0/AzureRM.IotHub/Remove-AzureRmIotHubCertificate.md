---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429769"
---
# <span data-ttu-id="d0faf-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="d0faf-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="d0faf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0faf-102">SYNOPSIS</span></span>
<span data-ttu-id="d0faf-103">Exclui um certificado de Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0faf-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0faf-104">SYNTAX</span></span>

### <span data-ttu-id="d0faf-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0faf-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0faf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0faf-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0faf-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="d0faf-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0faf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0faf-108">DESCRIPTION</span></span>
<span data-ttu-id="d0faf-109">Para obter uma explicação detalhada dos certificados de CA no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="d0faf-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="d0faf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0faf-110">EXAMPLES</span></span>

### <span data-ttu-id="d0faf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0faf-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="d0faf-112">Exclui o meu certificado</span><span class="sxs-lookup"><span data-stu-id="d0faf-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="d0faf-113">OS</span><span class="sxs-lookup"><span data-stu-id="d0faf-113">PARAMETERS</span></span>

### <span data-ttu-id="d0faf-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d0faf-114">-CertificateName</span></span>
<span data-ttu-id="d0faf-115">Nome do certificado</span><span class="sxs-lookup"><span data-stu-id="d0faf-115">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0faf-116">-DefaultProfile</span></span>
<span data-ttu-id="d0faf-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0faf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="d0faf-118">-Etag</span></span>
<span data-ttu-id="d0faf-119">ETag do certificado</span><span class="sxs-lookup"><span data-stu-id="d0faf-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0faf-120">-InputObject</span></span>
<span data-ttu-id="d0faf-121">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="d0faf-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0faf-122">-Name</span></span>
<span data-ttu-id="d0faf-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="d0faf-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0faf-124">-PassThru</span></span>
<span data-ttu-id="d0faf-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="d0faf-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0faf-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0faf-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d0faf-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0faf-128">-ResourceId</span></span>
<span data-ttu-id="d0faf-129">ID do recurso do certificado</span><span class="sxs-lookup"><span data-stu-id="d0faf-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d0faf-130">-Confirm</span></span>
<span data-ttu-id="d0faf-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0faf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0faf-132">-WhatIf</span></span>
<span data-ttu-id="d0faf-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0faf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0faf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0faf-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0faf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0faf-135">CommonParameters</span></span>
<span data-ttu-id="d0faf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0faf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0faf-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0faf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0faf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0faf-138">INPUTS</span></span>

### <span data-ttu-id="d0faf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d0faf-139">System.String</span></span>

## <span data-ttu-id="d0faf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0faf-140">OUTPUTS</span></span>

### <span data-ttu-id="d0faf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0faf-141">System.Boolean</span></span>

## <span data-ttu-id="d0faf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0faf-142">NOTES</span></span>

## <span data-ttu-id="d0faf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0faf-143">RELATED LINKS</span></span>

