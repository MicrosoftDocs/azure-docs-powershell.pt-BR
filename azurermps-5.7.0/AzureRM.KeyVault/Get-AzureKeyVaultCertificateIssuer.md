---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428908"
---
# <span data-ttu-id="e85d6-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e85d6-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="e85d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e85d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e85d6-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e85d6-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e85d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e85d6-104">SYNTAX</span></span>

### <span data-ttu-id="e85d6-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e85d6-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e85d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e85d6-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e85d6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e85d6-107">DESCRIPTION</span></span>
<span data-ttu-id="e85d6-108">O cmdlet **Get-AzureKeyVaultCertificateIssuer** Obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="e85d6-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e85d6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e85d6-109">EXAMPLES</span></span>

### <span data-ttu-id="e85d6-110">Exemplo 1: obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="e85d6-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="e85d6-111">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="e85d6-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="e85d6-112">OS</span><span class="sxs-lookup"><span data-stu-id="e85d6-112">PARAMETERS</span></span>

### <span data-ttu-id="e85d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85d6-113">-DefaultProfile</span></span>
<span data-ttu-id="e85d6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e85d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e85d6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e85d6-115">-InputObject</span></span>
<span data-ttu-id="e85d6-116">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="e85d6-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e85d6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e85d6-117">-Name</span></span>
<span data-ttu-id="e85d6-118">Especifica o nome do emissor do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="e85d6-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e85d6-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e85d6-119">-VaultName</span></span>
<span data-ttu-id="e85d6-120">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e85d6-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e85d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85d6-121">CommonParameters</span></span>
<span data-ttu-id="e85d6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85d6-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85d6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85d6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e85d6-124">INPUTS</span></span>

### <span data-ttu-id="e85d6-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e85d6-125">None</span></span>
<span data-ttu-id="e85d6-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e85d6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e85d6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e85d6-127">OUTPUTS</span></span>

### <span data-ttu-id="e85d6-128">List<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e85d6-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="e85d6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e85d6-129">NOTES</span></span>

## <span data-ttu-id="e85d6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e85d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="e85d6-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e85d6-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="e85d6-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="e85d6-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


