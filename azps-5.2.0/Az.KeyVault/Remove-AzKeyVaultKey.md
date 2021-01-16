---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: e78b6729061efe5a83f31bd25b9e542c09627ca3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258652"
---
# <span data-ttu-id="82756-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82756-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="82756-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82756-102">SYNOPSIS</span></span>
<span data-ttu-id="82756-103">Exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="82756-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="82756-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82756-104">SYNTAX</span></span>

### <span data-ttu-id="82756-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="82756-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82756-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="82756-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82756-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="82756-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82756-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82756-108">DESCRIPTION</span></span>
<span data-ttu-id="82756-109">O cmdlet Remove-AzKeyVaultKey exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="82756-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="82756-110">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzKeyVaultKeyRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="82756-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="82756-111">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="82756-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="82756-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82756-112">EXAMPLES</span></span>

### <span data-ttu-id="82756-113">Exemplo 1: remover uma chave de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="82756-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="82756-114">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="82756-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="82756-115">Exemplo 2: remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="82756-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="82756-116">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="82756-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="82756-117">O comando especifica o parâmetro *Force* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="82756-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="82756-118">Exemplo 3: limpar uma chave excluída do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="82756-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="82756-119">Esse comando Remove a chave denominada ITSoftware do cofre de chaves chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="82756-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="82756-120">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="82756-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="82756-121">Exemplo 4: remover chaves usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="82756-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="82756-122">Esse comando obtém todas as chaves no cofre de chaves chamado contoso e passa-as para o cmdlet **WHERE do objeto** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="82756-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="82756-123">Esse cmdlet passa as chaves que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="82756-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="82756-124">Esse cmdlet Remove essas chaves.</span><span class="sxs-lookup"><span data-stu-id="82756-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="82756-125">OS</span><span class="sxs-lookup"><span data-stu-id="82756-125">PARAMETERS</span></span>

### <span data-ttu-id="82756-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82756-126">-DefaultProfile</span></span>
<span data-ttu-id="82756-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="82756-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82756-128">-Force</span><span class="sxs-lookup"><span data-stu-id="82756-128">-Force</span></span>
<span data-ttu-id="82756-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="82756-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82756-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="82756-130">-HsmName</span></span>
<span data-ttu-id="82756-131">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="82756-131">HSM name.</span></span> <span data-ttu-id="82756-132">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="82756-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="82756-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82756-133">-InputObject</span></span>
<span data-ttu-id="82756-134">Objeto keybundle</span><span class="sxs-lookup"><span data-stu-id="82756-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="82756-135">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="82756-135">-InRemovedState</span></span>
<span data-ttu-id="82756-136">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="82756-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="82756-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="82756-137">-Name</span></span>
<span data-ttu-id="82756-138">Especifica o nome da chave a ser removida.</span><span class="sxs-lookup"><span data-stu-id="82756-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="82756-139">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="82756-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="82756-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82756-140">-PassThru</span></span>
<span data-ttu-id="82756-141">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="82756-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="82756-142">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="82756-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82756-143">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="82756-143">-VaultName</span></span>
<span data-ttu-id="82756-144">Especifica o nome do cofre de chaves do qual a chave será removida.</span><span class="sxs-lookup"><span data-stu-id="82756-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="82756-145">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="82756-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="82756-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82756-146">-Confirm</span></span>
<span data-ttu-id="82756-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82756-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82756-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82756-148">-WhatIf</span></span>
<span data-ttu-id="82756-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82756-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82756-150">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82756-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82756-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82756-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82756-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82756-152">CommonParameters</span></span>
<span data-ttu-id="82756-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82756-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82756-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82756-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82756-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82756-155">INPUTS</span></span>

### <span data-ttu-id="82756-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="82756-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="82756-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82756-157">OUTPUTS</span></span>

### <span data-ttu-id="82756-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82756-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="82756-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82756-159">NOTES</span></span>

## <span data-ttu-id="82756-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82756-160">RELATED LINKS</span></span>

[<span data-ttu-id="82756-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82756-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="82756-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="82756-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="82756-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="82756-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="82756-164">Desfazer-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="82756-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

