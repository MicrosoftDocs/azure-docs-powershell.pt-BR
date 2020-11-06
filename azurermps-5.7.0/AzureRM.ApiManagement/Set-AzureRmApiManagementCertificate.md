---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430542"
---
# <span data-ttu-id="fc666-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fc666-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="fc666-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc666-102">SYNOPSIS</span></span>
<span data-ttu-id="fc666-103">Modifica um certificado de gerenciamento de API que está configurado para autenticação mútua com back-end.</span><span class="sxs-lookup"><span data-stu-id="fc666-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc666-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc666-104">SYNTAX</span></span>

### <span data-ttu-id="fc666-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc666-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc666-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="fc666-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc666-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc666-107">DESCRIPTION</span></span>
<span data-ttu-id="fc666-108">O cmdlet **set-AzureRmApiManagementCertificate** modifica um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc666-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="fc666-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc666-109">EXAMPLES</span></span>

### <span data-ttu-id="fc666-110">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="fc666-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="fc666-111">Esse comando modifica o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="fc666-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="fc666-112">OS</span><span class="sxs-lookup"><span data-stu-id="fc666-112">PARAMETERS</span></span>

### <span data-ttu-id="fc666-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="fc666-113">-CertificateId</span></span>
<span data-ttu-id="fc666-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="fc666-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="fc666-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fc666-115">-Context</span></span>
<span data-ttu-id="fc666-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fc666-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fc666-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc666-117">-DefaultProfile</span></span>
<span data-ttu-id="fc666-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc666-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fc666-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc666-119">-PassThru</span></span>
<span data-ttu-id="fc666-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="fc666-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc666-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="fc666-121">-PfxBytes</span></span>
<span data-ttu-id="fc666-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="fc666-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="fc666-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="fc666-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="fc666-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="fc666-124">-PfxFilePath</span></span>
<span data-ttu-id="fc666-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="fc666-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="fc666-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="fc666-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="fc666-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="fc666-127">-PfxPassword</span></span>
<span data-ttu-id="fc666-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="fc666-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="fc666-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc666-129">CommonParameters</span></span>
<span data-ttu-id="fc666-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc666-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc666-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc666-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc666-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc666-132">INPUTS</span></span>

### <span data-ttu-id="fc666-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc666-133">None</span></span>
<span data-ttu-id="fc666-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fc666-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc666-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc666-135">OUTPUTS</span></span>

### <span data-ttu-id="fc666-136">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fc666-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="fc666-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc666-137">NOTES</span></span>

## <span data-ttu-id="fc666-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc666-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc666-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fc666-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="fc666-140">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fc666-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="fc666-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fc666-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


