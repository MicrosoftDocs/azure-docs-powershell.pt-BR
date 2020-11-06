---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428902"
---
# <span data-ttu-id="510cd-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="510cd-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="510cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="510cd-102">SYNOPSIS</span></span>
<span data-ttu-id="510cd-103">Obtém a política para um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="510cd-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="510cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="510cd-104">SYNTAX</span></span>

### <span data-ttu-id="510cd-105">VaultAndCertName (padrão)</span><span class="sxs-lookup"><span data-stu-id="510cd-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="510cd-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="510cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="510cd-107">DESCRIPTION</span></span>
<span data-ttu-id="510cd-108">O cmdlet **Get-AzureKeyVaultCertificatePolicy** Obtém a política para um certificado em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="510cd-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="510cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="510cd-109">EXAMPLES</span></span>

### <span data-ttu-id="510cd-110">Exemplo 1: obter uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="510cd-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="510cd-111">Esse comando obtém a política de certificado para o certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="510cd-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="510cd-112">OS</span><span class="sxs-lookup"><span data-stu-id="510cd-112">PARAMETERS</span></span>

### <span data-ttu-id="510cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510cd-113">-DefaultProfile</span></span>
<span data-ttu-id="510cd-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="510cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="510cd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="510cd-115">-InputObject</span></span>
<span data-ttu-id="510cd-116">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="510cd-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="510cd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="510cd-117">-Name</span></span>
<span data-ttu-id="510cd-118">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="510cd-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510cd-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="510cd-119">-VaultName</span></span>
<span data-ttu-id="510cd-120">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="510cd-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="510cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510cd-121">CommonParameters</span></span>
<span data-ttu-id="510cd-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="510cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510cd-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510cd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510cd-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="510cd-124">INPUTS</span></span>

### <span data-ttu-id="510cd-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="510cd-125">None</span></span>
<span data-ttu-id="510cd-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="510cd-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="510cd-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="510cd-127">OUTPUTS</span></span>

### <span data-ttu-id="510cd-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="510cd-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="510cd-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="510cd-129">NOTES</span></span>

## <span data-ttu-id="510cd-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="510cd-130">RELATED LINKS</span></span>

[<span data-ttu-id="510cd-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="510cd-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="510cd-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="510cd-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

