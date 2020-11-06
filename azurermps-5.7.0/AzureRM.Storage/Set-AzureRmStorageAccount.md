---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428691"
---
# <span data-ttu-id="26b94-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26b94-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="26b94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26b94-102">SYNOPSIS</span></span>
<span data-ttu-id="26b94-103">Modifica uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26b94-104">SYNTAX</span></span>

### <span data-ttu-id="26b94-105">StorageEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="26b94-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26b94-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="26b94-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b94-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26b94-107">DESCRIPTION</span></span>
<span data-ttu-id="26b94-108">O cmdlet **set-AzureRmStorageAccount** modifica uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="26b94-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="26b94-109">Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio de cliente ou definir marcas em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="26b94-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26b94-110">EXAMPLES</span></span>

### <span data-ttu-id="26b94-111">Exemplo 1: definir o tipo de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b94-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="26b94-112">Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="26b94-113">Exemplo 2: definir um domínio personalizado para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b94-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="26b94-114">Este comando define um domínio personalizado para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="26b94-115">Exemplo 3: habilitar a criptografia em BLOB e em serviços de arquivo</span><span class="sxs-lookup"><span data-stu-id="26b94-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="26b94-116">Esse comando habilita a criptografia do serviço de armazenamento em BLOB e arquivo para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="26b94-117">Exemplo 4: definir o valor da camada de acesso</span><span class="sxs-lookup"><span data-stu-id="26b94-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="26b94-118">O comando define o valor da camada de acesso como legal.</span><span class="sxs-lookup"><span data-stu-id="26b94-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="26b94-119">Exemplo 4: definir o domínio e as marcas personalizadas</span><span class="sxs-lookup"><span data-stu-id="26b94-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="26b94-120">O comando define o valor da camada de acesso como legal.</span><span class="sxs-lookup"><span data-stu-id="26b94-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="26b94-121">Exemplo 5: habilitar a criptografia em serviços de blob com o keyvault</span><span class="sxs-lookup"><span data-stu-id="26b94-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="26b94-122">Esse comando habilita a criptografia do serviço de armazenamento no blob com um novo cofre de conteúdo criado.</span><span class="sxs-lookup"><span data-stu-id="26b94-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="26b94-123">Exemplo 6: desabilitar a criptografia em serviços de arquivo com a fonte definida como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="26b94-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="26b94-124">Este comando desabilita a criptografia em serviços de arquivo com a fonte definida como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="26b94-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="26b94-125">OS</span><span class="sxs-lookup"><span data-stu-id="26b94-125">PARAMETERS</span></span>

