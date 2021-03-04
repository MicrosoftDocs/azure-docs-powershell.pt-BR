---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: b95f47de7fbdcf6b5ed7892cb8deb8656559da27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890395"
---
# <span data-ttu-id="a25d9-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a25d9-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a25d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a25d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a25d9-103">Define uma definição de Assinatura de Acesso Compartilhado (SAS) com o Key Vault para uma determinada Conta de Armazenamento gerenciada do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a25d9-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a25d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a25d9-104">SYNTAX</span></span>

### <span data-ttu-id="a25d9-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a25d9-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a25d9-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a25d9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a25d9-107">DESCRIPTION</span></span>
<span data-ttu-id="a25d9-108">Define uma definição SAS (Assinatura de Acesso Compartilhado) com uma determinada Conta de Armazenamento gerenciada do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a25d9-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="a25d9-109">Isso também define um segredo que pode ser usado para obter o token SAS de acordo com essa definição do SAS.</span><span class="sxs-lookup"><span data-stu-id="a25d9-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="a25d9-110">O token SAS é gerado usando esses parâmetros e a chave ativa da Conta de Armazenamento gerenciada do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a25d9-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a25d9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a25d9-111">EXAMPLES</span></span>

### <span data-ttu-id="a25d9-112">Exemplo 1: definir uma definição SAS de tipo de conta e obter um token SAS atual com base nele</span><span class="sxs-lookup"><span data-stu-id="a25d9-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="a25d9-113">Define uma definição de SAS de conta 'accountsas' em uma conta de armazenamento gerenciada por KeyVault 'mysa' no cofre 'mykv'.</span><span class="sxs-lookup"><span data-stu-id="a25d9-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="a25d9-114">Especificamente, a sequência acima executa o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a25d9-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="a25d9-115">obtém uma conta de armazenamento (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="a25d9-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="a25d9-116">obtém um cofre de chaves (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="a25d9-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="a25d9-117">adiciona uma conta de armazenamento gerenciada por KeyVault ao cofre, definindo Key1 como a chave ativa e com um período de regeneração de 180 dias</span><span class="sxs-lookup"><span data-stu-id="a25d9-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="a25d9-118">define um contexto de armazenamento para a conta de armazenamento especificada, com Key1</span><span class="sxs-lookup"><span data-stu-id="a25d9-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="a25d9-119">cria um token SAS de conta para serviços Blob, File, Table and Queue, para tipos de recursos Serviço, Contêiner e Objeto, com todas as permissões, sobre https e com as datas de início e término especificadas</span><span class="sxs-lookup"><span data-stu-id="a25d9-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="a25d9-120">define uma definição de SAS de armazenamento gerenciado por KeyVault no cofre, com o uri do modelo como o token SAS criado acima, do tipo SAS 'account' e válido por 30 dias</span><span class="sxs-lookup"><span data-stu-id="a25d9-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="a25d9-121">recupera o token de acesso real do segredo KeyVault correspondente à definição do SAS</span><span class="sxs-lookup"><span data-stu-id="a25d9-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="a25d9-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a25d9-122">PARAMETERS</span></span>

### <span data-ttu-id="a25d9-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a25d9-123">-AccountName</span></span>
<span data-ttu-id="a25d9-124">Nome da conta de armazenamento gerenciado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="a25d9-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="a25d9-125">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento envelhecido.</span><span class="sxs-lookup"><span data-stu-id="a25d9-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25d9-126">-DefaultProfile</span></span>
<span data-ttu-id="a25d9-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a25d9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a25d9-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="a25d9-128">-Disable</span></span>
<span data-ttu-id="a25d9-129">Desabilita o uso da definição sas para geração de token sas.</span><span class="sxs-lookup"><span data-stu-id="a25d9-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="a25d9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a25d9-130">-InputObject</span></span>
<span data-ttu-id="a25d9-131">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a25d9-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a25d9-132">-Name</span></span>
<span data-ttu-id="a25d9-133">Nome da definição de sas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a25d9-133">Storage sas definition name.</span></span> <span data-ttu-id="a25d9-134">O cmdlet constrói o FQDN de uma definição de sas de armazenamento a partir do nome do cofre, do ambiente selecionado no momento, do nome da conta de armazenamento e do nome da definição de sas.</span><span class="sxs-lookup"><span data-stu-id="a25d9-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="a25d9-135">-SasType</span></span>
<span data-ttu-id="a25d9-136">Tipo SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a25d9-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a25d9-137">-Tag</span></span>
<span data-ttu-id="a25d9-138">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a25d9-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a25d9-139">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a25d9-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a25d9-140">-TemplateUri</span></span>
<span data-ttu-id="a25d9-141">Uri do modelo de definição do SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a25d9-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="a25d9-142">-ValidityPeriod</span></span>
<span data-ttu-id="a25d9-143">Período de validade que será usado para definir o tempo de expiração do token sas a partir do momento em que ele for gerado</span><span class="sxs-lookup"><span data-stu-id="a25d9-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a25d9-144">-VaultName</span></span>
<span data-ttu-id="a25d9-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="a25d9-145">Vault name.</span></span>
<span data-ttu-id="a25d9-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="a25d9-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a25d9-147">-Confirm</span></span>
<span data-ttu-id="a25d9-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25d9-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25d9-149">-WhatIf</span></span>
<span data-ttu-id="a25d9-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a25d9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a25d9-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a25d9-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25d9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25d9-152">CommonParameters</span></span>
<span data-ttu-id="a25d9-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25d9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25d9-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a25d9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25d9-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a25d9-155">INPUTS</span></span>

### <span data-ttu-id="a25d9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a25d9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="a25d9-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a25d9-157">OUTPUTS</span></span>

### <span data-ttu-id="a25d9-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a25d9-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a25d9-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="a25d9-159">NOTES</span></span>

## <span data-ttu-id="a25d9-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a25d9-160">RELATED LINKS</span></span>

[<span data-ttu-id="a25d9-161">Azureâ€,RM.â€'Keyâ€.Vault</span><span class="sxs-lookup"><span data-stu-id="a25d9-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
