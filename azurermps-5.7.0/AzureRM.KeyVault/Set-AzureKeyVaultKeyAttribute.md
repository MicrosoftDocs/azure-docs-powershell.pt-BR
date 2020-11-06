---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430457"
---
# <span data-ttu-id="08a3f-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="08a3f-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="08a3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="08a3f-103">Atualiza os atributos de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="08a3f-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08a3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08a3f-104">SYNTAX</span></span>

### <span data-ttu-id="08a3f-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="08a3f-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a3f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="08a3f-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a3f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08a3f-107">DESCRIPTION</span></span>
<span data-ttu-id="08a3f-108">O cmdlet **set-AzureKeyVaultKeyAttribute** atualiza os atributos editáveis de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="08a3f-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="08a3f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08a3f-109">EXAMPLES</span></span>

### <span data-ttu-id="08a3f-110">Exemplo 1: modificar uma chave para habilitá-la e definir a data de expiração e as marcas</span><span class="sxs-lookup"><span data-stu-id="08a3f-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="08a3f-111">O primeiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="08a3f-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="08a3f-112">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="08a3f-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="08a3f-113">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="08a3f-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="08a3f-114">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="08a3f-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="08a3f-115">O segundo comando cria uma variável para armazenar valores de marca de alta gravidade e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="08a3f-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="08a3f-116">O comando final modifica uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="08a3f-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="08a3f-117">O comando habilita a chave, define seu tempo de expiração para a hora armazenada em $Expires e define as marcas armazenadas no $Tags.</span><span class="sxs-lookup"><span data-stu-id="08a3f-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="08a3f-118">Exemplo 2: modificar uma tecla para excluir todas as marcas</span><span class="sxs-lookup"><span data-stu-id="08a3f-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="08a3f-119">Esses comandos excluem todas as marcas para uma versão específica de uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="08a3f-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="08a3f-120">OS</span><span class="sxs-lookup"><span data-stu-id="08a3f-120">PARAMETERS</span></span>

### <span data-ttu-id="08a3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a3f-121">-DefaultProfile</span></span>
<span data-ttu-id="08a3f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="08a3f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08a3f-123">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="08a3f-123">-Enable</span></span>
<span data-ttu-id="08a3f-124">Especifica se uma tecla deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="08a3f-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="08a3f-125">Um valor de $True habilita a tecla.</span><span class="sxs-lookup"><span data-stu-id="08a3f-125">A value of $True enables the key.</span></span> <span data-ttu-id="08a3f-126">Um valor de $False desabilita a chave.</span><span class="sxs-lookup"><span data-stu-id="08a3f-126">A value of $False disables the key.</span></span> <span data-ttu-id="08a3f-127">Se você não especificar esse parâmetro, esse cmdlet não modificará o status da chave.</span><span class="sxs-lookup"><span data-stu-id="08a3f-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="08a3f-128">-Expira em</span><span class="sxs-lookup"><span data-stu-id="08a3f-128">-Expires</span></span>
<span data-ttu-id="08a3f-129">Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="08a3f-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="08a3f-130">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="08a3f-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="08a3f-131">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="08a3f-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="08a3f-132">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="08a3f-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="08a3f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08a3f-133">-InputObject</span></span>
<span data-ttu-id="08a3f-134">Objeto-chave</span><span class="sxs-lookup"><span data-stu-id="08a3f-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08a3f-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="08a3f-135">-KeyOps</span></span>
<span data-ttu-id="08a3f-136">Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="08a3f-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="08a3f-137">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="08a3f-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="08a3f-138">Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela especificação de chave da Web JSON.</span><span class="sxs-lookup"><span data-stu-id="08a3f-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="08a3f-139">Esses valores (diferenciam maiúsculas de minúsculas) são:</span><span class="sxs-lookup"><span data-stu-id="08a3f-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="08a3f-140">com</span><span class="sxs-lookup"><span data-stu-id="08a3f-140">encrypt</span></span>
- <span data-ttu-id="08a3f-141">criptografá</span><span class="sxs-lookup"><span data-stu-id="08a3f-141">decrypt</span></span>
- <span data-ttu-id="08a3f-142">quebrada</span><span class="sxs-lookup"><span data-stu-id="08a3f-142">wrap</span></span>
- <span data-ttu-id="08a3f-143">desenvolva</span><span class="sxs-lookup"><span data-stu-id="08a3f-143">unwrap</span></span>
- <span data-ttu-id="08a3f-144">designa</span><span class="sxs-lookup"><span data-stu-id="08a3f-144">sign</span></span>
- <span data-ttu-id="08a3f-145">verificar</span><span class="sxs-lookup"><span data-stu-id="08a3f-145">verify</span></span>
- <span data-ttu-id="08a3f-146">fazer</span><span class="sxs-lookup"><span data-stu-id="08a3f-146">backup</span></span>
- <span data-ttu-id="08a3f-147">restaurar</span><span class="sxs-lookup"><span data-stu-id="08a3f-147">restore</span></span>

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

### <span data-ttu-id="08a3f-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="08a3f-148">-Name</span></span>
<span data-ttu-id="08a3f-149">Especifica o nome da chave a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="08a3f-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="08a3f-150">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="08a3f-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a3f-151">-Não antes</span><span class="sxs-lookup"><span data-stu-id="08a3f-151">-NotBefore</span></span>
<span data-ttu-id="08a3f-152">Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="08a3f-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="08a3f-153">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="08a3f-153">This parameter uses UTC.</span></span>
<span data-ttu-id="08a3f-154">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="08a3f-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="08a3f-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08a3f-155">-PassThru</span></span>
<span data-ttu-id="08a3f-156">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="08a3f-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08a3f-157">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="08a3f-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08a3f-158">-Marca</span><span class="sxs-lookup"><span data-stu-id="08a3f-158">-Tag</span></span>
<span data-ttu-id="08a3f-159">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="08a3f-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08a3f-160">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="08a3f-160">For example:</span></span>

<span data-ttu-id="08a3f-161">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="08a3f-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="08a3f-162">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="08a3f-162">-VaultName</span></span>
<span data-ttu-id="08a3f-163">Especifica o nome do cofre de chaves no qual esse cmdlet modifica a chave.</span><span class="sxs-lookup"><span data-stu-id="08a3f-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="08a3f-164">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="08a3f-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a3f-165">-Versão</span><span class="sxs-lookup"><span data-stu-id="08a3f-165">-Version</span></span>
<span data-ttu-id="08a3f-166">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="08a3f-166">Specifies the key version.</span></span>
<span data-ttu-id="08a3f-167">Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.</span><span class="sxs-lookup"><span data-stu-id="08a3f-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="08a3f-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08a3f-168">-Confirm</span></span>
<span data-ttu-id="08a3f-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a3f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a3f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a3f-170">-WhatIf</span></span>
<span data-ttu-id="08a3f-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08a3f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a3f-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08a3f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a3f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a3f-173">CommonParameters</span></span>
<span data-ttu-id="08a3f-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08a3f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a3f-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08a3f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a3f-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08a3f-176">INPUTS</span></span>

### <span data-ttu-id="08a3f-177">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="08a3f-177">None</span></span>
<span data-ttu-id="08a3f-178">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="08a3f-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08a3f-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08a3f-179">OUTPUTS</span></span>

### <span data-ttu-id="08a3f-180">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08a3f-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="08a3f-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08a3f-181">NOTES</span></span>

## <span data-ttu-id="08a3f-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08a3f-182">RELATED LINKS</span></span>

[<span data-ttu-id="08a3f-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08a3f-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="08a3f-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08a3f-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="08a3f-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08a3f-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
