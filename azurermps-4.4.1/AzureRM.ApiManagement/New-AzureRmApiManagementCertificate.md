---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431228"
---
# <span data-ttu-id="3866e-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3866e-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="3866e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3866e-102">SYNOPSIS</span></span>
<span data-ttu-id="3866e-103">Cria um certificado de gerenciamento de API para ser usado durante a autenticação com back-end.</span><span class="sxs-lookup"><span data-stu-id="3866e-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3866e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3866e-104">SYNTAX</span></span>

### <span data-ttu-id="3866e-105">Carregar do arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="3866e-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3866e-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="3866e-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3866e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3866e-107">DESCRIPTION</span></span>
<span data-ttu-id="3866e-108">O cmdlet **New-AzureRmApiManagementCertificate** cria um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="3866e-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="3866e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3866e-109">EXAMPLES</span></span>

### <span data-ttu-id="3866e-110">Exemplo 1: criar e carregar um certificado</span><span class="sxs-lookup"><span data-stu-id="3866e-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="3866e-111">Esse comando cria um certificado de gerenciamento de API e o carrega.</span><span class="sxs-lookup"><span data-stu-id="3866e-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="3866e-112">OS</span><span class="sxs-lookup"><span data-stu-id="3866e-112">PARAMETERS</span></span>

### <span data-ttu-id="3866e-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="3866e-113">-CertificateId</span></span>
<span data-ttu-id="3866e-114">Especifica a ID do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3866e-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="3866e-115">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="3866e-115">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="3866e-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3866e-116">-Context</span></span>
<span data-ttu-id="3866e-117">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3866e-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3866e-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="3866e-118">-PfxBytes</span></span>
<span data-ttu-id="3866e-119">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="3866e-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="3866e-120">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="3866e-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="3866e-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="3866e-121">-PfxFilePath</span></span>
<span data-ttu-id="3866e-122">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="3866e-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="3866e-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="3866e-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="3866e-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="3866e-124">-PfxPassword</span></span>
<span data-ttu-id="3866e-125">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="3866e-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="3866e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3866e-126">-DefaultProfile</span></span>
<span data-ttu-id="3866e-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3866e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3866e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3866e-128">CommonParameters</span></span>
<span data-ttu-id="3866e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3866e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3866e-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3866e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3866e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3866e-131">INPUTS</span></span>

## <span data-ttu-id="3866e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3866e-132">OUTPUTS</span></span>

### <span data-ttu-id="3866e-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3866e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="3866e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3866e-134">NOTES</span></span>

## <span data-ttu-id="3866e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3866e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3866e-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3866e-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="3866e-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3866e-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="3866e-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3866e-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


