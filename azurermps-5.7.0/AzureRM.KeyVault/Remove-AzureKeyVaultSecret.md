---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: a4b90f91c44fc54f60539c326a6b37caba868488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431672"
---
# <span data-ttu-id="fa405-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fa405-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="fa405-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa405-102">SYNOPSIS</span></span>
<span data-ttu-id="fa405-103">Exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fa405-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa405-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa405-104">SYNTAX</span></span>

### <span data-ttu-id="fa405-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa405-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa405-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa405-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa405-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa405-107">DESCRIPTION</span></span>
<span data-ttu-id="fa405-108">O cmdlet Remove-AzureKeyVaultSecret exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fa405-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="fa405-109">Se o segredo foi excluído acidentalmente, o segredo pode ser recuperado usando Undo-AzureKeyVaultSecretRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="fa405-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="fa405-110">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="fa405-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="fa405-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa405-111">EXAMPLES</span></span>

### <span data-ttu-id="fa405-112">Exemplo 1: remover um segredo de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fa405-112">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="fa405-113">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso. '</span><span class="sxs-lookup"><span data-stu-id="fa405-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="fa405-114">Exemplo 2: remover um segredo de um cofre de chaves sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="fa405-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="fa405-115">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="fa405-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="fa405-116">O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fa405-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fa405-117">Exemplo 3: limpar o segredo excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="fa405-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="fa405-118">Esse comando premove o segredo nomeado FinanceSecret do cofre da chave chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="fa405-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="fa405-119">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fa405-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="fa405-120">OS</span><span class="sxs-lookup"><span data-stu-id="fa405-120">PARAMETERS</span></span>

### <span data-ttu-id="fa405-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa405-121">-DefaultProfile</span></span>
<span data-ttu-id="fa405-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fa405-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa405-123">-Force</span></span>
<span data-ttu-id="fa405-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa405-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa405-125">-InputObject</span></span>
<span data-ttu-id="fa405-126">Objeto secreto do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fa405-126">Key Vault Secret Object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-127">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="fa405-127">-InRemovedState</span></span>
<span data-ttu-id="fa405-128">Se presente, remove o segredo anteriormente excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="fa405-128">If present, removes the previously deleted secret permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa405-129">-Name</span></span>
<span data-ttu-id="fa405-130">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="fa405-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="fa405-131">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="fa405-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa405-132">-PassThru</span></span>
<span data-ttu-id="fa405-133">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="fa405-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="fa405-134">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fa405-134">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-135">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fa405-135">-VaultName</span></span>
<span data-ttu-id="fa405-136">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="fa405-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="fa405-137">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="fa405-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa405-138">-Confirm</span></span>
<span data-ttu-id="fa405-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa405-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa405-140">-WhatIf</span></span>
<span data-ttu-id="fa405-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa405-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa405-142">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa405-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa405-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa405-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa405-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa405-144">CommonParameters</span></span>
<span data-ttu-id="fa405-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa405-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa405-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa405-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa405-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa405-147">INPUTS</span></span>

### <span data-ttu-id="fa405-148">String</span><span class="sxs-lookup"><span data-stu-id="fa405-148">String</span></span>

## <span data-ttu-id="fa405-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa405-149">OUTPUTS</span></span>

### <span data-ttu-id="fa405-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fa405-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>
<span data-ttu-id="fa405-151">Esse cmdlet retornará um valor apenas se você especificar o parâmetro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="fa405-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="fa405-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa405-152">NOTES</span></span>

## <span data-ttu-id="fa405-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa405-153">RELATED LINKS</span></span>

[<span data-ttu-id="fa405-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fa405-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="fa405-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fa405-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="fa405-156">Desfazer-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="fa405-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

