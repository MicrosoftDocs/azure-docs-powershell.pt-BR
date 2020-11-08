---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115289"
---
# <span data-ttu-id="2059f-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="2059f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2059f-102">SYNOPSIS</span></span>
<span data-ttu-id="2059f-103">Exclui uma chave em um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2059f-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="2059f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2059f-104">SYNTAX</span></span>

### <span data-ttu-id="2059f-105">RemoveByKeyNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2059f-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2059f-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2059f-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2059f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2059f-107">DESCRIPTION</span></span>
<span data-ttu-id="2059f-108">O cmdlet Remove-AzManagedHsmKey exclui uma chave em um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2059f-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="2059f-109">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzManagedHsmKeyRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="2059f-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="2059f-110">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="2059f-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="2059f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2059f-111">EXAMPLES</span></span>

### <span data-ttu-id="2059f-112">Exemplo 1: remover uma chave de um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="2059f-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="2059f-113">Esse comando Remove a chave chamada TestKey do HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="2059f-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="2059f-114">Exemplo 2: remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="2059f-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="2059f-115">Esse comando Remove a chave chamada TestKey do HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="2059f-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="2059f-116">O comando especifica o parâmetro *Force* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="2059f-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2059f-117">Exemplo 3: limpar uma chave excluída do HSM gerenciado permanentemente</span><span class="sxs-lookup"><span data-stu-id="2059f-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="2059f-118">Esse comando Remove a chave chamada TestKey do HSM gerenciado chamado testmhsm permanentemente.</span><span class="sxs-lookup"><span data-stu-id="2059f-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="2059f-119">Executar esse cmdlet requer a permissão ' purge ', que deve ser anteriormente e explicitamente concedida ao usuário para esse HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2059f-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="2059f-120">Exemplo 4: remover chaves usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="2059f-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="2059f-121">Esse comando obtém todas as chaves no HSM gerenciado chamado testmhsm e passa-as para o cmdlet **WHERE do objeto** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="2059f-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2059f-122">Esse cmdlet passa as chaves que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2059f-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="2059f-123">Esse cmdlet Remove essas chaves.</span><span class="sxs-lookup"><span data-stu-id="2059f-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="2059f-124">OS</span><span class="sxs-lookup"><span data-stu-id="2059f-124">PARAMETERS</span></span>

### <span data-ttu-id="2059f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2059f-125">-DefaultProfile</span></span>
<span data-ttu-id="2059f-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2059f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2059f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2059f-127">-Force</span></span>
<span data-ttu-id="2059f-128">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2059f-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2059f-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2059f-129">-HsmName</span></span>
<span data-ttu-id="2059f-130">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="2059f-130">HSM name.</span></span> <span data-ttu-id="2059f-131">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2059f-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2059f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2059f-132">-InputObject</span></span>
<span data-ttu-id="2059f-133">Objeto-chave</span><span class="sxs-lookup"><span data-stu-id="2059f-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2059f-134">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="2059f-134">-InRemovedState</span></span>
<span data-ttu-id="2059f-135">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2059f-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="2059f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="2059f-136">-Name</span></span>
<span data-ttu-id="2059f-137">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="2059f-137">Key name.</span></span>
<span data-ttu-id="2059f-138">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="2059f-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2059f-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2059f-139">-PassThru</span></span>
<span data-ttu-id="2059f-140">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="2059f-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2059f-141">Se essa opção for especificada, o cmdlet retornará o objeto de chave que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="2059f-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="2059f-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2059f-142">-Confirm</span></span>
<span data-ttu-id="2059f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2059f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2059f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2059f-144">-WhatIf</span></span>
<span data-ttu-id="2059f-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2059f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2059f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2059f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2059f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2059f-147">CommonParameters</span></span>
<span data-ttu-id="2059f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2059f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2059f-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2059f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2059f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2059f-150">INPUTS</span></span>

### <span data-ttu-id="2059f-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2059f-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="2059f-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2059f-152">OUTPUTS</span></span>

### <span data-ttu-id="2059f-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2059f-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="2059f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2059f-154">NOTES</span></span>

## <span data-ttu-id="2059f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2059f-155">RELATED LINKS</span></span>

[<span data-ttu-id="2059f-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="2059f-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="2059f-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="2059f-159">Desfazer-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2059f-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="2059f-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="2059f-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2059f-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)