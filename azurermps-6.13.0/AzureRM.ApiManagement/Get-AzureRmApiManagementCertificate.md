---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: af187553ef8ea432299197cd06baefd585e73cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431474"
---
# <span data-ttu-id="5306f-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5306f-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="5306f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5306f-102">SYNOPSIS</span></span>
<span data-ttu-id="5306f-103">Obtém certificados de gerenciamento de API configurados para autenticação mútua com o back-end no serviço.</span><span class="sxs-lookup"><span data-stu-id="5306f-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5306f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5306f-104">SYNTAX</span></span>

### <span data-ttu-id="5306f-105">GetAllCertificates (padrão)</span><span class="sxs-lookup"><span data-stu-id="5306f-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5306f-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="5306f-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5306f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5306f-107">DESCRIPTION</span></span>
<span data-ttu-id="5306f-108">O cmdlet **Get-AzureRmApiManagementCertificate** Obtém todos os certificados de gerenciamento de API do Azure ou certificados que você especificar.</span><span class="sxs-lookup"><span data-stu-id="5306f-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="5306f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5306f-109">EXAMPLES</span></span>

### <span data-ttu-id="5306f-110">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="5306f-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="5306f-111">Esse comando obtém todos os certificados de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5306f-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="5306f-112">Exemplo 2: obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="5306f-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="5306f-113">Este comando obtém o certificado de gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="5306f-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="5306f-114">OS</span><span class="sxs-lookup"><span data-stu-id="5306f-114">PARAMETERS</span></span>

### <span data-ttu-id="5306f-115">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="5306f-115">-CertificateId</span></span>
<span data-ttu-id="5306f-116">Especifica a ID do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="5306f-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5306f-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5306f-117">-Context</span></span>
<span data-ttu-id="5306f-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5306f-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5306f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5306f-119">-DefaultProfile</span></span>
<span data-ttu-id="5306f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5306f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5306f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5306f-121">-Confirm</span></span>
<span data-ttu-id="5306f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5306f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5306f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5306f-123">-WhatIf</span></span>
<span data-ttu-id="5306f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5306f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5306f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5306f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5306f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5306f-126">CommonParameters</span></span>
<span data-ttu-id="5306f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5306f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5306f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5306f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5306f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5306f-129">INPUTS</span></span>

### <span data-ttu-id="5306f-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5306f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5306f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5306f-131">System.String</span></span>

## <span data-ttu-id="5306f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5306f-132">OUTPUTS</span></span>

### <span data-ttu-id="5306f-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5306f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="5306f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5306f-134">NOTES</span></span>

## <span data-ttu-id="5306f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5306f-135">RELATED LINKS</span></span>

[<span data-ttu-id="5306f-136">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5306f-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="5306f-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5306f-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="5306f-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="5306f-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)

