---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 7c3ad97a2896104d9c60c1e24b7ea844b3a090a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596129"
---
# <span data-ttu-id="e7a40-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e7a40-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e7a40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7a40-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a40-103">Modifica atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="e7a40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a40-104">SYNTAX</span></span>

### <span data-ttu-id="e7a40-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7a40-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7a40-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7a40-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a40-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7a40-107">DESCRIPTION</span></span>
<span data-ttu-id="e7a40-108">O cmdlet **Update-AzKeyVaultCertificate** modifica os atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="e7a40-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7a40-109">EXAMPLES</span></span>

### <span data-ttu-id="e7a40-110">Exemplo 1: modificar as marcas associadas a um certificado</span><span class="sxs-lookup"><span data-stu-id="e7a40-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="e7a40-111">O primeiro comando atribui uma matriz de pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="e7a40-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="e7a40-112">O segundo comando define o valor de marcas do certificado chamado TestCert01 para ser $Tags.</span><span class="sxs-lookup"><span data-stu-id="e7a40-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="e7a40-113">OS</span><span class="sxs-lookup"><span data-stu-id="e7a40-113">PARAMETERS</span></span>

### <span data-ttu-id="e7a40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a40-114">-DefaultProfile</span></span>
<span data-ttu-id="e7a40-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a40-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="e7a40-116">-Enable</span></span>
<span data-ttu-id="e7a40-117">Se houver, habilite um certificado se value for true.</span><span class="sxs-lookup"><span data-stu-id="e7a40-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="e7a40-118">Desabilitar um certificado se o valor for false.</span><span class="sxs-lookup"><span data-stu-id="e7a40-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="e7a40-119">Se não for especificado, o valor existente do estado habilitado/desabilitado do certificado permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a40-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a40-120">-InputObject</span></span>
<span data-ttu-id="e7a40-121">Objeto Certificate</span><span class="sxs-lookup"><span data-stu-id="e7a40-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7a40-122">-Name</span></span>
<span data-ttu-id="e7a40-123">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-123">Certificate name.</span></span>
<span data-ttu-id="e7a40-124">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="e7a40-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a40-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7a40-125">-PassThru</span></span>
<span data-ttu-id="e7a40-126">O cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e7a40-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="e7a40-127">Se essa opção for especificada, retorne o objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="e7a40-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="e7a40-128">-Tag</span></span>
<span data-ttu-id="e7a40-129">Uma Hashtable representando as marcas de certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="e7a40-130">Se não for especificado, as marcas existentes do sertificate permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="e7a40-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="e7a40-131">Remova uma marca especificando uma Hashtable vazia.</span><span class="sxs-lookup"><span data-stu-id="e7a40-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a40-132">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e7a40-132">-VaultName</span></span>
<span data-ttu-id="e7a40-133">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="e7a40-133">Vault name.</span></span>
<span data-ttu-id="e7a40-134">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e7a40-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e7a40-135">-Versão</span><span class="sxs-lookup"><span data-stu-id="e7a40-135">-Version</span></span>
<span data-ttu-id="e7a40-136">Versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-136">Certificate version.</span></span>
<span data-ttu-id="e7a40-137">O cmdlet constrói o FQDN de um certificado do nome do cofre, ambiente selecionado atualmente, nome do certificado e versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a40-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7a40-138">-Confirm</span></span>
<span data-ttu-id="e7a40-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a40-140">-WhatIf</span></span>
<span data-ttu-id="e7a40-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a40-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7a40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a40-143">CommonParameters</span></span>
<span data-ttu-id="e7a40-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a40-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a40-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a40-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7a40-146">INPUTS</span></span>

### <span data-ttu-id="e7a40-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e7a40-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="e7a40-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7a40-148">OUTPUTS</span></span>

### <span data-ttu-id="e7a40-149">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e7a40-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="e7a40-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7a40-150">NOTES</span></span>

## <span data-ttu-id="e7a40-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7a40-151">RELATED LINKS</span></span>
