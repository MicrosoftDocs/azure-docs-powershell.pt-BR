---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113094"
---
# <span data-ttu-id="31400-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="31400-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="31400-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31400-102">SYNOPSIS</span></span>
<span data-ttu-id="31400-103">Define um emissor de certificado em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="31400-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="31400-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31400-104">SYNTAX</span></span>

### <span data-ttu-id="31400-105">Expandido (Padrão)</span><span class="sxs-lookup"><span data-stu-id="31400-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31400-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="31400-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31400-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="31400-107">DESCRIPTION</span></span>
<span data-ttu-id="31400-108">O Set-AzKeyVaultCertificateIssuer cmdlet define um emissor de certificado em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="31400-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="31400-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31400-109">EXAMPLES</span></span>

### <span data-ttu-id="31400-110">Exemplo 1: Definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="31400-110">Example 1: Set a certificate issuer</span></span>
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

<span data-ttu-id="31400-111">Esse comando define as propriedades de um emissor de certificado.</span><span class="sxs-lookup"><span data-stu-id="31400-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="31400-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31400-112">PARAMETERS</span></span>

### <span data-ttu-id="31400-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="31400-113">-AccountId</span></span>
<span data-ttu-id="31400-114">Especifica a ID da conta do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="31400-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="31400-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="31400-115">-ApiKey</span></span>
<span data-ttu-id="31400-116">Especifica a chave da API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="31400-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="31400-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31400-117">-DefaultProfile</span></span>
<span data-ttu-id="31400-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="31400-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31400-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31400-119">-InputObject</span></span>
<span data-ttu-id="31400-120">Especifica o emissor do certificado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="31400-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="31400-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="31400-121">-IssuerProvider</span></span>
<span data-ttu-id="31400-122">Especifica o tipo de emissor de certificado.</span><span class="sxs-lookup"><span data-stu-id="31400-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="31400-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="31400-123">-Name</span></span>
<span data-ttu-id="31400-124">Especifica o nome do Emissor.</span><span class="sxs-lookup"><span data-stu-id="31400-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="31400-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="31400-125">-OrganizationDetails</span></span>
<span data-ttu-id="31400-126">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="31400-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="31400-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31400-127">-PassThru</span></span>
<span data-ttu-id="31400-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="31400-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="31400-129">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="31400-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31400-130">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="31400-130">-VaultName</span></span>
<span data-ttu-id="31400-131">Especifica o nome do cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="31400-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="31400-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="31400-132">-Confirm</span></span>
<span data-ttu-id="31400-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31400-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31400-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31400-134">-WhatIf</span></span>
<span data-ttu-id="31400-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="31400-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31400-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31400-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31400-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31400-137">CommonParameters</span></span>
<span data-ttu-id="31400-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31400-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31400-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31400-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31400-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="31400-140">INPUTS</span></span>

### <span data-ttu-id="31400-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="31400-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="31400-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="31400-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="31400-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="31400-143">OUTPUTS</span></span>

### <span data-ttu-id="31400-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="31400-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="31400-145">Notas</span><span class="sxs-lookup"><span data-stu-id="31400-145">NOTES</span></span>

## <span data-ttu-id="31400-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31400-146">RELATED LINKS</span></span>

[<span data-ttu-id="31400-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="31400-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="31400-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="31400-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

