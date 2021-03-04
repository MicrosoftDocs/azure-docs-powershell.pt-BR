---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: cc3cc5d0e7ae617fc745c2f119f7da9df88417a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886285"
---
# <span data-ttu-id="38b81-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="38b81-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="38b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b81-102">SYNOPSIS</span></span>
<span data-ttu-id="38b81-103">Cria uma instância de `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="38b81-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="38b81-104">O certificado pode ser emitido por acções privadas e será instalado no serviço de Gerenciamento de API `CertificateAuthority` ou `Root` no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38b81-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="38b81-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38b81-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b81-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38b81-106">DESCRIPTION</span></span>
<span data-ttu-id="38b81-107">O cmdlet **New-AzApiManagementSystemCertificate** é um comando auxiliar que cria uma instância de **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="38b81-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="38b81-108">Esse comando é usado com o New-AzApiManagement e Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b81-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="38b81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38b81-109">EXAMPLES</span></span>

### <span data-ttu-id="38b81-110">Exemplo 1: Criar e inicializar uma instância de PsApiManagementSystemCertificate usando um Certificado Ssl do arquivo</span><span class="sxs-lookup"><span data-stu-id="38b81-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="38b81-111">Este comando cria e inicializa uma instância **de PsApiManagementSystemCertificate** com um certificado ca raiz.</span><span class="sxs-lookup"><span data-stu-id="38b81-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="38b81-112">Em seguida, ele cria e o serviço de Gerenciamento de API que instala o certificado ca no armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="38b81-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="38b81-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38b81-113">PARAMETERS</span></span>

### <span data-ttu-id="38b81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b81-114">-DefaultProfile</span></span>
<span data-ttu-id="38b81-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38b81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b81-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="38b81-116">-PfxPassword</span></span>
<span data-ttu-id="38b81-117">Senha para o arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="38b81-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="38b81-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="38b81-118">-PfxPath</span></span>
<span data-ttu-id="38b81-119">Caminho para um arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="38b81-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="38b81-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="38b81-120">-StoreName</span></span>
<span data-ttu-id="38b81-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="38b81-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="38b81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b81-122">CommonParameters</span></span>
<span data-ttu-id="38b81-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b81-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38b81-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b81-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38b81-125">INPUTS</span></span>

### <span data-ttu-id="38b81-126">System.String</span><span class="sxs-lookup"><span data-stu-id="38b81-126">System.String</span></span>

### <span data-ttu-id="38b81-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="38b81-127">System.Security.SecureString</span></span>

## <span data-ttu-id="38b81-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38b81-128">OUTPUTS</span></span>

### <span data-ttu-id="38b81-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="38b81-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="38b81-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="38b81-130">NOTES</span></span>

## <span data-ttu-id="38b81-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38b81-131">RELATED LINKS</span></span>

[<span data-ttu-id="38b81-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="38b81-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="38b81-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="38b81-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)