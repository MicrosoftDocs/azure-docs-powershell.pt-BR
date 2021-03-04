---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 33c274154e122c0bb0925b8381d2dd51cad18264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886477"
---
# <span data-ttu-id="92011-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92011-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="92011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92011-102">SYNOPSIS</span></span>
<span data-ttu-id="92011-103">Define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="92011-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="92011-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92011-104">SYNTAX</span></span>

### <span data-ttu-id="92011-105">Expandido (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92011-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92011-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="92011-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92011-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92011-107">DESCRIPTION</span></span>
<span data-ttu-id="92011-108">O Set-AzKeyVaultCertificateIssuer cmdlet define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="92011-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="92011-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92011-109">EXAMPLES</span></span>

### <span data-ttu-id="92011-110">Exemplo 1: Definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="92011-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="92011-111">Este comando define as propriedades de um emissor de certificado.</span><span class="sxs-lookup"><span data-stu-id="92011-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="92011-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92011-112">PARAMETERS</span></span>

### <span data-ttu-id="92011-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="92011-113">-AccountId</span></span>
<span data-ttu-id="92011-114">Especifica a ID da conta para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="92011-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="92011-115">-ApiKey</span></span>
<span data-ttu-id="92011-116">Especifica a chave da API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="92011-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92011-117">-DefaultProfile</span></span>
<span data-ttu-id="92011-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="92011-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92011-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92011-119">-InputObject</span></span>
<span data-ttu-id="92011-120">Especifica o emissor do certificado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="92011-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92011-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="92011-121">-IssuerProvider</span></span>
<span data-ttu-id="92011-122">Especifica o tipo de emissor de certificado.</span><span class="sxs-lookup"><span data-stu-id="92011-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-123">-Name</span><span class="sxs-lookup"><span data-stu-id="92011-123">-Name</span></span>
<span data-ttu-id="92011-124">Especifica o nome do Emissor.</span><span class="sxs-lookup"><span data-stu-id="92011-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="92011-125">-OrganizationDetails</span></span>
<span data-ttu-id="92011-126">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="92011-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92011-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92011-127">-PassThru</span></span>
<span data-ttu-id="92011-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="92011-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92011-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="92011-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="92011-130">-VaultName</span></span>
<span data-ttu-id="92011-131">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="92011-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92011-132">-Confirm</span></span>
<span data-ttu-id="92011-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92011-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92011-134">-WhatIf</span></span>
<span data-ttu-id="92011-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92011-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92011-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92011-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92011-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92011-137">CommonParameters</span></span>
<span data-ttu-id="92011-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92011-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92011-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92011-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92011-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92011-140">INPUTS</span></span>

### <span data-ttu-id="92011-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="92011-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="92011-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="92011-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="92011-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92011-143">OUTPUTS</span></span>

### <span data-ttu-id="92011-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="92011-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="92011-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="92011-145">NOTES</span></span>

## <span data-ttu-id="92011-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92011-146">RELATED LINKS</span></span>

[<span data-ttu-id="92011-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92011-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="92011-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92011-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

