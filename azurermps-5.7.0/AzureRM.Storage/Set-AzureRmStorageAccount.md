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
# Set-AzureRmStorageAccount

## Sinopse
Modifica uma conta de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### StorageEncryption (padrão)
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmStorageAccount** modifica uma conta de armazenamento do Azure.
Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio de cliente ou definir marcas em uma conta de armazenamento.

## EXEMPLOS

### Exemplo 1: definir o tipo de conta de armazenamento
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.

### Exemplo 2: definir um domínio personalizado para uma conta de armazenamento
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

Este comando define um domínio personalizado para uma conta de armazenamento.

### Exemplo 3: habilitar a criptografia em BLOB e em serviços de arquivo
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

Esse comando habilita a criptografia do serviço de armazenamento em BLOB e arquivo para uma conta de armazenamento.

### Exemplo 4: definir o valor da camada de acesso
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

O comando define o valor da camada de acesso como legal.

### Exemplo 4: definir o domínio e as marcas personalizadas
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

O comando define o valor da camada de acesso como legal.

### Exemplo 5: habilitar a criptografia em serviços de blob com o keyvault
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

Esse comando habilita a criptografia do serviço de armazenamento no blob com um novo cofre de conteúdo criado.

### Exemplo 6: desabilitar a criptografia em serviços de arquivo com a fonte definida como "Microsoft. Storage"
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

Este comando desabilita a criptografia em serviços de arquivo com a fonte definida como "Microsoft. Storage"

## OS

### -AccessTier
Especifica a camada de acesso da conta de armazenamento que esse cmdlet modifica.
Os valores aceitáveis para esse parâmetro são: quente e legal.

Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.
Para obter mais informações, consulte armazenamento de blob do Azure: camadas de armazenamento incríveis e quentes https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .
Se o tipo de conta de armazenamento for armazenamento, não especifique esse parâmetro.

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

### -AssignIdentity
Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.

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

### -CustomDomainName
Especifica o nome do domínio personalizado.

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

### -DisableEncryptionService
Indica se esse cmdlet desabilita a criptografia do serviço de armazenamento no serviço de armazenamento.
O Azure Blob e o Azure File Services são suportados.

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

### -EnableEncryptionService
Indica se esse cmdlet habilita a criptografia do serviço de armazenamento no serviço de armazenamento.
O Azure Blob e o Azure File Services são suportados.

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

### -EnableHttpsTrafficOnly
Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.

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

### -Force
Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.
Para obter mais informações, consulte armazenamento de blob do Azure: camadas de armazenamento incríveis e quentes https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .
Se o tipo de conta de armazenamento for armazenamento, não especifique esse parâmetro.

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

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

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

### -InformationVariable
Especifica uma variável de informações.

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

### -KeyName
KeyName de repositório de fontes de criptografia de conta de armazenamento

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

### -KeyvaultEncryption
Define se deseja definir a fonte de fonte de criptografia da conta de armazenamento como Microsoft. keyvault ou não.
Se você especificar KeyName, keyversion e KeyvaultUri, a fonte de criptografia da conta de armazenamento também será definida como Microsoft. Weather Weather esse parâmetro está definido ou não.
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

### -KeyVaultUri
KeyVaultUri da fonte de armazenamento de conta de armazenamento

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

### -Keyversion
Compartilhamento de conta de armazenamento da fonte de repositório de conta de armazenamento

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

### -Nome
Especifica o nome da conta de armazenamento a ser modificada.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual a conta de armazenamento será modificada.

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

### -SkuName
Especifica o nome do SKU da conta de armazenamento.
Os valores aceitáveis para esse parâmetro são:

- Standard_LRS.
Armazenamento redundante localmente.
- Standard_ZRS.
Armazenamento redundante na zona.
- Standard_GRS.
Armazenamento com redundância geográfica.
- Standard_RAGRS.
Acesso de leitura com armazenamento redundante geográfico.
- Premium_LRS.
Premium-armazenamento redundante local.

Você não pode alterar tipos de Standard_ZRS e Premium_LRS para outros tipos de conta.
Você não pode alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.

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

### -StorageEncryption
Define se deseja definir a fonte de criptografia da conta de armazenamento como Microsoft. Storage ou não.

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

### -Marca
Se você especificar um valor de BlobStorage para o parâmetro *Kind* do cmdlet New-AzureRmStorageAccount, você deve especificar um valor para o parâmetro *AccessTier* .

Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .

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

### -UseSubDomain
Indica se a validação de CName indireto deve ser habilitada.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[New-AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)
