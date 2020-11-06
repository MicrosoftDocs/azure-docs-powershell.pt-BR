---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610220"
---
# <span data-ttu-id="baaee-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="baaee-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="baaee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baaee-102">SYNOPSIS</span></span>
<span data-ttu-id="baaee-103">Modifica um certificado de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="baaee-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baaee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baaee-104">SYNTAX</span></span>

### <span data-ttu-id="baaee-105">Carregar do arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="baaee-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baaee-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="baaee-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="baaee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="baaee-107">DESCRIPTION</span></span>
<span data-ttu-id="baaee-108">O cmdlet **set-AzureRmApiManagementCertificate** modifica um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="baaee-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="baaee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baaee-109">EXAMPLES</span></span>

### <span data-ttu-id="baaee-110">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="baaee-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="baaee-111">Esse comando modifica o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="baaee-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="baaee-112">OS</span><span class="sxs-lookup"><span data-stu-id="baaee-112">PARAMETERS</span></span>

### <span data-ttu-id="baaee-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="baaee-113">-CertificateId</span></span>
<span data-ttu-id="baaee-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="baaee-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="baaee-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="baaee-115">-Context</span></span>
<span data-ttu-id="baaee-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="baaee-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="baaee-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baaee-117">-PassThru</span></span>
<span data-ttu-id="baaee-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="baaee-118">passthru</span></span>

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

### <span data-ttu-id="baaee-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="baaee-119">-PfxBytes</span></span>
<span data-ttu-id="baaee-120">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="baaee-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="baaee-121">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="baaee-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaee-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="baaee-122">-PfxFilePath</span></span>
<span data-ttu-id="baaee-123">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="baaee-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="baaee-124">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="baaee-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaee-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="baaee-125">-PfxPassword</span></span>
<span data-ttu-id="baaee-126">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="baaee-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="baaee-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaee-127">-DefaultProfile</span></span>
<span data-ttu-id="baaee-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baaee-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baaee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaee-129">CommonParameters</span></span>
<span data-ttu-id="baaee-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baaee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaee-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaee-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="baaee-132">INPUTS</span></span>

## <span data-ttu-id="baaee-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="baaee-133">OUTPUTS</span></span>

### <span data-ttu-id="baaee-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="baaee-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="baaee-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="baaee-135">NOTES</span></span>

## <span data-ttu-id="baaee-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baaee-136">RELATED LINKS</span></span>

[<span data-ttu-id="baaee-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="baaee-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="baaee-138">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="baaee-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="baaee-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="baaee-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


