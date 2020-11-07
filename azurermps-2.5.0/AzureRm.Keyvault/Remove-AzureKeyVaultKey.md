---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 911ea06fdfa9d4d90f8c9935e3e98c026c70cce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785215"
---
# <span data-ttu-id="fc645-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc645-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="fc645-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc645-102">SYNOPSIS</span></span>
<span data-ttu-id="fc645-103">Exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fc645-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc645-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc645-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc645-105">DESCRIPTION</span></span>
<span data-ttu-id="fc645-106">O cmdlet Remove-AzureKeyVaultKey exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fc645-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="fc645-107">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzureKeyVaultKeyRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="fc645-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="fc645-108">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="fc645-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="fc645-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc645-109">EXAMPLES</span></span>

### <span data-ttu-id="fc645-110">Exemplo 1: remover uma chave de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fc645-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="fc645-111">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="fc645-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="fc645-112">Exemplo 2: remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="fc645-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="fc645-113">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="fc645-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="fc645-114">O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fc645-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fc645-115">Exemplo 3: limpar uma chave excluída do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="fc645-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="fc645-116">Esse comando Remove a chave denominada ITSoftware do cofre de chaves chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="fc645-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="fc645-117">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fc645-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="fc645-118">Exemplo 4: remover chaves usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="fc645-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="fc645-119">Esse comando obtém todas as chaves no cofre de chaves chamado contoso e passa-as para o cmdlet **WHERE do objeto** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc645-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fc645-120">Esse cmdlet passa as chaves que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="fc645-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="fc645-121">Esse cmdlet Remove essas chaves.</span><span class="sxs-lookup"><span data-stu-id="fc645-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="fc645-122">OS</span><span class="sxs-lookup"><span data-stu-id="fc645-122">PARAMETERS</span></span>

### <span data-ttu-id="fc645-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc645-123">-DefaultProfile</span></span>
<span data-ttu-id="fc645-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc645-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc645-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fc645-125">-Force</span></span>
<span data-ttu-id="fc645-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc645-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc645-127">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="fc645-127">-InRemovedState</span></span>
<span data-ttu-id="fc645-128">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fc645-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="fc645-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc645-129">-Name</span></span>
<span data-ttu-id="fc645-130">Especifica o nome da chave a ser removida.</span><span class="sxs-lookup"><span data-stu-id="fc645-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="fc645-131">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="fc645-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc645-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc645-132">-PassThru</span></span>
<span data-ttu-id="fc645-133">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. keybundle** .</span><span class="sxs-lookup"><span data-stu-id="fc645-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="fc645-134">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fc645-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc645-135">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fc645-135">-VaultName</span></span>
<span data-ttu-id="fc645-136">Especifica o nome do cofre de chaves do qual a chave será removida.</span><span class="sxs-lookup"><span data-stu-id="fc645-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="fc645-137">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="fc645-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="fc645-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc645-138">-Confirm</span></span>
<span data-ttu-id="fc645-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc645-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc645-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc645-140">-WhatIf</span></span>
<span data-ttu-id="fc645-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc645-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc645-142">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc645-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc645-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc645-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc645-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc645-144">CommonParameters</span></span>
<span data-ttu-id="fc645-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc645-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc645-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc645-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc645-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc645-147">INPUTS</span></span>

### <span data-ttu-id="fc645-148">String</span><span class="sxs-lookup"><span data-stu-id="fc645-148">String</span></span>

## <span data-ttu-id="fc645-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc645-149">OUTPUTS</span></span>

### <span data-ttu-id="fc645-150">Microsoft. Azure. Commands. keyvault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="fc645-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="fc645-151">Esse cmdlet retornará um valor apenas se você especificar o parâmetro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="fc645-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="fc645-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc645-152">NOTES</span></span>

## <span data-ttu-id="fc645-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc645-153">RELATED LINKS</span></span>

[<span data-ttu-id="fc645-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc645-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fc645-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc645-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fc645-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="fc645-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="fc645-157">Desfazer-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fc645-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

