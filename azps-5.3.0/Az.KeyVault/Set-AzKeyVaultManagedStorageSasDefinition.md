---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429229"
---
# <span data-ttu-id="b3848-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b3848-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b3848-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3848-102">SYNOPSIS</span></span>
<span data-ttu-id="b3848-103">Define uma definição de assinatura de acesso compartilhado (SAS) com o cofre de chaves para uma determinada conta de armazenamento do Azure, gerenciada pela chave.</span><span class="sxs-lookup"><span data-stu-id="b3848-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="b3848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3848-104">SYNTAX</span></span>

### <span data-ttu-id="b3848-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3848-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3848-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3848-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3848-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3848-107">DESCRIPTION</span></span>
<span data-ttu-id="b3848-108">Define uma definição de assinatura de acesso compartilhado (SAS) com uma determinada conta de armazenamento do Azure do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b3848-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="b3848-109">Isso também define um segredo que pode ser usado para obter o token SAS por essa definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="b3848-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="b3848-110">O token SAS é gerado usando esses parâmetros e a chave ativa da conta de armazenamento gerenciada do cofre do repositório de chaves.</span><span class="sxs-lookup"><span data-stu-id="b3848-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="b3848-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3848-111">EXAMPLES</span></span>

### <span data-ttu-id="b3848-112">Exemplo 1: definir uma definição de tipo de conta SAS e obter um token SAS atual baseado nela</span><span class="sxs-lookup"><span data-stu-id="b3848-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="b3848-113">Define uma definição de SAS de conta ' contasas ' em um keyvault-conta de armazenamento gerenciado ' Mysa ' no cofre ' mykv '.</span><span class="sxs-lookup"><span data-stu-id="b3848-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="b3848-114">Especificamente, a sequência acima executa o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3848-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="b3848-115">Obtém uma conta de armazenamento (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="b3848-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="b3848-116">Obtém um cofre de chaves (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="b3848-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="b3848-117">Adiciona uma conta de armazenamento gerenciada do keyvault ao cofre, definindo key1 como a chave ativa e com um período de regeneração de 180 dias</span><span class="sxs-lookup"><span data-stu-id="b3848-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="b3848-118">define um contexto de armazenamento para a conta de armazenamento especificada, com a key1</span><span class="sxs-lookup"><span data-stu-id="b3848-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="b3848-119">Cria um token SAS de conta para blob de serviços, arquivo, tabela e fila, para o serviço de tipos de recursos, contêiner e objeto, com todas as permissões, via HTTPS e com as datas de início e término especificadas</span><span class="sxs-lookup"><span data-stu-id="b3848-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="b3848-120">define uma definição de SAS de armazenamento gerenciado no cofre no cofre, com o URI de modelo como o token SAS criado acima, do tipo SAS ' conta ' e válido por 30 dias</span><span class="sxs-lookup"><span data-stu-id="b3848-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="b3848-121">Recupera o token de acesso real do segredo do keyvault correspondente à definição de SAS</span><span class="sxs-lookup"><span data-stu-id="b3848-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="b3848-122">OS</span><span class="sxs-lookup"><span data-stu-id="b3848-122">PARAMETERS</span></span>

### <span data-ttu-id="b3848-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3848-123">-AccountName</span></span>
<span data-ttu-id="b3848-124">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b3848-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="b3848-125">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b3848-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="b3848-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3848-126">-DefaultProfile</span></span>
<span data-ttu-id="b3848-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b3848-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3848-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="b3848-128">-Disable</span></span>
<span data-ttu-id="b3848-129">Desabilita o uso da definição de SAS para a geração de token SAS.</span><span class="sxs-lookup"><span data-stu-id="b3848-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="b3848-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3848-130">-InputObject</span></span>
<span data-ttu-id="b3848-131">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b3848-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="b3848-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3848-132">-Name</span></span>
<span data-ttu-id="b3848-133">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3848-133">Storage sas definition name.</span></span> <span data-ttu-id="b3848-134">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="b3848-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="b3848-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="b3848-135">-SasType</span></span>
<span data-ttu-id="b3848-136">Tipo de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3848-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="b3848-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="b3848-137">-Tag</span></span>
<span data-ttu-id="b3848-138">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b3848-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3848-139">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b3848-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b3848-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b3848-140">-TemplateUri</span></span>
<span data-ttu-id="b3848-141">URI do modelo de definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b3848-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="b3848-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="b3848-142">-ValidityPeriod</span></span>
<span data-ttu-id="b3848-143">Período de validade que será usado para definir o tempo de expiração do token SAS no momento da geração</span><span class="sxs-lookup"><span data-stu-id="b3848-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="b3848-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="b3848-144">-VaultName</span></span>
<span data-ttu-id="b3848-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="b3848-145">Vault name.</span></span>
<span data-ttu-id="b3848-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b3848-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b3848-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3848-147">-Confirm</span></span>
<span data-ttu-id="b3848-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3848-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3848-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3848-149">-WhatIf</span></span>
<span data-ttu-id="b3848-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3848-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3848-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3848-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3848-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3848-152">CommonParameters</span></span>
<span data-ttu-id="b3848-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3848-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3848-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3848-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3848-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3848-155">INPUTS</span></span>

### <span data-ttu-id="b3848-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b3848-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="b3848-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3848-157">OUTPUTS</span></span>

### <span data-ttu-id="b3848-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b3848-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b3848-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3848-159">NOTES</span></span>

## <span data-ttu-id="b3848-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3848-160">RELATED LINKS</span></span>

[<span data-ttu-id="b3848-161">Azureâ € ‹ RM. â € ‹ Keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="b3848-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
