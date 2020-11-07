---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775800"
---
# <span data-ttu-id="5226d-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5226d-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5226d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5226d-102">SYNOPSIS</span></span>
<span data-ttu-id="5226d-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5226d-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="5226d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5226d-104">SYNTAX</span></span>

### <span data-ttu-id="5226d-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5226d-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5226d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5226d-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5226d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5226d-107">DESCRIPTION</span></span>
<span data-ttu-id="5226d-108">O cmdlet **Get-AzKeyVaultCertificateIssuer** Obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5226d-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5226d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5226d-109">EXAMPLES</span></span>

### <span data-ttu-id="5226d-110">Exemplo 1: obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="5226d-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="5226d-111">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="5226d-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="5226d-112">OS</span><span class="sxs-lookup"><span data-stu-id="5226d-112">PARAMETERS</span></span>

### <span data-ttu-id="5226d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5226d-113">-DefaultProfile</span></span>
<span data-ttu-id="5226d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5226d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5226d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5226d-115">-Name</span></span>
<span data-ttu-id="5226d-116">Especifica o nome do emissor do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="5226d-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5226d-117">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5226d-117">-VaultName</span></span>
<span data-ttu-id="5226d-118">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5226d-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5226d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5226d-119">CommonParameters</span></span>
<span data-ttu-id="5226d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5226d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5226d-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5226d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5226d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5226d-122">INPUTS</span></span>

### <span data-ttu-id="5226d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5226d-123">None</span></span>
<span data-ttu-id="5226d-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5226d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5226d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5226d-125">OUTPUTS</span></span>

### <span data-ttu-id="5226d-126">List<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5226d-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5226d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5226d-127">NOTES</span></span>

## <span data-ttu-id="5226d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5226d-128">RELATED LINKS</span></span>

[<span data-ttu-id="5226d-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5226d-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="5226d-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5226d-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


