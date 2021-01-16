---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256829"
---
# <span data-ttu-id="10be4-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="10be4-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="10be4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10be4-102">SYNOPSIS</span></span>
<span data-ttu-id="10be4-103">Remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="10be4-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="10be4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10be4-104">SYNTAX</span></span>

### <span data-ttu-id="10be4-105">ByVaultNameAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="10be4-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10be4-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="10be4-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10be4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10be4-107">DESCRIPTION</span></span>
<span data-ttu-id="10be4-108">O cmdlet **Remove-AzKeyVaultCertificate** remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="10be4-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="10be4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10be4-109">EXAMPLES</span></span>

### <span data-ttu-id="10be4-110">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="10be4-110">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="10be4-111">Esse comando Remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="10be4-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="10be4-112">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="10be4-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="10be4-113">Portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="10be4-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="10be4-114">Exemplo 2: limpar permanentemente o certificado excluído do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="10be4-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="10be4-115">Esse comando remove permanentemente o certificado chamado ' MyCert ' do cofre de chaves chamado ' contoso '.</span><span class="sxs-lookup"><span data-stu-id="10be4-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="10be4-116">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário neste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="10be4-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="10be4-117">OS</span><span class="sxs-lookup"><span data-stu-id="10be4-117">PARAMETERS</span></span>

### <span data-ttu-id="10be4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10be4-118">-DefaultProfile</span></span>
<span data-ttu-id="10be4-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="10be4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10be4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="10be4-120">-Force</span></span>
<span data-ttu-id="10be4-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="10be4-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10be4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10be4-122">-InputObject</span></span>
<span data-ttu-id="10be4-123">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="10be4-123">Certificate Object.</span></span>

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

### <span data-ttu-id="10be4-124">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="10be4-124">-InRemovedState</span></span>
<span data-ttu-id="10be4-125">Se presente, remove permanentemente o certificado excluído anteriormente</span><span class="sxs-lookup"><span data-stu-id="10be4-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="10be4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="10be4-126">-Name</span></span>
<span data-ttu-id="10be4-127">Especifica o nome do certificado que este cmdlet Remove de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="10be4-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="10be4-128">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="10be4-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="10be4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10be4-129">-PassThru</span></span>
<span data-ttu-id="10be4-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="10be4-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="10be4-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="10be4-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="10be4-132">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="10be4-132">-VaultName</span></span>
<span data-ttu-id="10be4-133">Especifica o nome do cofre de chaves do qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="10be4-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="10be4-134">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="10be4-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="10be4-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10be4-135">-Confirm</span></span>
<span data-ttu-id="10be4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10be4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10be4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10be4-137">-WhatIf</span></span>
<span data-ttu-id="10be4-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10be4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10be4-139">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10be4-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10be4-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10be4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10be4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10be4-141">CommonParameters</span></span>
<span data-ttu-id="10be4-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10be4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10be4-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10be4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10be4-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10be4-144">INPUTS</span></span>

### <span data-ttu-id="10be4-145">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="10be4-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="10be4-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10be4-146">OUTPUTS</span></span>

### <span data-ttu-id="10be4-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="10be4-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="10be4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10be4-148">NOTES</span></span>

## <span data-ttu-id="10be4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10be4-149">RELATED LINKS</span></span>

[<span data-ttu-id="10be4-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="10be4-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="10be4-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="10be4-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="10be4-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="10be4-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="10be4-153">Desfazer-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="10be4-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
