---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609794"
---
# <span data-ttu-id="60216-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="60216-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="60216-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60216-102">SYNOPSIS</span></span>
<span data-ttu-id="60216-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="60216-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60216-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60216-104">SYNTAX</span></span>

### <span data-ttu-id="60216-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="60216-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60216-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60216-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60216-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60216-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60216-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60216-108">DESCRIPTION</span></span>
<span data-ttu-id="60216-109">O cmdlet **Get-AzureKeyVaultCertificateIssuer** Obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="60216-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="60216-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60216-110">EXAMPLES</span></span>

### <span data-ttu-id="60216-111">Exemplo 1: obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="60216-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="60216-112">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="60216-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="60216-113">OS</span><span class="sxs-lookup"><span data-stu-id="60216-113">PARAMETERS</span></span>

### <span data-ttu-id="60216-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60216-114">-DefaultProfile</span></span>
<span data-ttu-id="60216-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60216-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60216-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60216-116">-InputObject</span></span>
<span data-ttu-id="60216-117">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="60216-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60216-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="60216-118">-Name</span></span>
<span data-ttu-id="60216-119">Especifica o nome do emissor do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="60216-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60216-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60216-120">-ResourceId</span></span>
<span data-ttu-id="60216-121">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="60216-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60216-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="60216-122">-VaultName</span></span>
<span data-ttu-id="60216-123">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="60216-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60216-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60216-124">CommonParameters</span></span>
<span data-ttu-id="60216-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60216-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60216-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60216-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60216-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60216-127">INPUTS</span></span>

### <span data-ttu-id="60216-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="60216-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="60216-129">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60216-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="60216-130">System. String</span><span class="sxs-lookup"><span data-stu-id="60216-130">System.String</span></span>

## <span data-ttu-id="60216-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60216-131">OUTPUTS</span></span>

### <span data-ttu-id="60216-132">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="60216-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="60216-133">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="60216-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="60216-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60216-134">NOTES</span></span>

## <span data-ttu-id="60216-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60216-135">RELATED LINKS</span></span>

[<span data-ttu-id="60216-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="60216-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="60216-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="60216-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


