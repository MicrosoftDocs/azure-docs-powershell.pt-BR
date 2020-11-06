---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439943"
---
# <span data-ttu-id="2f03a-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f03a-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2f03a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f03a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f03a-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2f03a-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f03a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f03a-104">SYNTAX</span></span>

### <span data-ttu-id="2f03a-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f03a-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f03a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2f03a-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f03a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f03a-107">DESCRIPTION</span></span>
<span data-ttu-id="2f03a-108">O cmdlet **Get-AzureKeyVaultCertificateIssuer** Obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f03a-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2f03a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f03a-109">EXAMPLES</span></span>

### <span data-ttu-id="2f03a-110">Exemplo 1: obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="2f03a-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="2f03a-111">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="2f03a-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="2f03a-112">OS</span><span class="sxs-lookup"><span data-stu-id="2f03a-112">PARAMETERS</span></span>

### <span data-ttu-id="2f03a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f03a-113">-Name</span></span>
<span data-ttu-id="2f03a-114">Especifica o nome do emissor do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="2f03a-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f03a-115">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2f03a-115">-VaultName</span></span>
<span data-ttu-id="2f03a-116">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2f03a-116">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f03a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f03a-117">-DefaultProfile</span></span>
<span data-ttu-id="2f03a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f03a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f03a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f03a-119">CommonParameters</span></span>
<span data-ttu-id="2f03a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f03a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f03a-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f03a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f03a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f03a-122">INPUTS</span></span>

## <span data-ttu-id="2f03a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f03a-123">OUTPUTS</span></span>

### <span data-ttu-id="2f03a-124">List<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f03a-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2f03a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f03a-125">NOTES</span></span>

## <span data-ttu-id="2f03a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f03a-126">RELATED LINKS</span></span>

[<span data-ttu-id="2f03a-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f03a-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2f03a-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f03a-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


