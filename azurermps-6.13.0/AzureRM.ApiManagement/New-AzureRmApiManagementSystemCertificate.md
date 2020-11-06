---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426507"
---
# <span data-ttu-id="7dd49-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="7dd49-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="7dd49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dd49-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd49-103">Cria uma instância de `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="7dd49-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="7dd49-104">O certificado pode ser emitido por uma autoridade de certificação privada e será instalado no serviço de gerenciamento de API no `CertificateAuthority` ou na `Root` loja.</span><span class="sxs-lookup"><span data-stu-id="7dd49-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd49-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dd49-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd49-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dd49-106">DESCRIPTION</span></span>
<span data-ttu-id="7dd49-107">O cmdlet **New-AzureRmApiManagementSystemCertificate** é um comando auxiliar que cria uma instância de **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="7dd49-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="7dd49-108">Esse comando é usado com o cmdlet New-AzureRmApiManagement e Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7dd49-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="7dd49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dd49-109">EXAMPLES</span></span>

### <span data-ttu-id="7dd49-110">Exemplo 1: criar e inicializar uma instância do PsApiManagementSystemCertificate usando um certificado SSL de um arquivo</span><span class="sxs-lookup"><span data-stu-id="7dd49-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="7dd49-111">Esse comando cria e Inicializa uma instância de **PsApiManagementSystemCertificate** com um certificado de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="7dd49-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="7dd49-112">Em seguida, ele cria e o serviço de gerenciamento de API, que instala o certificado da CA no armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="7dd49-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="7dd49-113">OS</span><span class="sxs-lookup"><span data-stu-id="7dd49-113">PARAMETERS</span></span>

### <span data-ttu-id="7dd49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd49-114">-DefaultProfile</span></span>
<span data-ttu-id="7dd49-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd49-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd49-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="7dd49-116">-PfxPassword</span></span>
<span data-ttu-id="7dd49-117">Senha para o arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="7dd49-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd49-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="7dd49-118">-PfxPath</span></span>
<span data-ttu-id="7dd49-119">Caminho para um arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="7dd49-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="7dd49-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="7dd49-120">-StoreName</span></span>
<span data-ttu-id="7dd49-121">StoreName de certificado</span><span class="sxs-lookup"><span data-stu-id="7dd49-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd49-122">CommonParameters</span></span>
<span data-ttu-id="7dd49-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd49-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd49-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dd49-125">INPUTS</span></span>

### <span data-ttu-id="7dd49-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd49-126">System.String</span></span>

### <span data-ttu-id="7dd49-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7dd49-127">System.Security.SecureString</span></span>

## <span data-ttu-id="7dd49-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dd49-128">OUTPUTS</span></span>

### <span data-ttu-id="7dd49-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="7dd49-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="7dd49-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dd49-130">NOTES</span></span>

## <span data-ttu-id="7dd49-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dd49-131">RELATED LINKS</span></span>

[<span data-ttu-id="7dd49-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7dd49-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="7dd49-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7dd49-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