### <span data-ttu-id="26b94-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="26b94-126">-AccessTier</span></span>
<span data-ttu-id="26b94-127">Especifica a camada de acesso da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="26b94-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="26b94-128">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="26b94-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="26b94-129">Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="26b94-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="26b94-130">Para obter mais informações, consulte armazenamento de blob do Azure: camadas de armazenamento incríveis e quentes https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="26b94-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="26b94-131">Se o tipo de conta de armazenamento for armazenamento, não especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="26b94-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="26b94-132">-AssignIdentity</span></span>
<span data-ttu-id="26b94-133">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="26b94-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="26b94-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="26b94-134">-CustomDomainName</span></span>
<span data-ttu-id="26b94-135">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="26b94-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="26b94-136">-DisableEncryptionService</span></span>
<span data-ttu-id="26b94-137">Indica se esse cmdlet desabilita a criptografia do serviço de armazenamento no serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="26b94-138">O Azure Blob e o Azure File Services são suportados.</span><span class="sxs-lookup"><span data-stu-id="26b94-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="26b94-139">-EnableEncryptionService</span></span>
<span data-ttu-id="26b94-140">Indica se esse cmdlet habilita a criptografia do serviço de armazenamento no serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="26b94-141">O Azure Blob e o Azure File Services são suportados.</span><span class="sxs-lookup"><span data-stu-id="26b94-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="26b94-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="26b94-143">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="26b94-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-144">-Force</span><span class="sxs-lookup"><span data-stu-id="26b94-144">-Force</span></span>
<span data-ttu-id="26b94-145">Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="26b94-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="26b94-146">Para obter mais informações, consulte armazenamento de blob do Azure: camadas de armazenamento incríveis e quentes https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="26b94-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="26b94-147">Se o tipo de conta de armazenamento for armazenamento, não especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="26b94-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="26b94-148">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="26b94-148">-InformationAction</span></span>
<span data-ttu-id="26b94-149">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="26b94-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="26b94-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="26b94-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26b94-151">Contínuo</span><span class="sxs-lookup"><span data-stu-id="26b94-151">Continue</span></span>
- <span data-ttu-id="26b94-152">Ignorar</span><span class="sxs-lookup"><span data-stu-id="26b94-152">Ignore</span></span>
- <span data-ttu-id="26b94-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="26b94-153">Inquire</span></span>
- <span data-ttu-id="26b94-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="26b94-154">SilentlyContinue</span></span>
- <span data-ttu-id="26b94-155">Finaliza</span><span class="sxs-lookup"><span data-stu-id="26b94-155">Stop</span></span>
- <span data-ttu-id="26b94-156">Suspensão</span><span class="sxs-lookup"><span data-stu-id="26b94-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="26b94-157">-InformationVariable</span></span>
<span data-ttu-id="26b94-158">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="26b94-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-159">-KeyName</span><span class="sxs-lookup"><span data-stu-id="26b94-159">-KeyName</span></span>
<span data-ttu-id="26b94-160">KeyName de repositório de fontes de criptografia de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b94-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="26b94-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="26b94-162">Define se deseja definir a fonte de fonte de criptografia da conta de armazenamento como Microsoft. keyvault ou não.</span><span class="sxs-lookup"><span data-stu-id="26b94-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span>
<span data-ttu-id="26b94-163">Se você especificar KeyName, keyversion e KeyvaultUri, a fonte de criptografia da conta de armazenamento também será definida como Microsoft. Weather Weather esse parâmetro está definido ou não.</span><span class="sxs-lookup"><span data-stu-id="26b94-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="26b94-164">-KeyVaultUri</span></span>
<span data-ttu-id="26b94-165">KeyVaultUri da fonte de armazenamento de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b94-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-166">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="26b94-166">-KeyVersion</span></span>
<span data-ttu-id="26b94-167">Compartilhamento de conta de armazenamento da fonte de repositório de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="26b94-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="26b94-168">-Name</span></span>
<span data-ttu-id="26b94-169">Especifica o nome da conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="26b94-169">Specifies the name of the Storage account to Modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b94-170">-ResourceGroupName</span></span>
<span data-ttu-id="26b94-171">Especifica o nome do grupo de recursos no qual a conta de armazenamento será modificada.</span><span class="sxs-lookup"><span data-stu-id="26b94-171">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="26b94-172">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26b94-172">-SkuName</span></span>
<span data-ttu-id="26b94-173">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26b94-173">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="26b94-174">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="26b94-174">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26b94-175">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-175">Standard_LRS.</span></span>
<span data-ttu-id="26b94-176">Armazenamento redundante localmente.</span><span class="sxs-lookup"><span data-stu-id="26b94-176">Locally-redundant storage.</span></span>
- <span data-ttu-id="26b94-177">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-177">Standard_ZRS.</span></span>
<span data-ttu-id="26b94-178">Armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="26b94-178">Zone-redundant storage.</span></span>
- <span data-ttu-id="26b94-179">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-179">Standard_GRS.</span></span>
<span data-ttu-id="26b94-180">Armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="26b94-180">Geo-redundant storage.</span></span>
- <span data-ttu-id="26b94-181">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-181">Standard_RAGRS.</span></span>
<span data-ttu-id="26b94-182">Acesso de leitura com armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="26b94-182">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="26b94-183">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-183">Premium_LRS.</span></span>
<span data-ttu-id="26b94-184">Premium-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="26b94-184">Premium locally-redundant storage.</span></span>

<span data-ttu-id="26b94-185">Você não pode alterar tipos de Standard_ZRS e Premium_LRS para outros tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="26b94-185">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="26b94-186">Você não pode alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="26b94-186">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-187">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="26b94-187">-StorageEncryption</span></span>
<span data-ttu-id="26b94-188">Define se deseja definir a fonte de criptografia da conta de armazenamento como Microsoft. Storage ou não.</span><span class="sxs-lookup"><span data-stu-id="26b94-188">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-189">-Marca</span><span class="sxs-lookup"><span data-stu-id="26b94-189">-Tag</span></span>
<span data-ttu-id="26b94-190">Se você especificar um valor de BlobStorage para o parâmetro *Kind* do cmdlet New-AzureRmStorageAccount, você deve especificar um valor para o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="26b94-190">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="26b94-191">Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="26b94-191">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="26b94-192">-UseSubDomain</span></span>
<span data-ttu-id="26b94-193">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="26b94-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b94-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26b94-194">-Confirm</span></span>
<span data-ttu-id="26b94-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b94-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b94-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b94-196">-WhatIf</span></span>
<span data-ttu-id="26b94-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26b94-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b94-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26b94-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b94-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b94-199">CommonParameters</span></span>
<span data-ttu-id="26b94-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b94-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b94-201">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b94-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b94-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26b94-202">INPUTS</span></span>

### <span data-ttu-id="26b94-203">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="26b94-203">None</span></span>
<span data-ttu-id="26b94-204">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="26b94-204">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26b94-205">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26b94-205">OUTPUTS</span></span>

## <span data-ttu-id="26b94-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26b94-206">NOTES</span></span>

## <span data-ttu-id="26b94-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26b94-207">RELATED LINKS</span></span>

[<span data-ttu-id="26b94-208">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26b94-208">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="26b94-209">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26b94-209">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="26b94-210">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26b94-210">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
