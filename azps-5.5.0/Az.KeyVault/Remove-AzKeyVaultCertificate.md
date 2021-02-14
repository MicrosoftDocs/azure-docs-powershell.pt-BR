---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116715"
---
# <span data-ttu-id="3cdd8-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3cdd8-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3cdd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cdd8-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdd8-103">Remove um certificado de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="3cdd8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cdd8-104">SYNTAX</span></span>

### <span data-ttu-id="3cdd8-105">ByVaultNameAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3cdd8-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cdd8-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="3cdd8-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cdd8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cdd8-107">DESCRIPTION</span></span>
<span data-ttu-id="3cdd8-108">O cmdlet **Remove-AzKeyVaultCertificate** remove um certificado de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="3cdd8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3cdd8-109">EXAMPLES</span></span>

### <span data-ttu-id="3cdd8-110">Exemplo 1: Remover um certificado</span><span class="sxs-lookup"><span data-stu-id="3cdd8-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="3cdd8-111">Esse comando remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="3cdd8-112">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="3cdd8-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3cdd8-113">Portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="3cdd8-114">Exemplo 2: limpar permanentemente o certificado excluído do cofre de chave</span><span class="sxs-lookup"><span data-stu-id="3cdd8-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="3cdd8-115">Esse comando remove permanentemente o certificado chamado 'MeuCert' do cofre de chaves chamado 'Contoso'.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="3cdd8-116">Executar este cmdlet requer a permissão de "limpeza", que deve ter sido concedida explicitamente ao usuário neste cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="3cdd8-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cdd8-117">PARAMETERS</span></span>

### <span data-ttu-id="3cdd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdd8-118">-DefaultProfile</span></span>
<span data-ttu-id="3cdd8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3cdd8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cdd8-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3cdd8-120">-Force</span></span>
<span data-ttu-id="3cdd8-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3cdd8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cdd8-122">-InputObject</span></span>
<span data-ttu-id="3cdd8-123">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cdd8-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3cdd8-124">-InRemovedState</span></span>
<span data-ttu-id="3cdd8-125">Se estiver presente, removerá permanentemente o certificado excluído anteriormente</span><span class="sxs-lookup"><span data-stu-id="3cdd8-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="3cdd8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cdd8-126">-Name</span></span>
<span data-ttu-id="3cdd8-127">Especifica o nome do certificado que este cmdlet remove de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="3cdd8-128">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de um certificado com base no nome especificado por esse parâmetro, o nome do cofre de chave e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdd8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cdd8-129">-PassThru</span></span>
<span data-ttu-id="3cdd8-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3cdd8-131">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3cdd8-132">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="3cdd8-132">-VaultName</span></span>
<span data-ttu-id="3cdd8-133">Especifica o nome do cofre de chave do qual este cmdlet remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="3cdd8-134">Esse cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdd8-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3cdd8-135">-Confirm</span></span>
<span data-ttu-id="3cdd8-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdd8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cdd8-137">-WhatIf</span></span>
<span data-ttu-id="3cdd8-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cdd8-139">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cdd8-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cdd8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdd8-141">CommonParameters</span></span>
<span data-ttu-id="3cdd8-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdd8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdd8-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cdd8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdd8-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="3cdd8-144">INPUTS</span></span>

### <span data-ttu-id="3cdd8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3cdd8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="3cdd8-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="3cdd8-146">OUTPUTS</span></span>

### <span data-ttu-id="3cdd8-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3cdd8-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="3cdd8-148">Notas</span><span class="sxs-lookup"><span data-stu-id="3cdd8-148">NOTES</span></span>

## <span data-ttu-id="3cdd8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cdd8-149">RELATED LINKS</span></span>

[<span data-ttu-id="3cdd8-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3cdd8-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="3cdd8-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3cdd8-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="3cdd8-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3cdd8-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="3cdd8-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="3cdd8-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
