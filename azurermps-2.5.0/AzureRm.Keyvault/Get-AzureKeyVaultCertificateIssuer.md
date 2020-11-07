---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785944"
---
# <span data-ttu-id="0db3e-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0db3e-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0db3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0db3e-102">SYNOPSIS</span></span>
<span data-ttu-id="0db3e-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0db3e-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0db3e-104">SYNTAX</span></span>

### <span data-ttu-id="0db3e-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0db3e-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0db3e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0db3e-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0db3e-107">DESCRIPTION</span></span>
<span data-ttu-id="0db3e-108">O cmdlet **Get-AzureKeyVaultCertificateIssuer** Obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="0db3e-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0db3e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0db3e-109">EXAMPLES</span></span>

### <span data-ttu-id="0db3e-110">Exemplo 1: obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="0db3e-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="0db3e-111">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="0db3e-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="0db3e-112">OS</span><span class="sxs-lookup"><span data-stu-id="0db3e-112">PARAMETERS</span></span>

### <span data-ttu-id="0db3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db3e-113">-DefaultProfile</span></span>
<span data-ttu-id="0db3e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0db3e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db3e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0db3e-115">-Name</span></span>
<span data-ttu-id="0db3e-116">Especifica o nome do emissor do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="0db3e-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="0db3e-117">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0db3e-117">-VaultName</span></span>
<span data-ttu-id="0db3e-118">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0db3e-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0db3e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db3e-119">CommonParameters</span></span>
<span data-ttu-id="0db3e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db3e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db3e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db3e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db3e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0db3e-122">INPUTS</span></span>

## <span data-ttu-id="0db3e-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0db3e-123">OUTPUTS</span></span>

### <span data-ttu-id="0db3e-124">List<Microsoft. Azure. Commands. keyvault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0db3e-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0db3e-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0db3e-125">NOTES</span></span>

## <span data-ttu-id="0db3e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0db3e-126">RELATED LINKS</span></span>

[<span data-ttu-id="0db3e-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0db3e-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0db3e-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0db3e-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


