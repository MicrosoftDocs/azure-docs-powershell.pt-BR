---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113101"
---
# <span data-ttu-id="d1fe4-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1fe4-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="d1fe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fe4-103">Exclui uma chave em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="d1fe4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1fe4-104">SYNTAX</span></span>

### <span data-ttu-id="d1fe4-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1fe4-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fe4-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="d1fe4-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fe4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1fe4-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1fe4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1fe4-108">DESCRIPTION</span></span>
<span data-ttu-id="d1fe4-109">O Remove-AzKeyVaultKey cmdlet exclui uma chave em um cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="d1fe4-110">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzKeyVaultKeyRemoval um usuário com permissões especiais de "recuperar".</span><span class="sxs-lookup"><span data-stu-id="d1fe4-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="d1fe4-111">Este cmdlet tem um valor alto para a **propriedade ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="d1fe4-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="d1fe4-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1fe4-112">EXAMPLES</span></span>

### <span data-ttu-id="d1fe4-113">Exemplo 1: Remover uma chave de um cofre de chave</span><span class="sxs-lookup"><span data-stu-id="d1fe4-113">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d1fe4-114">Esse comando remove a chave chamada ITSoftware do cofre de teclas chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="d1fe4-115">Exemplo 2: Remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="d1fe4-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="d1fe4-116">Esse comando remove a chave chamada ITSoftware do cofre de teclas chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="d1fe4-117">O comando especifica o parâmetro *Forçar* e, portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d1fe4-118">Exemplo 3: limpar permanentemente uma chave excluída do cofre de chave</span><span class="sxs-lookup"><span data-stu-id="d1fe4-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="d1fe4-119">Esse comando remove permanentemente a chave chamada ITSoftware do cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="d1fe4-120">Executar este cmdlet requer a permissão de "limpeza", que deve ter sido concedida explicitamente ao usuário para esse cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="d1fe4-121">Exemplo 4: Remover teclas usando o operador de pipeline</span><span class="sxs-lookup"><span data-stu-id="d1fe4-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="d1fe4-122">Esse comando obtém todas as chaves no cofre de teclas chamado Contoso e passa-as para o cmdlet **Where-Object** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d1fe4-123">Esse cmdlet passa as teclas que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="d1fe4-124">Esse cmdlet remove essas teclas.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="d1fe4-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1fe4-125">PARAMETERS</span></span>

### <span data-ttu-id="d1fe4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fe4-126">-DefaultProfile</span></span>
<span data-ttu-id="d1fe4-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d1fe4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1fe4-128">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d1fe4-128">-Force</span></span>
<span data-ttu-id="d1fe4-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1fe4-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d1fe4-130">-HsmName</span></span>
<span data-ttu-id="d1fe4-131">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-131">HSM name.</span></span> <span data-ttu-id="d1fe4-132">O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1fe4-133">-InputObject</span></span>
<span data-ttu-id="d1fe4-134">Objeto KeyBundle</span><span class="sxs-lookup"><span data-stu-id="d1fe4-134">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe4-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d1fe4-135">-InRemovedState</span></span>
<span data-ttu-id="d1fe4-136">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="d1fe4-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1fe4-137">-Name</span></span>
<span data-ttu-id="d1fe4-138">Especifica o nome da chave a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="d1fe4-139">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome especificado por esse parâmetro, o nome do cofre de chave e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe4-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1fe4-140">-PassThru</span></span>
<span data-ttu-id="d1fe4-141">Indica que esse cmdlet retorna um objeto **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="d1fe4-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="d1fe4-142">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1fe4-143">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="d1fe4-143">-VaultName</span></span>
<span data-ttu-id="d1fe4-144">Especifica o nome do cofre de chave do qual a chave deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="d1fe4-145">Esse cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe4-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d1fe4-146">-Confirm</span></span>
<span data-ttu-id="d1fe4-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fe4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fe4-148">-WhatIf</span></span>
<span data-ttu-id="d1fe4-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fe4-150">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fe4-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fe4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fe4-152">CommonParameters</span></span>
<span data-ttu-id="d1fe4-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fe4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fe4-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1fe4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fe4-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1fe4-155">INPUTS</span></span>

### <span data-ttu-id="d1fe4-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d1fe4-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="d1fe4-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1fe4-157">OUTPUTS</span></span>

### <span data-ttu-id="d1fe4-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1fe4-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d1fe4-159">Notas</span><span class="sxs-lookup"><span data-stu-id="d1fe4-159">NOTES</span></span>

## <span data-ttu-id="d1fe4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1fe4-160">RELATED LINKS</span></span>

[<span data-ttu-id="d1fe4-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1fe4-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d1fe4-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1fe4-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="d1fe4-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d1fe4-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="d1fe4-164">Desfazer-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d1fe4-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

