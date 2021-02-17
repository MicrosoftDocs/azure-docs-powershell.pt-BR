---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: afa9f59520cba9f90f0f5d0a2edb6564b73245bf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399236"
---
# <span data-ttu-id="1adfa-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1adfa-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="1adfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1adfa-102">SYNOPSIS</span></span>
<span data-ttu-id="1adfa-103">Exclui uma chave em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="1adfa-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="1adfa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1adfa-104">SYNTAX</span></span>

### <span data-ttu-id="1adfa-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1adfa-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1adfa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1adfa-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1adfa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1adfa-107">DESCRIPTION</span></span>
<span data-ttu-id="1adfa-108">O Remove-AzKeyVaultKey cmdlet exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1adfa-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="1adfa-109">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzKeyVaultKeyRemoval um usuário com permissões especiais de "recuperar".</span><span class="sxs-lookup"><span data-stu-id="1adfa-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="1adfa-110">Este cmdlet tem um valor alto para a **propriedade ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="1adfa-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="1adfa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1adfa-111">EXAMPLES</span></span>

### <span data-ttu-id="1adfa-112">Exemplo 1: Remover uma chave de um cofre de chave</span><span class="sxs-lookup"><span data-stu-id="1adfa-112">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="1adfa-113">Esse comando remove a chave chamada ITSoftware do cofre de teclas chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="1adfa-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="1adfa-114">Exemplo 2: Remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="1adfa-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="1adfa-115">Esse comando remove a chave chamada ITSoftware do cofre de teclas chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="1adfa-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="1adfa-116">O comando especifica o parâmetro *Forçar* e, portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1adfa-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="1adfa-117">Exemplo 3: limpar permanentemente uma chave excluída do cofre de chave</span><span class="sxs-lookup"><span data-stu-id="1adfa-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="1adfa-118">Esse comando remove permanentemente a chave chamada ITSoftware do cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="1adfa-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="1adfa-119">Executar este cmdlet requer a permissão de "limpeza", que deve ter sido concedida explicitamente ao usuário para esse cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="1adfa-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="1adfa-120">Exemplo 4: Remover teclas usando o operador de pipeline</span><span class="sxs-lookup"><span data-stu-id="1adfa-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="1adfa-121">Esse comando obtém todas as chaves no cofre de teclas chamado Contoso e passa-as para o cmdlet **Where-Object** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1adfa-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1adfa-122">Esse cmdlet passa as teclas que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1adfa-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="1adfa-123">Esse cmdlet remove essas teclas.</span><span class="sxs-lookup"><span data-stu-id="1adfa-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="1adfa-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1adfa-124">PARAMETERS</span></span>

### <span data-ttu-id="1adfa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adfa-125">-DefaultProfile</span></span>
<span data-ttu-id="1adfa-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1adfa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1adfa-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1adfa-127">-Force</span></span>
<span data-ttu-id="1adfa-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1adfa-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1adfa-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1adfa-129">-InputObject</span></span>
<span data-ttu-id="1adfa-130">Objeto KeyBundle</span><span class="sxs-lookup"><span data-stu-id="1adfa-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="1adfa-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1adfa-131">-InRemovedState</span></span>
<span data-ttu-id="1adfa-132">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1adfa-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="1adfa-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="1adfa-133">-Name</span></span>
<span data-ttu-id="1adfa-134">Especifica o nome da chave a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1adfa-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="1adfa-135">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome especificado por esse parâmetro, o nome do cofre de chave e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="1adfa-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1adfa-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1adfa-136">-PassThru</span></span>
<span data-ttu-id="1adfa-137">Indica que esse cmdlet retorna um objeto **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="1adfa-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="1adfa-138">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="1adfa-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1adfa-139">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="1adfa-139">-VaultName</span></span>
<span data-ttu-id="1adfa-140">Especifica o nome do cofre de chave do qual a chave deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="1adfa-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="1adfa-141">Esse cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="1adfa-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="1adfa-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1adfa-142">-Confirm</span></span>
<span data-ttu-id="1adfa-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1adfa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1adfa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1adfa-144">-WhatIf</span></span>
<span data-ttu-id="1adfa-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1adfa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1adfa-146">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1adfa-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1adfa-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1adfa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1adfa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adfa-148">CommonParameters</span></span>
<span data-ttu-id="1adfa-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adfa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adfa-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1adfa-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adfa-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="1adfa-151">INPUTS</span></span>

### <span data-ttu-id="1adfa-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1adfa-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="1adfa-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="1adfa-153">OUTPUTS</span></span>

### <span data-ttu-id="1adfa-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1adfa-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="1adfa-155">Notas</span><span class="sxs-lookup"><span data-stu-id="1adfa-155">NOTES</span></span>

## <span data-ttu-id="1adfa-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1adfa-156">RELATED LINKS</span></span>

[<span data-ttu-id="1adfa-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1adfa-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1adfa-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1adfa-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="1adfa-159">Desfazer-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1adfa-159">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

