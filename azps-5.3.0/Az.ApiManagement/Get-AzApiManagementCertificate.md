---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432737"
---
# <span data-ttu-id="f9b31-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b31-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="f9b31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9b31-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b31-103">Obtém certificados de gerenciamento de API configurados para autenticação mútua com o back-end no serviço.</span><span class="sxs-lookup"><span data-stu-id="f9b31-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="f9b31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9b31-104">SYNTAX</span></span>

### <span data-ttu-id="f9b31-105">ContextParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9b31-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b31-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b31-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b31-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9b31-107">DESCRIPTION</span></span>
<span data-ttu-id="f9b31-108">O cmdlet **Get-AzApiManagementCertificate** Obtém todos os certificados de gerenciamento de API do Azure ou certificados que você especificar.</span><span class="sxs-lookup"><span data-stu-id="f9b31-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="f9b31-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9b31-109">EXAMPLES</span></span>

### <span data-ttu-id="f9b31-110">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="f9b31-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="f9b31-111">Esse comando obtém todos os certificados de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f9b31-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="f9b31-112">Exemplo 2: obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="f9b31-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="f9b31-113">Este comando obtém o certificado de gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="f9b31-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="f9b31-114">OS</span><span class="sxs-lookup"><span data-stu-id="f9b31-114">PARAMETERS</span></span>

### <span data-ttu-id="f9b31-115">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="f9b31-115">-CertificateId</span></span>
<span data-ttu-id="f9b31-116">Especifica a ID do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="f9b31-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b31-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f9b31-117">-Context</span></span>
<span data-ttu-id="f9b31-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f9b31-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b31-119">-DefaultProfile</span></span>
<span data-ttu-id="f9b31-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b31-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b31-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b31-121">-ResourceId</span></span>
<span data-ttu-id="f9b31-122">Identificador de recursos ARM do certificado.</span><span class="sxs-lookup"><span data-stu-id="f9b31-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="f9b31-123">Se especificado, você tentará localizar o certificado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="f9b31-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="f9b31-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9b31-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b31-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9b31-125">-Confirm</span></span>
<span data-ttu-id="f9b31-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b31-127">-WhatIf</span></span>
<span data-ttu-id="f9b31-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9b31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b31-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9b31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b31-130">CommonParameters</span></span>
<span data-ttu-id="f9b31-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b31-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b31-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b31-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9b31-133">INPUTS</span></span>

### <span data-ttu-id="f9b31-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9b31-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9b31-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b31-135">System.String</span></span>

## <span data-ttu-id="f9b31-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9b31-136">OUTPUTS</span></span>

### <span data-ttu-id="f9b31-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b31-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="f9b31-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9b31-138">NOTES</span></span>

## <span data-ttu-id="f9b31-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b31-139">RELATED LINKS</span></span>

[<span data-ttu-id="f9b31-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b31-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="f9b31-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b31-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="f9b31-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b31-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


