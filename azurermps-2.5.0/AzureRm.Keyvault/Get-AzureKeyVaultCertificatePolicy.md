---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785942"
---
# <span data-ttu-id="6b079-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b079-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6b079-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b079-102">SYNOPSIS</span></span>
<span data-ttu-id="6b079-103">Obtém a política para um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6b079-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b079-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b079-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b079-105">DESCRIPTION</span></span>
<span data-ttu-id="6b079-106">O cmdlet **Get-AzureKeyVaultCertificatePolicy** Obtém a política para um certificado em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b079-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6b079-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b079-107">EXAMPLES</span></span>

### <span data-ttu-id="6b079-108">Exemplo 1: obter uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="6b079-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="6b079-109">Esse comando obtém a política de certificado para o certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6b079-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6b079-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b079-110">PARAMETERS</span></span>

### <span data-ttu-id="6b079-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b079-111">-DefaultProfile</span></span>
<span data-ttu-id="6b079-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b079-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b079-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b079-113">-Name</span></span>
<span data-ttu-id="6b079-114">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="6b079-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b079-115">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="6b079-115">-VaultName</span></span>
<span data-ttu-id="6b079-116">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6b079-116">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b079-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b079-117">CommonParameters</span></span>
<span data-ttu-id="6b079-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b079-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b079-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b079-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b079-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b079-120">INPUTS</span></span>

## <span data-ttu-id="6b079-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b079-121">OUTPUTS</span></span>

### <span data-ttu-id="6b079-122">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b079-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6b079-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b079-123">NOTES</span></span>

## <span data-ttu-id="6b079-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b079-124">RELATED LINKS</span></span>

[<span data-ttu-id="6b079-125">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b079-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6b079-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b079-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

