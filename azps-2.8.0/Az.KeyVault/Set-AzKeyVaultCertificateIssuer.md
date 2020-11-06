---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: fdb90d670034e87c4a08c316b73d4bd15614d872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596150"
---
# <span data-ttu-id="6261e-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6261e-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6261e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6261e-102">SYNOPSIS</span></span>
<span data-ttu-id="6261e-103">Define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6261e-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="6261e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6261e-104">SYNTAX</span></span>

### <span data-ttu-id="6261e-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="6261e-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6261e-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="6261e-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6261e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6261e-107">DESCRIPTION</span></span>
<span data-ttu-id="6261e-108">O cmdlet Set-AzKeyVaultCertificateIssuer define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6261e-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="6261e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6261e-109">EXAMPLES</span></span>

### <span data-ttu-id="6261e-110">Exemplo 1: definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="6261e-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="6261e-111">Esse comando define as propriedades de um emissor de certificado.</span><span class="sxs-lookup"><span data-stu-id="6261e-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="6261e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6261e-112">PARAMETERS</span></span>

### <span data-ttu-id="6261e-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="6261e-113">-AccountId</span></span>
<span data-ttu-id="6261e-114">Especifica a ID da conta para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="6261e-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="6261e-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="6261e-115">-ApiKey</span></span>
<span data-ttu-id="6261e-116">Especifica a chave de API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="6261e-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="6261e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6261e-117">-DefaultProfile</span></span>
<span data-ttu-id="6261e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6261e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6261e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6261e-119">-InputObject</span></span>
<span data-ttu-id="6261e-120">Especifica o emissor do certificado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="6261e-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="6261e-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="6261e-121">-IssuerProvider</span></span>
<span data-ttu-id="6261e-122">Especifica o tipo de emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="6261e-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="6261e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6261e-123">-Name</span></span>
<span data-ttu-id="6261e-124">Especifica o nome do emissor.</span><span class="sxs-lookup"><span data-stu-id="6261e-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="6261e-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6261e-125">-OrganizationDetails</span></span>
<span data-ttu-id="6261e-126">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="6261e-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="6261e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6261e-127">-PassThru</span></span>
<span data-ttu-id="6261e-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6261e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6261e-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6261e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6261e-130">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="6261e-130">-VaultName</span></span>
<span data-ttu-id="6261e-131">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6261e-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="6261e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6261e-132">-Confirm</span></span>
<span data-ttu-id="6261e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6261e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6261e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6261e-134">-WhatIf</span></span>
<span data-ttu-id="6261e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6261e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6261e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6261e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6261e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6261e-137">CommonParameters</span></span>
<span data-ttu-id="6261e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6261e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6261e-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6261e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6261e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6261e-140">INPUTS</span></span>

### <span data-ttu-id="6261e-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6261e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="6261e-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6261e-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="6261e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6261e-143">OUTPUTS</span></span>

### <span data-ttu-id="6261e-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6261e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6261e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6261e-145">NOTES</span></span>

## <span data-ttu-id="6261e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6261e-146">RELATED LINKS</span></span>

[<span data-ttu-id="6261e-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6261e-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6261e-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6261e-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

