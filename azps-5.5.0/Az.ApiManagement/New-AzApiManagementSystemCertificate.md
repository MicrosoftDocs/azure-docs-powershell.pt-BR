---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115558"
---
# <span data-ttu-id="40a55-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="40a55-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="40a55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40a55-102">SYNOPSIS</span></span>
<span data-ttu-id="40a55-103">Cria uma instância de `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="40a55-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="40a55-104">O certificado pode ser emitido por ca's particulares e será instalado no serviço de Gerenciamento de API `CertificateAuthority` no armazenamento ou na `Root` loja.</span><span class="sxs-lookup"><span data-stu-id="40a55-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="40a55-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40a55-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a55-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="40a55-106">DESCRIPTION</span></span>
<span data-ttu-id="40a55-107">O cmdlet **New-AzApiManagementSystemCertificate** é um comando auxiliar que cria uma instância de **PsApiManagementSystemCertificate.**</span><span class="sxs-lookup"><span data-stu-id="40a55-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="40a55-108">Esse comando é usado com o New-AzApiManagement e Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40a55-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="40a55-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40a55-109">EXAMPLES</span></span>

### <span data-ttu-id="40a55-110">Exemplo 1: Criar e inicializar uma instância do PsApiManagementSystemCertificate usando um Certificado SSL do arquivo</span><span class="sxs-lookup"><span data-stu-id="40a55-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="40a55-111">Esse comando cria e inicializa uma instância do **PsApiManagementSystemCertificate** com um certificado de AC raiz.</span><span class="sxs-lookup"><span data-stu-id="40a55-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="40a55-112">Em seguida, ele cria e o serviço de Gerenciamento de API que instala o certificado de AC no armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="40a55-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="40a55-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a55-113">PARAMETERS</span></span>

### <span data-ttu-id="40a55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a55-114">-DefaultProfile</span></span>
<span data-ttu-id="40a55-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40a55-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40a55-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="40a55-116">-PfxPassword</span></span>
<span data-ttu-id="40a55-117">Senha do arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="40a55-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="40a55-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="40a55-118">-PfxPath</span></span>
<span data-ttu-id="40a55-119">Caminho para um arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="40a55-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="40a55-120">-Nomeda Store</span><span class="sxs-lookup"><span data-stu-id="40a55-120">-StoreName</span></span>
<span data-ttu-id="40a55-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="40a55-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="40a55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a55-122">CommonParameters</span></span>
<span data-ttu-id="40a55-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a55-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40a55-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a55-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="40a55-125">INPUTS</span></span>

### <span data-ttu-id="40a55-126">System.String</span><span class="sxs-lookup"><span data-stu-id="40a55-126">System.String</span></span>

### <span data-ttu-id="40a55-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="40a55-127">System.Security.SecureString</span></span>

## <span data-ttu-id="40a55-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="40a55-128">OUTPUTS</span></span>

### <span data-ttu-id="40a55-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="40a55-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="40a55-130">Notas</span><span class="sxs-lookup"><span data-stu-id="40a55-130">NOTES</span></span>

## <span data-ttu-id="40a55-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40a55-131">RELATED LINKS</span></span>

[<span data-ttu-id="40a55-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="40a55-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="40a55-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="40a55-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)