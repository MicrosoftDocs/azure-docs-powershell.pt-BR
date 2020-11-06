---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602284"
---
# <span data-ttu-id="093df-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="093df-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="093df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="093df-102">SYNOPSIS</span></span>
<span data-ttu-id="093df-103">Remove um certificado de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="093df-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="093df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="093df-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="093df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="093df-105">DESCRIPTION</span></span>
<span data-ttu-id="093df-106">O cmdlet **Remove-AzureRmApiManagementCertificate** remove um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="093df-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="093df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="093df-107">EXAMPLES</span></span>

### <span data-ttu-id="093df-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="093df-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="093df-109">Esse comando Remove o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="093df-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="093df-110">Como o parâmetro *Force* é especificado, nenhuma confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="093df-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="093df-111">OS</span><span class="sxs-lookup"><span data-stu-id="093df-111">PARAMETERS</span></span>

### <span data-ttu-id="093df-112">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="093df-112">-CertificateId</span></span>
<span data-ttu-id="093df-113">Especifica a ID do certificado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="093df-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="093df-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="093df-114">-Context</span></span>
<span data-ttu-id="093df-115">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="093df-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="093df-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="093df-116">-PassThru</span></span>
<span data-ttu-id="093df-117">PassThru</span><span class="sxs-lookup"><span data-stu-id="093df-117">passthru</span></span>

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

### <span data-ttu-id="093df-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="093df-118">-Confirm</span></span>
<span data-ttu-id="093df-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093df-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093df-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093df-120">-WhatIf</span></span>
<span data-ttu-id="093df-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="093df-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="093df-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="093df-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093df-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093df-123">-DefaultProfile</span></span>
<span data-ttu-id="093df-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="093df-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="093df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093df-125">CommonParameters</span></span>
<span data-ttu-id="093df-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093df-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="093df-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093df-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="093df-128">INPUTS</span></span>

## <span data-ttu-id="093df-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="093df-129">OUTPUTS</span></span>

### <span data-ttu-id="093df-130">Booliana</span><span class="sxs-lookup"><span data-stu-id="093df-130">Boolean</span></span>

## <span data-ttu-id="093df-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="093df-131">NOTES</span></span>

## <span data-ttu-id="093df-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="093df-132">RELATED LINKS</span></span>

[<span data-ttu-id="093df-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="093df-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="093df-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="093df-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="093df-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="093df-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


