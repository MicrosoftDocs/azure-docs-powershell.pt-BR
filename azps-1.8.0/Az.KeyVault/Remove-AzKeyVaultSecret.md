---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 2c52d6cbd5a3e027baf41959d28816f63062b046
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770616"
---
# <span data-ttu-id="0afe6-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0afe6-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="0afe6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0afe6-102">SYNOPSIS</span></span>
<span data-ttu-id="0afe6-103">Exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0afe6-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="0afe6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0afe6-104">SYNTAX</span></span>

### <span data-ttu-id="0afe6-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0afe6-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afe6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0afe6-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afe6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0afe6-107">DESCRIPTION</span></span>
<span data-ttu-id="0afe6-108">O cmdlet Remove-AzKeyVaultSecret exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0afe6-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="0afe6-109">Se o segredo foi excluído acidentalmente, o segredo pode ser recuperado usando Undo-AzKeyVaultSecretRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="0afe6-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="0afe6-110">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="0afe6-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="0afe6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0afe6-111">EXAMPLES</span></span>

### <span data-ttu-id="0afe6-112">Exemplo 1: remover um segredo de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="0afe6-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="0afe6-113">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso. '</span><span class="sxs-lookup"><span data-stu-id="0afe6-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="0afe6-114">Exemplo 2: remover um segredo de um cofre de chaves sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="0afe6-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="0afe6-115">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="0afe6-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="0afe6-116">O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="0afe6-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="0afe6-117">Exemplo 3: limpar o segredo excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="0afe6-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="0afe6-118">Esse comando premove o segredo nomeado FinanceSecret do cofre da chave chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="0afe6-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="0afe6-119">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0afe6-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="0afe6-120">OS</span><span class="sxs-lookup"><span data-stu-id="0afe6-120">PARAMETERS</span></span>

### <span data-ttu-id="0afe6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afe6-121">-DefaultProfile</span></span>
<span data-ttu-id="0afe6-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0afe6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0afe6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0afe6-123">-Force</span></span>
<span data-ttu-id="0afe6-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0afe6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0afe6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afe6-125">-InputObject</span></span>
<span data-ttu-id="0afe6-126">Objeto secreto do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="0afe6-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0afe6-127">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="0afe6-127">-InRemovedState</span></span>
<span data-ttu-id="0afe6-128">Se presente, remove o segredo anteriormente excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="0afe6-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="0afe6-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="0afe6-129">-Name</span></span>
<span data-ttu-id="0afe6-130">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="0afe6-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="0afe6-131">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="0afe6-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe6-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0afe6-132">-PassThru</span></span>
<span data-ttu-id="0afe6-133">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="0afe6-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="0afe6-134">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0afe6-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0afe6-135">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0afe6-135">-VaultName</span></span>
<span data-ttu-id="0afe6-136">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="0afe6-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="0afe6-137">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="0afe6-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0afe6-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0afe6-138">-Confirm</span></span>
<span data-ttu-id="0afe6-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afe6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afe6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afe6-140">-WhatIf</span></span>
<span data-ttu-id="0afe6-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0afe6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afe6-142">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0afe6-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afe6-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0afe6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afe6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afe6-144">CommonParameters</span></span>
<span data-ttu-id="0afe6-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afe6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afe6-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afe6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afe6-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0afe6-147">INPUTS</span></span>

### <span data-ttu-id="0afe6-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0afe6-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="0afe6-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0afe6-149">OUTPUTS</span></span>

### <span data-ttu-id="0afe6-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0afe6-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="0afe6-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0afe6-151">NOTES</span></span>

## <span data-ttu-id="0afe6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0afe6-152">RELATED LINKS</span></span>

[<span data-ttu-id="0afe6-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0afe6-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="0afe6-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0afe6-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="0afe6-155">Desfazer-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="0afe6-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

