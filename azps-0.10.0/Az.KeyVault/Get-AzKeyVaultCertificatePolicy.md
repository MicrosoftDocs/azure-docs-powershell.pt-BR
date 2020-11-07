---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775794"
---
# <span data-ttu-id="506fd-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="506fd-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="506fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="506fd-102">SYNOPSIS</span></span>
<span data-ttu-id="506fd-103">Obtém a política para um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="506fd-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="506fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="506fd-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="506fd-105">DESCRIPTION</span></span>
<span data-ttu-id="506fd-106">O cmdlet **Get-AzKeyVaultCertificatePolicy** Obtém a política para um certificado em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="506fd-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="506fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="506fd-107">EXAMPLES</span></span>

### <span data-ttu-id="506fd-108">Exemplo 1: obter uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="506fd-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="506fd-109">Esse comando obtém a política de certificado para o certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="506fd-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="506fd-110">OS</span><span class="sxs-lookup"><span data-stu-id="506fd-110">PARAMETERS</span></span>

### <span data-ttu-id="506fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506fd-111">-DefaultProfile</span></span>
<span data-ttu-id="506fd-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="506fd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506fd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="506fd-113">-Name</span></span>
<span data-ttu-id="506fd-114">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="506fd-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="506fd-115">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="506fd-115">-VaultName</span></span>
<span data-ttu-id="506fd-116">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="506fd-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="506fd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506fd-117">CommonParameters</span></span>
<span data-ttu-id="506fd-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506fd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506fd-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506fd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506fd-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="506fd-120">INPUTS</span></span>

### <span data-ttu-id="506fd-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="506fd-121">None</span></span>
<span data-ttu-id="506fd-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="506fd-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="506fd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="506fd-123">OUTPUTS</span></span>

### <span data-ttu-id="506fd-124">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="506fd-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="506fd-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="506fd-125">NOTES</span></span>

## <span data-ttu-id="506fd-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="506fd-126">RELATED LINKS</span></span>

[<span data-ttu-id="506fd-127">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="506fd-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="506fd-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="506fd-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)
