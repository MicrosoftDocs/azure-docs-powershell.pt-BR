---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955929"
---
# <span data-ttu-id="7948c-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7948c-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7948c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7948c-102">SYNOPSIS</span></span>
<span data-ttu-id="7948c-103">Obtém a política para um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7948c-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="7948c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7948c-104">SYNTAX</span></span>

### <span data-ttu-id="7948c-105">VaultAndCertName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7948c-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7948c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7948c-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7948c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7948c-107">DESCRIPTION</span></span>
<span data-ttu-id="7948c-108">O cmdlet **Get-AzKeyVaultCertificatePolicy** Obtém a política para um certificado em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="7948c-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7948c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7948c-109">EXAMPLES</span></span>

### <span data-ttu-id="7948c-110">Exemplo 1: obter uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="7948c-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="7948c-111">Esse comando obtém a política de certificado para o certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="7948c-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="7948c-112">OS</span><span class="sxs-lookup"><span data-stu-id="7948c-112">PARAMETERS</span></span>

### <span data-ttu-id="7948c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7948c-113">-DefaultProfile</span></span>
<span data-ttu-id="7948c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7948c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7948c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7948c-115">-InputObject</span></span>
<span data-ttu-id="7948c-116">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="7948c-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7948c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7948c-117">-Name</span></span>
<span data-ttu-id="7948c-118">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="7948c-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7948c-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="7948c-119">-VaultName</span></span>
<span data-ttu-id="7948c-120">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7948c-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7948c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7948c-121">CommonParameters</span></span>
<span data-ttu-id="7948c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7948c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7948c-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7948c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7948c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7948c-124">INPUTS</span></span>

### <span data-ttu-id="7948c-125">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7948c-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="7948c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7948c-126">OUTPUTS</span></span>

### <span data-ttu-id="7948c-127">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7948c-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7948c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7948c-128">NOTES</span></span>

## <span data-ttu-id="7948c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7948c-129">RELATED LINKS</span></span>

[<span data-ttu-id="7948c-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7948c-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="7948c-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7948c-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

