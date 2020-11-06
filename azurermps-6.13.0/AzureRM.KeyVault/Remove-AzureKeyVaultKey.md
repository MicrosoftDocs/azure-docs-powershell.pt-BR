---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: ff7e5a02899d806633e485f06f419a6f1f2082a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430914"
---
# <span data-ttu-id="97ddd-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97ddd-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="97ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="97ddd-103">Exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="97ddd-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97ddd-104">SYNTAX</span></span>

### <span data-ttu-id="97ddd-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="97ddd-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97ddd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97ddd-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97ddd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="97ddd-108">O cmdlet Remove-AzureKeyVaultKey exclui uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="97ddd-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="97ddd-109">Se a chave foi excluída acidentalmente, a chave pode ser recuperada usando Undo-AzureKeyVaultKeyRemoval por um usuário com permissões "recuperar" especiais.</span><span class="sxs-lookup"><span data-stu-id="97ddd-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="97ddd-110">Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="97ddd-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="97ddd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97ddd-111">EXAMPLES</span></span>

### <span data-ttu-id="97ddd-112">Exemplo 1: remover uma chave de um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="97ddd-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

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

<span data-ttu-id="97ddd-113">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="97ddd-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="97ddd-114">Exemplo 2: remover uma chave sem confirmação do usuário</span><span class="sxs-lookup"><span data-stu-id="97ddd-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="97ddd-115">Esse comando Remove a chave chamada ITSoftware do cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="97ddd-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="97ddd-116">O comando especifica o parâmetro *Force* e, portanto, o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="97ddd-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="97ddd-117">Exemplo 3: limpar uma chave excluída do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="97ddd-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="97ddd-118">Esse comando Remove a chave denominada ITSoftware do cofre de chaves chamado contoso permanentemente.</span><span class="sxs-lookup"><span data-stu-id="97ddd-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="97ddd-119">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="97ddd-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="97ddd-120">Exemplo 4: remover chaves usando o operador pipeline</span><span class="sxs-lookup"><span data-stu-id="97ddd-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="97ddd-121">Esse comando obtém todas as chaves no cofre de chaves chamado contoso e passa-as para o cmdlet **WHERE do objeto** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="97ddd-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="97ddd-122">Esse cmdlet passa as chaves que têm um valor de $False para o atributo **Enabled** para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="97ddd-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="97ddd-123">Esse cmdlet Remove essas chaves.</span><span class="sxs-lookup"><span data-stu-id="97ddd-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="97ddd-124">OS</span><span class="sxs-lookup"><span data-stu-id="97ddd-124">PARAMETERS</span></span>

### <span data-ttu-id="97ddd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ddd-125">-DefaultProfile</span></span>
<span data-ttu-id="97ddd-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="97ddd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97ddd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="97ddd-127">-Force</span></span>
<span data-ttu-id="97ddd-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="97ddd-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97ddd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ddd-129">-InputObject</span></span>
<span data-ttu-id="97ddd-130">Objeto keybundle</span><span class="sxs-lookup"><span data-stu-id="97ddd-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="97ddd-131">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="97ddd-131">-InRemovedState</span></span>
<span data-ttu-id="97ddd-132">Remova permanentemente a chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="97ddd-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="97ddd-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="97ddd-133">-Name</span></span>
<span data-ttu-id="97ddd-134">Especifica o nome da chave a ser removida.</span><span class="sxs-lookup"><span data-stu-id="97ddd-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="97ddd-135">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="97ddd-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="97ddd-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97ddd-136">-PassThru</span></span>
<span data-ttu-id="97ddd-137">Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="97ddd-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="97ddd-138">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="97ddd-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97ddd-139">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="97ddd-139">-VaultName</span></span>
<span data-ttu-id="97ddd-140">Especifica o nome do cofre de chaves do qual a chave será removida.</span><span class="sxs-lookup"><span data-stu-id="97ddd-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="97ddd-141">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="97ddd-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="97ddd-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97ddd-142">-Confirm</span></span>
<span data-ttu-id="97ddd-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ddd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ddd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ddd-144">-WhatIf</span></span>
<span data-ttu-id="97ddd-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97ddd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ddd-146">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97ddd-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ddd-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97ddd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97ddd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ddd-148">CommonParameters</span></span>
<span data-ttu-id="97ddd-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ddd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ddd-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ddd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ddd-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97ddd-151">INPUTS</span></span>

### <span data-ttu-id="97ddd-152">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="97ddd-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="97ddd-153">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97ddd-153">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="97ddd-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97ddd-154">OUTPUTS</span></span>

### <span data-ttu-id="97ddd-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97ddd-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="97ddd-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97ddd-156">NOTES</span></span>

## <span data-ttu-id="97ddd-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97ddd-157">RELATED LINKS</span></span>

[<span data-ttu-id="97ddd-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97ddd-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="97ddd-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="97ddd-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="97ddd-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="97ddd-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="97ddd-161">Desfazer-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="97ddd-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

