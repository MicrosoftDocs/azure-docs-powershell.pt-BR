---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: f1491fcf42ace90efa012778cfb5fec7faeaee07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888694"
---
# <span data-ttu-id="d3657-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3657-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d3657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3657-102">SYNOPSIS</span></span>
<span data-ttu-id="d3657-103">Remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d3657-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="d3657-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3657-104">SYNTAX</span></span>

### <span data-ttu-id="d3657-105">ByVaultNameAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3657-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3657-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="d3657-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3657-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3657-107">DESCRIPTION</span></span>
<span data-ttu-id="d3657-108">O cmdlet **Remove-AzKeyVaultCertificate** remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d3657-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="d3657-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3657-109">EXAMPLES</span></span>

### <span data-ttu-id="d3657-110">Exemplo 1: Remover um certificado</span><span class="sxs-lookup"><span data-stu-id="d3657-110">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="d3657-111">Este comando remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d3657-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="d3657-112">Este comando especifica o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="d3657-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d3657-113">Portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="d3657-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d3657-114">Exemplo 2: limpar permanentemente o certificado excluído do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="d3657-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="d3657-115">Esse comando remove permanentemente o certificado chamado 'MyCert' do cofre de chaves chamado 'Contoso'.</span><span class="sxs-lookup"><span data-stu-id="d3657-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="d3657-116">A execução desse cmdlet requer a permissão de "limpeza", que deve ter sido concedida anteriormente e explicitamente ao usuário neste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d3657-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="d3657-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3657-117">PARAMETERS</span></span>

### <span data-ttu-id="d3657-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3657-118">-DefaultProfile</span></span>
<span data-ttu-id="d3657-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d3657-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3657-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d3657-120">-Force</span></span>
<span data-ttu-id="d3657-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d3657-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3657-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3657-122">-InputObject</span></span>
<span data-ttu-id="d3657-123">Objeto Certificate.</span><span class="sxs-lookup"><span data-stu-id="d3657-123">Certificate Object.</span></span>

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

### <span data-ttu-id="d3657-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d3657-124">-InRemovedState</span></span>
<span data-ttu-id="d3657-125">Se presente, remove permanentemente o certificado excluído anteriormente</span><span class="sxs-lookup"><span data-stu-id="d3657-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="d3657-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d3657-126">-Name</span></span>
<span data-ttu-id="d3657-127">Especifica o nome do certificado que esse cmdlet remove de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d3657-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="d3657-128">Este cmdlet constrói o FQDN (nome de domínio totalmente qualificado) de um certificado com base no nome especificado por esse parâmetro, o nome do cofre de chaves e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d3657-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="d3657-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3657-129">-PassThru</span></span>
<span data-ttu-id="d3657-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d3657-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3657-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d3657-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3657-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d3657-132">-VaultName</span></span>
<span data-ttu-id="d3657-133">Especifica o nome do cofre de chaves do qual este cmdlet remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="d3657-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="d3657-134">Este cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado por esse parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d3657-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d3657-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3657-135">-Confirm</span></span>
<span data-ttu-id="d3657-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3657-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3657-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3657-137">-WhatIf</span></span>
<span data-ttu-id="d3657-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3657-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3657-139">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3657-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3657-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3657-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3657-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3657-141">CommonParameters</span></span>
<span data-ttu-id="d3657-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3657-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3657-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3657-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3657-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3657-144">INPUTS</span></span>

### <span data-ttu-id="d3657-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d3657-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="d3657-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3657-146">OUTPUTS</span></span>

### <span data-ttu-id="d3657-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3657-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="d3657-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3657-148">NOTES</span></span>

## <span data-ttu-id="d3657-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3657-149">RELATED LINKS</span></span>

[<span data-ttu-id="d3657-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3657-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="d3657-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3657-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="d3657-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3657-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="d3657-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d3657-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
