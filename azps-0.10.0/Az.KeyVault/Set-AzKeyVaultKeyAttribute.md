---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776648"
---
# <span data-ttu-id="d512c-101">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d512c-101">Set-AzKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="d512c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d512c-102">SYNOPSIS</span></span>
<span data-ttu-id="d512c-103">Atualiza os atributos de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d512c-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="d512c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d512c-104">SYNTAX</span></span>

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d512c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d512c-105">DESCRIPTION</span></span>
<span data-ttu-id="d512c-106">O cmdlet **set-AzKeyVaultKeyAttribute** atualiza os atributos editáveis de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d512c-106">The **Set-AzKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="d512c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d512c-107">EXAMPLES</span></span>

### <span data-ttu-id="d512c-108">Exemplo 1: modificar uma chave para habilitá-la e definir a data de expiração e as marcas</span><span class="sxs-lookup"><span data-stu-id="d512c-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="d512c-109">O primeiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="d512c-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="d512c-110">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="d512c-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="d512c-111">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="d512c-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="d512c-112">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d512c-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="d512c-113">O segundo comando cria uma variável para armazenar valores de marca de alta gravidade e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="d512c-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="d512c-114">O comando final modifica uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="d512c-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="d512c-115">O comando habilita a chave, define seu tempo de expiração para a hora armazenada em $Expires e define as marcas armazenadas no $Tags.</span><span class="sxs-lookup"><span data-stu-id="d512c-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="d512c-116">Exemplo 2: modificar uma tecla para excluir todas as marcas</span><span class="sxs-lookup"><span data-stu-id="d512c-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="d512c-117">Esses comandos excluem todas as marcas para uma versão específica de uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="d512c-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="d512c-118">OS</span><span class="sxs-lookup"><span data-stu-id="d512c-118">PARAMETERS</span></span>

### <span data-ttu-id="d512c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d512c-119">-DefaultProfile</span></span>
<span data-ttu-id="d512c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d512c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d512c-121">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="d512c-121">-Enable</span></span>
<span data-ttu-id="d512c-122">Especifica se uma tecla deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d512c-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="d512c-123">Um valor de $True habilita a tecla.</span><span class="sxs-lookup"><span data-stu-id="d512c-123">A value of $True enables the key.</span></span> <span data-ttu-id="d512c-124">Um valor de $False desabilita a chave.</span><span class="sxs-lookup"><span data-stu-id="d512c-124">A value of $False disables the key.</span></span> <span data-ttu-id="d512c-125">Se você não especificar esse parâmetro, esse cmdlet não modificará o status da chave.</span><span class="sxs-lookup"><span data-stu-id="d512c-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-126">-Expira em</span><span class="sxs-lookup"><span data-stu-id="d512c-126">-Expires</span></span>
<span data-ttu-id="d512c-127">Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="d512c-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="d512c-128">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="d512c-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d512c-129">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="d512c-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="d512c-130">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d512c-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="d512c-131">-KeyOps</span></span>
<span data-ttu-id="d512c-132">Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="d512c-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="d512c-133">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d512c-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="d512c-134">Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela especificação de chave da Web JSON.</span><span class="sxs-lookup"><span data-stu-id="d512c-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="d512c-135">Esses valores (diferenciam maiúsculas de minúsculas) são:</span><span class="sxs-lookup"><span data-stu-id="d512c-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="d512c-136">com</span><span class="sxs-lookup"><span data-stu-id="d512c-136">encrypt</span></span>
- <span data-ttu-id="d512c-137">criptografá</span><span class="sxs-lookup"><span data-stu-id="d512c-137">decrypt</span></span>
- <span data-ttu-id="d512c-138">quebrada</span><span class="sxs-lookup"><span data-stu-id="d512c-138">wrap</span></span>
- <span data-ttu-id="d512c-139">desenvolva</span><span class="sxs-lookup"><span data-stu-id="d512c-139">unwrap</span></span>
- <span data-ttu-id="d512c-140">designa</span><span class="sxs-lookup"><span data-stu-id="d512c-140">sign</span></span>
- <span data-ttu-id="d512c-141">verificar</span><span class="sxs-lookup"><span data-stu-id="d512c-141">verify</span></span>
- <span data-ttu-id="d512c-142">fazer</span><span class="sxs-lookup"><span data-stu-id="d512c-142">backup</span></span>
- <span data-ttu-id="d512c-143">restaurar</span><span class="sxs-lookup"><span data-stu-id="d512c-143">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="d512c-144">-Name</span></span>
<span data-ttu-id="d512c-145">Especifica o nome da chave a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d512c-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="d512c-146">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d512c-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="d512c-147">-Não antes</span><span class="sxs-lookup"><span data-stu-id="d512c-147">-NotBefore</span></span>
<span data-ttu-id="d512c-148">Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="d512c-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="d512c-149">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="d512c-149">This parameter uses UTC.</span></span>
<span data-ttu-id="d512c-150">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="d512c-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d512c-151">-PassThru</span></span>
<span data-ttu-id="d512c-152">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d512c-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d512c-153">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d512c-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d512c-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="d512c-154">-Tag</span></span>
<span data-ttu-id="d512c-155">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d512c-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d512c-156">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d512c-156">For example:</span></span>

<span data-ttu-id="d512c-157">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d512c-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-158">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="d512c-158">-VaultName</span></span>
<span data-ttu-id="d512c-159">Especifica o nome do cofre de chaves no qual esse cmdlet modifica a chave.</span><span class="sxs-lookup"><span data-stu-id="d512c-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="d512c-160">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d512c-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d512c-161">-Versão</span><span class="sxs-lookup"><span data-stu-id="d512c-161">-Version</span></span>
<span data-ttu-id="d512c-162">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="d512c-162">Specifies the key version.</span></span>
<span data-ttu-id="d512c-163">Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.</span><span class="sxs-lookup"><span data-stu-id="d512c-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d512c-164">-Confirm</span></span>
<span data-ttu-id="d512c-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d512c-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d512c-166">-WhatIf</span></span>
<span data-ttu-id="d512c-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d512c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d512c-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d512c-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d512c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d512c-169">CommonParameters</span></span>
<span data-ttu-id="d512c-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d512c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d512c-171">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d512c-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d512c-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d512c-172">INPUTS</span></span>

### <span data-ttu-id="d512c-173">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d512c-173">None</span></span>
<span data-ttu-id="d512c-174">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d512c-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d512c-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d512c-175">OUTPUTS</span></span>

### <span data-ttu-id="d512c-176">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="d512c-176">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="d512c-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d512c-177">NOTES</span></span>

## <span data-ttu-id="d512c-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d512c-178">RELATED LINKS</span></span>

[<span data-ttu-id="d512c-179">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d512c-179">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d512c-180">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d512c-180">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="d512c-181">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d512c-181">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)