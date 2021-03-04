---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d9d77eaac735044091aacbce6f92ee51be1210ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892155"
---
# <span data-ttu-id="ef0d4-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ef0d4-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="ef0d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0d4-103">Obtém um emissor de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="ef0d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef0d4-104">SYNTAX</span></span>

### <span data-ttu-id="ef0d4-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef0d4-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef0d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef0d4-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef0d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0d4-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef0d4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef0d4-108">DESCRIPTION</span></span>
<span data-ttu-id="ef0d4-109">O cmdlet **Get-AzKeyVaultCertificateIssuer** obtém um emissor de certificado especificado ou todos os emissores de certificado para um cofre de chaves no Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="ef0d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="ef0d4-111">Exemplo 1: Obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="ef0d4-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="ef0d4-112">Este comando obtém o emissor de certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="ef0d4-113">Exemplo 2: listar emissores de certificado usando filtragem</span><span class="sxs-lookup"><span data-stu-id="ef0d4-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="ef0d4-114">Este comando obtém os emissores de certificado que começam com "test".</span><span class="sxs-lookup"><span data-stu-id="ef0d4-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="ef0d4-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-115">PARAMETERS</span></span>

### <span data-ttu-id="ef0d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0d4-116">-DefaultProfile</span></span>
<span data-ttu-id="ef0d4-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ef0d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef0d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0d4-118">-InputObject</span></span>
<span data-ttu-id="ef0d4-119">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-119">KeyVault object.</span></span>

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

### <span data-ttu-id="ef0d4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ef0d4-120">-Name</span></span>
<span data-ttu-id="ef0d4-121">Especifica o nome do emissor do certificado a ser obter.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ef0d4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0d4-122">-ResourceId</span></span>
<span data-ttu-id="ef0d4-123">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="ef0d4-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ef0d4-124">-VaultName</span></span>
<span data-ttu-id="ef0d4-125">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ef0d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0d4-126">CommonParameters</span></span>
<span data-ttu-id="ef0d4-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0d4-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef0d4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0d4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-129">INPUTS</span></span>

### <span data-ttu-id="ef0d4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ef0d4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ef0d4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ef0d4-131">System.String</span></span>

## <span data-ttu-id="ef0d4-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-132">OUTPUTS</span></span>

### <span data-ttu-id="ef0d4-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ef0d4-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="ef0d4-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ef0d4-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="ef0d4-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef0d4-135">NOTES</span></span>

## <span data-ttu-id="ef0d4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef0d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef0d4-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ef0d4-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="ef0d4-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ef0d4-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


