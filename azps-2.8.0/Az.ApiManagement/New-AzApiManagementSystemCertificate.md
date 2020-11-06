---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 834a713e5fb7cc6bfcf24244bbb376eb0f01a8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598020"
---
# <span data-ttu-id="a31b0-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="a31b0-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="a31b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a31b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a31b0-103">Cria uma instância de `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="a31b0-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="a31b0-104">O certificado pode ser emitido por uma autoridade de certificação privada e será instalado no serviço de gerenciamento de API no `CertificateAuthority` ou na `Root` loja.</span><span class="sxs-lookup"><span data-stu-id="a31b0-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="a31b0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a31b0-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a31b0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a31b0-106">DESCRIPTION</span></span>
<span data-ttu-id="a31b0-107">O cmdlet **New-AzApiManagementSystemCertificate** é um comando auxiliar que cria uma instância de **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="a31b0-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="a31b0-108">Esse comando é usado com o cmdlet New-AzApiManagement e Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a31b0-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="a31b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a31b0-109">EXAMPLES</span></span>

### <span data-ttu-id="a31b0-110">Exemplo 1: criar e inicializar uma instância do PsApiManagementSystemCertificate usando um certificado SSL de um arquivo</span><span class="sxs-lookup"><span data-stu-id="a31b0-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="a31b0-111">Esse comando cria e Inicializa uma instância de **PsApiManagementSystemCertificate** com um certificado de autoridade de certificação raiz.</span><span class="sxs-lookup"><span data-stu-id="a31b0-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="a31b0-112">Em seguida, ele cria e o serviço de gerenciamento de API, que instala o certificado da CA no armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="a31b0-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="a31b0-113">OS</span><span class="sxs-lookup"><span data-stu-id="a31b0-113">PARAMETERS</span></span>

### <span data-ttu-id="a31b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31b0-114">-DefaultProfile</span></span>
<span data-ttu-id="a31b0-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a31b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a31b0-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="a31b0-116">-PfxPassword</span></span>
<span data-ttu-id="a31b0-117">Senha para o arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="a31b0-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="a31b0-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="a31b0-118">-PfxPath</span></span>
<span data-ttu-id="a31b0-119">Caminho para um arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="a31b0-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="a31b0-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="a31b0-120">-StoreName</span></span>
<span data-ttu-id="a31b0-121">StoreName de certificado</span><span class="sxs-lookup"><span data-stu-id="a31b0-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="a31b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31b0-122">CommonParameters</span></span>
<span data-ttu-id="a31b0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31b0-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a31b0-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31b0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a31b0-125">INPUTS</span></span>

### <span data-ttu-id="a31b0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a31b0-126">System.String</span></span>

### <span data-ttu-id="a31b0-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a31b0-127">System.Security.SecureString</span></span>

## <span data-ttu-id="a31b0-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a31b0-128">OUTPUTS</span></span>

### <span data-ttu-id="a31b0-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="a31b0-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="a31b0-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a31b0-130">NOTES</span></span>

## <span data-ttu-id="a31b0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a31b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="a31b0-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a31b0-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="a31b0-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a31b0-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)