---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429911"
---
# <span data-ttu-id="4aac8-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4aac8-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="4aac8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4aac8-102">SYNOPSIS</span></span>
<span data-ttu-id="4aac8-103">Cria um certificado de gerenciamento de API para ser usado durante a autenticação com back-end.</span><span class="sxs-lookup"><span data-stu-id="4aac8-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aac8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aac8-104">SYNTAX</span></span>

### <span data-ttu-id="4aac8-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="4aac8-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aac8-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="4aac8-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aac8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4aac8-107">DESCRIPTION</span></span>
<span data-ttu-id="4aac8-108">O cmdlet **New-AzureRmApiManagementCertificate** cria um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4aac8-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="4aac8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4aac8-109">EXAMPLES</span></span>

### <span data-ttu-id="4aac8-110">Exemplo 1: criar e carregar um certificado</span><span class="sxs-lookup"><span data-stu-id="4aac8-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="4aac8-111">Esse comando carrega um certificado para o gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4aac8-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="4aac8-112">Esse certificado pode ser usado para autenticação mútua com back-end usando políticas.</span><span class="sxs-lookup"><span data-stu-id="4aac8-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="4aac8-113">OS</span><span class="sxs-lookup"><span data-stu-id="4aac8-113">PARAMETERS</span></span>

### <span data-ttu-id="4aac8-114">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="4aac8-114">-CertificateId</span></span>
<span data-ttu-id="4aac8-115">Especifica a ID do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4aac8-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="4aac8-116">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="4aac8-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4aac8-117">-Context</span></span>
<span data-ttu-id="4aac8-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4aac8-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aac8-119">-DefaultProfile</span></span>
<span data-ttu-id="4aac8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4aac8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="4aac8-121">-PfxBytes</span></span>
<span data-ttu-id="4aac8-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="4aac8-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="4aac8-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="4aac8-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="4aac8-124">-PfxFilePath</span></span>
<span data-ttu-id="4aac8-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="4aac8-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="4aac8-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="4aac8-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="4aac8-127">-PfxPassword</span></span>
<span data-ttu-id="4aac8-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="4aac8-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aac8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aac8-129">CommonParameters</span></span>
<span data-ttu-id="4aac8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aac8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aac8-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aac8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aac8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4aac8-132">INPUTS</span></span>

### <span data-ttu-id="4aac8-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4aac8-133">None</span></span>
<span data-ttu-id="4aac8-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4aac8-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aac8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4aac8-135">OUTPUTS</span></span>

### <span data-ttu-id="4aac8-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4aac8-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4aac8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4aac8-137">NOTES</span></span>

## <span data-ttu-id="4aac8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4aac8-138">RELATED LINKS</span></span>

[<span data-ttu-id="4aac8-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4aac8-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="4aac8-140">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4aac8-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="4aac8-141">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4aac8-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


