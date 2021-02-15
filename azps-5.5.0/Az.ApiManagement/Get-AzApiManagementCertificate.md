---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118084"
---
# <span data-ttu-id="ad280-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ad280-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="ad280-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad280-102">SYNOPSIS</span></span>
<span data-ttu-id="ad280-103">Obtém certificados de Gerenciamento de API configurados para Autenticação Mútuo com Backend no serviço.</span><span class="sxs-lookup"><span data-stu-id="ad280-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="ad280-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad280-104">SYNTAX</span></span>

### <span data-ttu-id="ad280-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad280-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad280-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad280-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad280-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad280-107">DESCRIPTION</span></span>
<span data-ttu-id="ad280-108">O cmdlet **Get-AzApiManagementCertificate** obtém todos os certificados ou certificados de Gerenciamento de API do Azure especificados por você.</span><span class="sxs-lookup"><span data-stu-id="ad280-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="ad280-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad280-109">EXAMPLES</span></span>

### <span data-ttu-id="ad280-110">Exemplo 1: Obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="ad280-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="ad280-111">Esse comando obtém todos os certificados de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ad280-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="ad280-112">Exemplo 2: Obter um certificado por sua ID</span><span class="sxs-lookup"><span data-stu-id="ad280-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="ad280-113">Esse comando obtém o certificado de Gerenciamento de API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ad280-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="ad280-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad280-114">PARAMETERS</span></span>

### <span data-ttu-id="ad280-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="ad280-115">-CertificateId</span></span>
<span data-ttu-id="ad280-116">Especifica a ID do certificado a ser obter.</span><span class="sxs-lookup"><span data-stu-id="ad280-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="ad280-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ad280-117">-Context</span></span>
<span data-ttu-id="ad280-118">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="ad280-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ad280-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad280-119">-DefaultProfile</span></span>
<span data-ttu-id="ad280-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ad280-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad280-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad280-121">-ResourceId</span></span>
<span data-ttu-id="ad280-122">Arm Resource Identifier do Certificado.</span><span class="sxs-lookup"><span data-stu-id="ad280-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="ad280-123">Se especificado, tentará encontrar o certificado pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="ad280-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="ad280-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="ad280-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ad280-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ad280-125">-Confirm</span></span>
<span data-ttu-id="ad280-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad280-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad280-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad280-127">-WhatIf</span></span>
<span data-ttu-id="ad280-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ad280-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad280-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad280-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad280-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad280-130">CommonParameters</span></span>
<span data-ttu-id="ad280-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad280-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad280-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad280-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad280-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad280-133">INPUTS</span></span>

### <span data-ttu-id="ad280-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad280-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad280-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ad280-135">System.String</span></span>

## <span data-ttu-id="ad280-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad280-136">OUTPUTS</span></span>

### <span data-ttu-id="ad280-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ad280-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="ad280-138">Notas</span><span class="sxs-lookup"><span data-stu-id="ad280-138">NOTES</span></span>

## <span data-ttu-id="ad280-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad280-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad280-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ad280-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="ad280-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ad280-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="ad280-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="ad280-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


