---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126150"
---
# Remove-AzKeyVaultManagedStorageAccount

## Sinopse
Remove uma conta de armazenamento gerenciada do Key Vault e todas as definições de SAS associadas.

## SYNTAX

### ByDefinitionName (padrão)
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
Desassocia uma conta de armazenamento do Azure do cofre de chaves. Isso não remove uma conta de armazenamento do Azure, mas remove as chaves da conta de serem gerenciadas pelo cofre de chave do Azure. Todas as definições de SAS de armazenamento gerenciado de Key Vault também são removidas.

## EXEMPLOS

### Exemplo 1: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves. A conta "mystorageaccount" não será removida. Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.

### Exemplo 2: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas sem confirmação do usuário.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves. A conta "mystorageaccount" não será removida. Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.

### Exemplo 3: excluir permanentemente (limpar) uma conta de armazenamento gerenciada do Azure e todas as definições de SAS associadas de um cofre habilitado para exclusão soft.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

O exemplo pressupõe que a exclusão suave está habilitada para este cofre. Verifique se esse é o caso examinando as propriedades do cofre ou o atributo RecoveryLevel de uma entidade no cofre.
O primeiro cmdlet desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves. A conta "mystorageaccount" não será removida. Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.
O segundo cmdlet verifica se a conta de armazenamento está em um estado excluído, mas recuperável. Alcançar esse Estado pode exigir algum tempo, aguarde ~ 30s antes de tentar.
O terceiro cmdlet remove permanentemente a conta de armazenamento – a recuperação não será mais possível.

## OS

### -AccountName
Nome da conta de armazenamento gerenciado do cofre de chaves. O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Force
Não peça confirmação.

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

### -InputObject
Objeto ManagedStorageAccount.

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

### -Inremovestate
Remova permanentemente a conta de armazenamento gerenciado anteriormente excluída.

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

### -PassThru
O cmdlet não retorna um objeto por padrão.
Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.

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

### -Cofrename
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem

## EXIBE

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## INFORMA

## LINKS RELACIONADOS

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

