---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775769"
---
# <span data-ttu-id="63cb1-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="63cb1-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="63cb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="63cb1-103">Exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="63cb1-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="63cb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63cb1-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63cb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="63cb1-106">O cmdlet Remove-AzKeyVaultSecret exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="63cb1-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="63cb1-107">Se o segredo foi excluído acidentalmente, o segredo pode ser recuperado usando Undo-AzKeyVaultSecretRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="63cb1-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="63cb1-108">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="63cb1-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="63cb1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="63cb1-110">Exemplo 1: remover um segredo de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="63cb1-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="63cb1-111">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso. '</span><span class="sxs-lookup"><span data-stu-id="63cb1-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="63cb1-112">Exemplo 2: remover um segredo de um cofre de chaves sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="63cb1-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="63cb1-113">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="63cb1-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="63cb1-114">O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="63cb1-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="63cb1-115">Exemplo 3: limpar o segredo excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="63cb1-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="63cb1-116">Esse comando premove o segredo nomeado FinanceSecret do cofre da chave chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="63cb1-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="63cb1-117">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="63cb1-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="63cb1-118">OS</span><span class="sxs-lookup"><span data-stu-id="63cb1-118">PARAMETERS</span></span>

### <span data-ttu-id="63cb1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cb1-119">-DefaultProfile</span></span>
<span data-ttu-id="63cb1-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="63cb1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63cb1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="63cb1-121">-Force</span></span>
<span data-ttu-id="63cb1-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="63cb1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63cb1-123">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="63cb1-123">-InRemovedState</span></span>
<span data-ttu-id="63cb1-124">Se presente, remove o segredo anteriormente excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="63cb1-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="63cb1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="63cb1-125">-Name</span></span>
<span data-ttu-id="63cb1-126">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="63cb1-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="63cb1-127">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="63cb1-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cb1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63cb1-128">-PassThru</span></span>
<span data-ttu-id="63cb1-129">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="63cb1-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="63cb1-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="63cb1-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63cb1-131">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="63cb1-131">-VaultName</span></span>
<span data-ttu-id="63cb1-132">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="63cb1-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="63cb1-133">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="63cb1-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cb1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63cb1-134">-Confirm</span></span>
<span data-ttu-id="63cb1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63cb1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63cb1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cb1-136">-WhatIf</span></span>
<span data-ttu-id="63cb1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63cb1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63cb1-138">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63cb1-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63cb1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63cb1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63cb1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cb1-140">CommonParameters</span></span>
<span data-ttu-id="63cb1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cb1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cb1-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63cb1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cb1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63cb1-143">INPUTS</span></span>

### <span data-ttu-id="63cb1-144">String</span><span class="sxs-lookup"><span data-stu-id="63cb1-144">String</span></span>

## <span data-ttu-id="63cb1-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63cb1-145">OUTPUTS</span></span>

### <span data-ttu-id="63cb1-146">Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="63cb1-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="63cb1-147">Esse cmdlet retornará um valor apenas se você especificar o parâmetro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="63cb1-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="63cb1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63cb1-148">NOTES</span></span>

## <span data-ttu-id="63cb1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63cb1-149">RELATED LINKS</span></span>

[<span data-ttu-id="63cb1-150">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="63cb1-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="63cb1-151">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="63cb1-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="63cb1-152">Desfazer-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="63cb1-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

