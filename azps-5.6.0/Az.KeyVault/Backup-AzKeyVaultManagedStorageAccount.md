---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890400"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
O back up a KeyVault-managed storage account.

## SINTAXE

### ByStorageAccountName (Padrão)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Backup-AzKeyVaultManagedStorageAccount** faz backup de uma conta de armazenamento gerenciada especificada em um cofre de chaves baixando-a e armazená-la em um arquivo.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Azure Key Vault.
Você pode restaurar uma conta de armazenamento com backup em qualquer cofre de chaves da assinatura da sua assinatura, desde que o cofre seja na mesma geografia do Azure.
Os motivos típicos para usar esse cmdlet são: 
- Você deseja manter uma cópia offline da conta de armazenamento caso exclua acidentalmente o original do cofre.
 
- Você criou uma conta de armazenamento gerenciado usando o Cofre de Chaves e agora deseja clonar o objeto em uma região diferente do Azure, para que você possa usá-lo de todas as instâncias do seu aplicativo distribuído.
Use o cmdlet **Backup-AzKeyVaultManagedStorageAccount** para recuperar a conta de armazenamento gerenciado em formato criptografado e, em seguida, use o cmdlet **Restore-AzKeyVaultManagedStorageAccount** e especifique um cofre de chaves na segunda região.

## EXEMPLOS

### Exemplo 1: Fazer o back up de uma conta de armazenamento gerenciado com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Este comando recupera a conta de armazenamento gerenciado chamada MyMSAK do cofre de chaves chamado MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.

### Exemplo 2: Fazer o back up de uma conta de armazenamento gerenciado para um nome de arquivo especificado
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Este comando recupera a conta de armazenamento gerenciado chamada MyMSAK do cofre de chaves chamado MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo chamado Backup.blob.

### Exemplo 3: Fazer o back up de uma conta de armazenamento gerenciado recuperada anteriormente para um nome de arquivo especificado, sobrescrevendo o arquivo de destino sem solicitar.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando cria um backup da conta de armazenamento gerenciado chamada $msak. Nome no cofre chamado $msak. VaultName para um arquivo chamado Backup.blob, sobrescrevendo silenciosamente o arquivo se ele já existir.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
Substituir o arquivo determinado se ele existir

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
Pacote de conta de armazenamento a ser feito com backup, canalizou a partir da saída de uma chamada de recuperação.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome secreto.
O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Arquivo de saída.
O arquivo de saída para armazenar o backup da conta de armazenamento.
Se não for especificado, um nome de arquivo padrão será gerado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## SAÍDAS

### System.String

## NOTES

## LINKS RELACIONADOS
