---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429522"
---
# <span data-ttu-id="72083-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="72083-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="72083-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72083-102">SYNOPSIS</span></span>
<span data-ttu-id="72083-103">Define uma definição de assinatura de acesso compartilhado (SAS) com o cofre de chaves para uma determinada conta de armazenamento do Azure, gerenciada pela chave.</span><span class="sxs-lookup"><span data-stu-id="72083-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72083-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72083-104">SYNTAX</span></span>

### <span data-ttu-id="72083-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="72083-105">Default (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72083-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="72083-106">ByInputObject</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72083-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72083-107">DESCRIPTION</span></span>
<span data-ttu-id="72083-108">Define uma definição de assinatura de acesso compartilhado (SAS) com uma determinada conta de armazenamento do Azure do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="72083-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="72083-109">Isso também define um segredo que pode ser usado para obter o token SAS por essa definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="72083-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="72083-110">O token SAS é gerado usando esses parâmetros e a chave ativa da conta de armazenamento gerenciada do cofre do repositório de chaves.</span><span class="sxs-lookup"><span data-stu-id="72083-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="72083-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72083-111">EXAMPLES</span></span>

### <span data-ttu-id="72083-112">Exemplo 1: definir uma definição de tipo de conta SAS e obter um token SAS atual baseado nela</span><span class="sxs-lookup"><span data-stu-id="72083-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="72083-113">Define uma definição de SAS de conta ' contasas ' em um keyvault-conta de armazenamento gerenciado ' Mysa ' no cofre ' mykv '.</span><span class="sxs-lookup"><span data-stu-id="72083-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="72083-114">Especificamente, a sequência acima executa o seguinte:</span><span class="sxs-lookup"><span data-stu-id="72083-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="72083-115">Obtém uma conta de armazenamento (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="72083-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="72083-116">Obtém um cofre de chaves (pré-existente)</span><span class="sxs-lookup"><span data-stu-id="72083-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="72083-117">Adiciona uma conta de armazenamento gerenciada do keyvault ao cofre, definindo key1 como a chave ativa e com um período de regeneração de 180 dias</span><span class="sxs-lookup"><span data-stu-id="72083-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="72083-118">define um contexto de armazenamento para a conta de armazenamento especificada, com a key1</span><span class="sxs-lookup"><span data-stu-id="72083-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="72083-119">Cria um token SAS de conta para blob de serviços, arquivo, tabela e fila, para o serviço de tipos de recursos, contêiner e objeto, com todas as permissões, via HTTPS e com as datas de início e término especificadas</span><span class="sxs-lookup"><span data-stu-id="72083-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="72083-120">define uma definição de SAS de armazenamento gerenciado no cofre no cofre, com o URI de modelo como o token SAS criado acima, do tipo SAS ' conta ' e válido por 30 dias</span><span class="sxs-lookup"><span data-stu-id="72083-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="72083-121">Recupera o token de acesso real do segredo do keyvault correspondente à definição de SAS</span><span class="sxs-lookup"><span data-stu-id="72083-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="72083-122">OS</span><span class="sxs-lookup"><span data-stu-id="72083-122">PARAMETERS</span></span>

### <span data-ttu-id="72083-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72083-123">-AccountName</span></span>
<span data-ttu-id="72083-124">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="72083-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="72083-125">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="72083-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="72083-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72083-126">-DefaultProfile</span></span>
<span data-ttu-id="72083-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72083-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72083-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="72083-128">-Disable</span></span>
<span data-ttu-id="72083-129">Desabilita o uso da definição de SAS para a geração de token SAS.</span><span class="sxs-lookup"><span data-stu-id="72083-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="72083-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72083-130">-InputObject</span></span>
<span data-ttu-id="72083-131">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="72083-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="72083-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="72083-132">-Name</span></span>
<span data-ttu-id="72083-133">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="72083-133">Storage sas definition name.</span></span> <span data-ttu-id="72083-134">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="72083-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="72083-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="72083-135">-SasType</span></span>
<span data-ttu-id="72083-136">Tipo de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="72083-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="72083-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="72083-137">-Tag</span></span>
<span data-ttu-id="72083-138">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="72083-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72083-139">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="72083-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72083-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="72083-140">-TemplateUri</span></span>
<span data-ttu-id="72083-141">URI do modelo de definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="72083-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="72083-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="72083-142">-ValidityPeriod</span></span>
<span data-ttu-id="72083-143">Período de validade que será usado para definir o tempo de expiração do token SAS no momento da geração</span><span class="sxs-lookup"><span data-stu-id="72083-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="72083-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="72083-144">-VaultName</span></span>
<span data-ttu-id="72083-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="72083-145">Vault name.</span></span>
<span data-ttu-id="72083-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="72083-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="72083-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72083-147">-Confirm</span></span>
<span data-ttu-id="72083-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72083-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72083-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72083-149">-WhatIf</span></span>
<span data-ttu-id="72083-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72083-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72083-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72083-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72083-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72083-152">CommonParameters</span></span>
<span data-ttu-id="72083-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72083-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72083-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72083-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72083-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72083-155">INPUTS</span></span>

### <span data-ttu-id="72083-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72083-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="72083-157">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72083-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="72083-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72083-158">OUTPUTS</span></span>

### <span data-ttu-id="72083-159">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="72083-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="72083-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72083-160">NOTES</span></span>

## <span data-ttu-id="72083-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72083-161">RELATED LINKS</span></span>

[<span data-ttu-id="72083-162">Azureâ € ‹ RM. â € ‹ Keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="72083-162">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
