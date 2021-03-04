---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887919"
---
# <span data-ttu-id="4cb64-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4cb64-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4cb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb64-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb64-103">Obtém certificados de Gerenciamento de API configurados para Autenticação Mútua com Backend no serviço.</span><span class="sxs-lookup"><span data-stu-id="4cb64-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="4cb64-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4cb64-104">SYNTAX</span></span>

### <span data-ttu-id="4cb64-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4cb64-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cb64-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb64-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb64-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4cb64-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb64-108">O cmdlet **Get-AzApiManagementCertificate** obtém todos os certificados ou certificados de Gerenciamento de API do Azure especificados.</span><span class="sxs-lookup"><span data-stu-id="4cb64-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="4cb64-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cb64-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb64-110">Exemplo 1: Obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="4cb64-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="4cb64-111">Este comando obtém todos os certificados de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4cb64-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="4cb64-112">Exemplo 2: obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="4cb64-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="4cb64-113">Este comando obtém o certificado de Gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="4cb64-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="4cb64-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4cb64-114">PARAMETERS</span></span>

### <span data-ttu-id="4cb64-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4cb64-115">-CertificateId</span></span>
<span data-ttu-id="4cb64-116">Especifica a ID do certificado a ser obter.</span><span class="sxs-lookup"><span data-stu-id="4cb64-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="4cb64-117">-Context</span><span class="sxs-lookup"><span data-stu-id="4cb64-117">-Context</span></span>
<span data-ttu-id="4cb64-118">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4cb64-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4cb64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb64-119">-DefaultProfile</span></span>
<span data-ttu-id="4cb64-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4cb64-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb64-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cb64-121">-ResourceId</span></span>
<span data-ttu-id="4cb64-122">Identificador de Recurso arm do Certificado.</span><span class="sxs-lookup"><span data-stu-id="4cb64-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="4cb64-123">Se especificado, tentará encontrar o certificado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="4cb64-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="4cb64-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4cb64-124">This parameter is required.</span></span>

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

### <span data-ttu-id="4cb64-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cb64-125">-Confirm</span></span>
<span data-ttu-id="4cb64-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb64-127">-WhatIf</span></span>
<span data-ttu-id="4cb64-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cb64-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb64-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cb64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb64-130">CommonParameters</span></span>
<span data-ttu-id="4cb64-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb64-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cb64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb64-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cb64-133">INPUTS</span></span>

### <span data-ttu-id="4cb64-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cb64-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cb64-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4cb64-135">System.String</span></span>

## <span data-ttu-id="4cb64-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4cb64-136">OUTPUTS</span></span>

### <span data-ttu-id="4cb64-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4cb64-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4cb64-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="4cb64-138">NOTES</span></span>

## <span data-ttu-id="4cb64-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cb64-139">RELATED LINKS</span></span>

[<span data-ttu-id="4cb64-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4cb64-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4cb64-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4cb64-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="4cb64-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4cb64-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


