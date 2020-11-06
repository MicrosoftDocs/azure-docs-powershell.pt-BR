---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428914"
---
# Add-AzureKeyVaultManagedStorageAccount

## Sinopse
Adiciona uma conta de armazenamento do Azure existente ao cofre de chaves especificado para que as chaves sejam gerenciadas pelo serviço do cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Configura uma conta de armazenamento existente do Azure com o Key Vault para que as chaves de conta de armazenamento sejam gerenciadas pelo cofre de chaves. A conta de armazenamento já deve existir. As teclas de armazenamento nunca são expostas ao chamador.
O Key Vault automaticamente regenera e alterna a chave ativa com base no período de regeneração.

## EXEMPLOS

### Exemplo 1: definir uma conta de armazenamento do Azure com o cofre de chaves para gerenciar as chaves
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Define uma conta de armazenamento com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves. O conjunto de teclas ativas é ' key1 '. Essa chave será usada para gerar tokens SAS. O cofre de chaves regenerará a chave "Key2" após o período de regeneração no momento do comando e a definirá como a chave ativa. Esse processo de regeneração automática continuará entre ' key1 ' e ' Key2 ' com um intervalo de 90 dias.

### Exemplo 2: definir uma conta de armazenamento clássica do Azure com o cofre de chaves para gerenciar as chaves
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Define uma conta de armazenamento clássica com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves. O conjunto de teclas ativas é ' Primary '. Essa chave será usada para gerar tokens SAS. O cofre de chaves reproduzirá a tecla ' secundária ' após o período de regeneração da hora do comando e a definirá como a chave ativa. Esse processo de regeneração automática continuará entre ' principal ' e ' secundário ', com um intervalo de 90 a dias.

## OS

### -AccountName
Nome da conta de armazenamento gerenciado do cofre de chaves. O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
ID do recurso do Azure da conta de armazenamento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Nome da chave da conta de armazenamento que deve ser usada para gerar tokens SAS.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Disable
Desabilita o uso da chave da conta de armazenamento gerenciado para a geração de tokens SAS.

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

### -DisableAutoRegenerateKey
Regenerar chave automaticamente. Se verdadeiro, a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a nova chave ativa após o período de regeneração. Se falso, as chaves da conta de armazenamento gerenciado não serão regeneradas automaticamente.

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

### -RegenerationPeriod
Período de regeneração. Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será regenerada automaticamente e se tornará a nova chave ativa.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

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

### -Cofrename
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount

## INFORMA

## LINKS RELACIONADOS

[AzureRM. keyvault](/powershell/module/azurerm.keyvault)
