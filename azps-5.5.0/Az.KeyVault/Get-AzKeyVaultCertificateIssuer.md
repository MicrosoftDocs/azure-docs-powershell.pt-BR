---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113762"
---
# <span data-ttu-id="10e7a-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10e7a-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="10e7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="10e7a-103">Obtém um emissor de certificado para um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="10e7a-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="10e7a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10e7a-104">SYNTAX</span></span>

### <span data-ttu-id="10e7a-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="10e7a-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e7a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10e7a-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e7a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10e7a-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10e7a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="10e7a-108">DESCRIPTION</span></span>
<span data-ttu-id="10e7a-109">O cmdlet **Get-AzKeyVaultCertificateIssuer** obtém um emissor de certificado especificado ou todos os emissores de certificados para um cofre de chave no Cofre de Chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="10e7a-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="10e7a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="10e7a-111">Exemplo 1: Obter um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="10e7a-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="10e7a-112">Esse comando obtém o emissor do certificado chamado TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="10e7a-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="10e7a-113">Exemplo 2: Emissores de certificado de lista usando filtragem</span><span class="sxs-lookup"><span data-stu-id="10e7a-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="10e7a-114">Esse comando obtém os emissores de certificado que começam com "teste".</span><span class="sxs-lookup"><span data-stu-id="10e7a-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="10e7a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10e7a-115">PARAMETERS</span></span>

### <span data-ttu-id="10e7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e7a-116">-DefaultProfile</span></span>
<span data-ttu-id="10e7a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="10e7a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10e7a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10e7a-118">-InputObject</span></span>
<span data-ttu-id="10e7a-119">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="10e7a-119">KeyVault object.</span></span>

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

### <span data-ttu-id="10e7a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="10e7a-120">-Name</span></span>
<span data-ttu-id="10e7a-121">Especifica o nome do emissor do certificado para obter.</span><span class="sxs-lookup"><span data-stu-id="10e7a-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="10e7a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10e7a-122">-ResourceId</span></span>
<span data-ttu-id="10e7a-123">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="10e7a-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="10e7a-124">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="10e7a-124">-VaultName</span></span>
<span data-ttu-id="10e7a-125">Especifica o nome de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="10e7a-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="10e7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e7a-126">CommonParameters</span></span>
<span data-ttu-id="10e7a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e7a-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e7a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e7a-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="10e7a-129">INPUTS</span></span>

### <span data-ttu-id="10e7a-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="10e7a-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="10e7a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="10e7a-131">System.String</span></span>

## <span data-ttu-id="10e7a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="10e7a-132">OUTPUTS</span></span>

### <span data-ttu-id="10e7a-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="10e7a-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="10e7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10e7a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="10e7a-135">Notas</span><span class="sxs-lookup"><span data-stu-id="10e7a-135">NOTES</span></span>

## <span data-ttu-id="10e7a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10e7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="10e7a-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10e7a-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="10e7a-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10e7a-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


