---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431258"
---
# <span data-ttu-id="58d7a-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="58d7a-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="58d7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="58d7a-103">Obtém certificados de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="58d7a-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d7a-104">SYNTAX</span></span>

### <span data-ttu-id="58d7a-105">Obter todos os certificados (padrão)</span><span class="sxs-lookup"><span data-stu-id="58d7a-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d7a-106">Obter certificado por ID</span><span class="sxs-lookup"><span data-stu-id="58d7a-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d7a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="58d7a-108">O cmdlet **Get-AzureRmApiManagementCertificate** Obtém todos os certificados de gerenciamento de API do Azure ou certificados que você especificar.</span><span class="sxs-lookup"><span data-stu-id="58d7a-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="58d7a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="58d7a-110">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="58d7a-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="58d7a-111">Esse comando obtém todos os certificados de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="58d7a-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="58d7a-112">Exemplo 2: obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="58d7a-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="58d7a-113">Este comando obtém o certificado de gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="58d7a-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="58d7a-114">OS</span><span class="sxs-lookup"><span data-stu-id="58d7a-114">PARAMETERS</span></span>

### <span data-ttu-id="58d7a-115">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="58d7a-115">-CertificateId</span></span>
<span data-ttu-id="58d7a-116">Especifica a ID do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="58d7a-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d7a-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="58d7a-117">-Context</span></span>
<span data-ttu-id="58d7a-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="58d7a-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="58d7a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58d7a-119">-Confirm</span></span>
<span data-ttu-id="58d7a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d7a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d7a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d7a-121">-WhatIf</span></span>
<span data-ttu-id="58d7a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58d7a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d7a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58d7a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d7a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d7a-124">-DefaultProfile</span></span>
<span data-ttu-id="58d7a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58d7a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58d7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d7a-126">CommonParameters</span></span>
<span data-ttu-id="58d7a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d7a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d7a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d7a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58d7a-129">INPUTS</span></span>

## <span data-ttu-id="58d7a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58d7a-130">OUTPUTS</span></span>

### <span data-ttu-id="58d7a-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="58d7a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="58d7a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58d7a-132">NOTES</span></span>

## <span data-ttu-id="58d7a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58d7a-133">RELATED LINKS</span></span>

[<span data-ttu-id="58d7a-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="58d7a-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="58d7a-135">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="58d7a-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="58d7a-136">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="58d7a-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


