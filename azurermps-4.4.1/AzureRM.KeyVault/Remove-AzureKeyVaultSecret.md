---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439932"
---
# <span data-ttu-id="0b0db-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0b0db-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="0b0db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b0db-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0db-103">Exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0b0db-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b0db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b0db-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b0db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b0db-105">DESCRIPTION</span></span>
<span data-ttu-id="0b0db-106">O cmdlet Remove-AzureKeyVaultSecret exclui um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0b0db-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="0b0db-107">Se o segredo foi excluído acidentalmente, o segredo pode ser recuperado usando Undo-AzureKeyVaultSecretRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="0b0db-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="0b0db-108">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="0b0db-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="0b0db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b0db-109">EXAMPLES</span></span>

### <span data-ttu-id="0b0db-110">Exemplo 1: remover um segredo de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="0b0db-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="0b0db-111">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso. '</span><span class="sxs-lookup"><span data-stu-id="0b0db-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="0b0db-112">Exemplo 2: remover um segredo de um cofre de chaves sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="0b0db-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="0b0db-113">Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="0b0db-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="0b0db-114">O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="0b0db-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="0b0db-115">Exemplo 3: limpar o segredo excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="0b0db-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="0b0db-116">Esse comando premove o segredo nomeado FinanceSecret do cofre da chave chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="0b0db-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="0b0db-117">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0b0db-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="0b0db-118">OS</span><span class="sxs-lookup"><span data-stu-id="0b0db-118">PARAMETERS</span></span>

### <span data-ttu-id="0b0db-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0b0db-119">-Force</span></span>
<span data-ttu-id="0b0db-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b0db-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b0db-121">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="0b0db-121">-InRemovedState</span></span>
<span data-ttu-id="0b0db-122">Se presente, remove o segredo anteriormente excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="0b0db-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="0b0db-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b0db-123">-Name</span></span>
<span data-ttu-id="0b0db-124">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="0b0db-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="0b0db-125">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="0b0db-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0db-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b0db-126">-PassThru</span></span>
<span data-ttu-id="0b0db-127">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="0b0db-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="0b0db-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0b0db-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b0db-129">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0b0db-129">-VaultName</span></span>
<span data-ttu-id="0b0db-130">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="0b0db-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="0b0db-131">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="0b0db-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b0db-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b0db-132">-Confirm</span></span>
<span data-ttu-id="0b0db-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b0db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0db-134">-WhatIf</span></span>
<span data-ttu-id="0b0db-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b0db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0db-136">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b0db-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0db-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b0db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0db-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0db-138">-DefaultProfile</span></span>
<span data-ttu-id="0b0db-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b0db-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0db-140">CommonParameters</span></span>
<span data-ttu-id="0b0db-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0db-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b0db-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0db-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b0db-143">INPUTS</span></span>

### <span data-ttu-id="0b0db-144">String</span><span class="sxs-lookup"><span data-stu-id="0b0db-144">String</span></span>

## <span data-ttu-id="0b0db-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b0db-145">OUTPUTS</span></span>

### <span data-ttu-id="0b0db-146">Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="0b0db-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="0b0db-147">Esse cmdlet retornará um valor apenas se você especificar o parâmetro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="0b0db-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="0b0db-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b0db-148">NOTES</span></span>

## <span data-ttu-id="0b0db-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b0db-149">RELATED LINKS</span></span>

[<span data-ttu-id="0b0db-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0b0db-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="0b0db-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0b0db-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="0b0db-152">Desfazer-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="0b0db-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

