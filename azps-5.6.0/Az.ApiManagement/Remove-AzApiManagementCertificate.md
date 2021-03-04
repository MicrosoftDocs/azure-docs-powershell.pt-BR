---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 2a28464c735627e97551e845b1d463da9f324a5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887917"
---
# <span data-ttu-id="4088f-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4088f-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4088f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4088f-102">SYNOPSIS</span></span>
<span data-ttu-id="4088f-103">Remove um certificado de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4088f-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="4088f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4088f-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4088f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4088f-105">DESCRIPTION</span></span>
<span data-ttu-id="4088f-106">O cmdlet **Remove-AzApiManagementCertificate** remove um certificado de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4088f-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="4088f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4088f-107">EXAMPLES</span></span>

### <span data-ttu-id="4088f-108">Exemplo 1: Remover um certificado</span><span class="sxs-lookup"><span data-stu-id="4088f-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="4088f-109">Este comando remove o certificado de Gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="4088f-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="4088f-110">Como o *parâmetro Force* é especificado, nenhuma confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="4088f-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="4088f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4088f-111">PARAMETERS</span></span>

### <span data-ttu-id="4088f-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4088f-112">-CertificateId</span></span>
<span data-ttu-id="4088f-113">Especifica a ID do certificado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4088f-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4088f-114">-Context</span></span>
<span data-ttu-id="4088f-115">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4088f-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4088f-116">-DefaultProfile</span></span>
<span data-ttu-id="4088f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4088f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4088f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4088f-118">-PassThru</span></span>
<span data-ttu-id="4088f-119">passthru</span><span class="sxs-lookup"><span data-stu-id="4088f-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4088f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4088f-120">-Confirm</span></span>
<span data-ttu-id="4088f-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4088f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4088f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4088f-122">-WhatIf</span></span>
<span data-ttu-id="4088f-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4088f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4088f-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4088f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4088f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4088f-125">CommonParameters</span></span>
<span data-ttu-id="4088f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4088f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4088f-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4088f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4088f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4088f-128">INPUTS</span></span>

### <span data-ttu-id="4088f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4088f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4088f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4088f-130">System.String</span></span>

### <span data-ttu-id="4088f-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4088f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4088f-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4088f-132">OUTPUTS</span></span>

### <span data-ttu-id="4088f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4088f-133">System.Boolean</span></span>

## <span data-ttu-id="4088f-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="4088f-134">NOTES</span></span>

## <span data-ttu-id="4088f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4088f-135">RELATED LINKS</span></span>

[<span data-ttu-id="4088f-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4088f-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="4088f-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4088f-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4088f-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4088f-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


