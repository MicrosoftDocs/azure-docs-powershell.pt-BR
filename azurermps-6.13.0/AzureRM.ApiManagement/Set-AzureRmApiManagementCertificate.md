---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426483"
---
# <span data-ttu-id="1b04d-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1b04d-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1b04d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b04d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b04d-103">Modifica um certificado de gerenciamento de API que está configurado para autenticação mútua com back-end.</span><span class="sxs-lookup"><span data-stu-id="1b04d-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b04d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b04d-104">SYNTAX</span></span>

### <span data-ttu-id="1b04d-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b04d-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b04d-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="1b04d-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b04d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b04d-107">DESCRIPTION</span></span>
<span data-ttu-id="1b04d-108">O cmdlet **set-AzureRmApiManagementCertificate** modifica um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b04d-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="1b04d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b04d-109">EXAMPLES</span></span>

### <span data-ttu-id="1b04d-110">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="1b04d-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="1b04d-111">Esse comando modifica o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="1b04d-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="1b04d-112">OS</span><span class="sxs-lookup"><span data-stu-id="1b04d-112">PARAMETERS</span></span>

### <span data-ttu-id="1b04d-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="1b04d-113">-CertificateId</span></span>
<span data-ttu-id="1b04d-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="1b04d-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="1b04d-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1b04d-115">-Context</span></span>
<span data-ttu-id="1b04d-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1b04d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b04d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b04d-117">-DefaultProfile</span></span>
<span data-ttu-id="1b04d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b04d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b04d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b04d-119">-PassThru</span></span>
<span data-ttu-id="1b04d-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="1b04d-120">passthru</span></span>

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

### <span data-ttu-id="1b04d-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1b04d-121">-PfxBytes</span></span>
<span data-ttu-id="1b04d-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="1b04d-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1b04d-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="1b04d-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="1b04d-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1b04d-124">-PfxFilePath</span></span>
<span data-ttu-id="1b04d-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="1b04d-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1b04d-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="1b04d-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b04d-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1b04d-127">-PfxPassword</span></span>
<span data-ttu-id="1b04d-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="1b04d-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="1b04d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b04d-129">CommonParameters</span></span>
<span data-ttu-id="1b04d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b04d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b04d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b04d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b04d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b04d-132">INPUTS</span></span>

### <span data-ttu-id="1b04d-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b04d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1b04d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1b04d-134">System.String</span></span>

### <span data-ttu-id="1b04d-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="1b04d-135">System.Byte[]</span></span>

### <span data-ttu-id="1b04d-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b04d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b04d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b04d-137">OUTPUTS</span></span>

### <span data-ttu-id="1b04d-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1b04d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1b04d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b04d-139">NOTES</span></span>

## <span data-ttu-id="1b04d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b04d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1b04d-141">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1b04d-141">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1b04d-142">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1b04d-142">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1b04d-143">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1b04d-143">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


