---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595686"
---
# <span data-ttu-id="45ec0-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45ec0-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="45ec0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="45ec0-103">Obtém certificados de gerenciamento de API configurados para autenticação mútua com o back-end no serviço.</span><span class="sxs-lookup"><span data-stu-id="45ec0-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="45ec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45ec0-104">SYNTAX</span></span>

### <span data-ttu-id="45ec0-105">GetAllCertificates (padrão)</span><span class="sxs-lookup"><span data-stu-id="45ec0-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ec0-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="45ec0-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ec0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="45ec0-108">O cmdlet **Get-AzApiManagementCertificate** Obtém todos os certificados de gerenciamento de API do Azure ou certificados que você especificar.</span><span class="sxs-lookup"><span data-stu-id="45ec0-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="45ec0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="45ec0-110">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="45ec0-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="45ec0-111">Esse comando obtém todos os certificados de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="45ec0-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="45ec0-112">Exemplo 2: obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="45ec0-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="45ec0-113">Este comando obtém o certificado de gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="45ec0-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="45ec0-114">OS</span><span class="sxs-lookup"><span data-stu-id="45ec0-114">PARAMETERS</span></span>

### <span data-ttu-id="45ec0-115">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="45ec0-115">-CertificateId</span></span>
<span data-ttu-id="45ec0-116">Especifica a ID do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="45ec0-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="45ec0-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="45ec0-117">-Context</span></span>
<span data-ttu-id="45ec0-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="45ec0-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45ec0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ec0-119">-DefaultProfile</span></span>
<span data-ttu-id="45ec0-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45ec0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45ec0-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45ec0-121">-Confirm</span></span>
<span data-ttu-id="45ec0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ec0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ec0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ec0-123">-WhatIf</span></span>
<span data-ttu-id="45ec0-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45ec0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ec0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45ec0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ec0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ec0-126">CommonParameters</span></span>
<span data-ttu-id="45ec0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ec0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ec0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ec0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ec0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45ec0-129">INPUTS</span></span>

### <span data-ttu-id="45ec0-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45ec0-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45ec0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="45ec0-131">System.String</span></span>

## <span data-ttu-id="45ec0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45ec0-132">OUTPUTS</span></span>

### <span data-ttu-id="45ec0-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45ec0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="45ec0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45ec0-134">NOTES</span></span>

## <span data-ttu-id="45ec0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45ec0-135">RELATED LINKS</span></span>

[<span data-ttu-id="45ec0-136">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45ec0-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="45ec0-137">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45ec0-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="45ec0-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="45ec0-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


