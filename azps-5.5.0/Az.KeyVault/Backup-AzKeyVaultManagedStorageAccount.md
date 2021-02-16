---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117598"
---
# Backup-AzKeyVaultManagedStorageAccount

## Sinopse
Fazer o back up de uma conta de armazenamento gerenciada pelo KeyVault.

## Sintaxe

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

## Descrição
O cmdlet **Backup-AzKeyVaultManagedStorageAccount** faz backup de uma conta de armazenamento gerenciada especificada em um cofre de chave baixando-a e armazenado-a em um arquivo.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Cofre de Teclas do Azure.
Você pode restaurar uma conta de armazenamento em backup em qualquer cofre de chave da assinatura da sua assinatura, desde que o cofre se mantenha na mesma geografia do Azure.
Os motivos típicos para usar este cmdlet são: 
- Você deseja manter uma cópia offline da conta de armazenamento caso exclua acidentalmente o original do cofre.
 
- Você criou uma conta de armazenamento gerenciado usando o Cofre de Teclas e agora deseja clonar o objeto em uma região diferente do Azure, para poder usá-lo em todas as instâncias do aplicativo distribuído.
Use o cmdlet **Backup-AzKeyVaultManagedStorageAccount** para recuperar a conta de armazenamento gerenciado em formato criptografado e use o cmdlet **Restore-AzKeyVaultManagedStorageAccount** e especifique um cofre de chave na segunda região.

## Exemplos

### Exemplo 1: Fazer o back up de uma conta de armazenamento gerenciado com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Esse comando recupera a conta de armazenamento gerenciada chamada MyMSAK do cofre de chave MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.

### Exemplo 2: Fazer o back up de uma conta de armazenamento gerenciada para um nome de arquivo especificado
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Esse comando recupera a conta de armazenamento gerenciada chamada MyMSAK do cofre de chave MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo chamado Backup.blob.

### Exemplo 3: Fazer o back up de uma conta de armazenamento gerenciada recuperada anteriormente para um nome de arquivo especificado, sobrescrever o arquivo de destino sem solicitar.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando cria um backup da conta de armazenamento gerenciada chamada $msak. Nome no cofre chamado $msak. VaultName para um arquivo chamado Backup.blob, sobrescrever silenciosamente o arquivo se ele já existir.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Forçar
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
Pacote de conta de armazenamento a ser feito backup, com pipeline a partir da saída de uma chamada de recuperação.

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

### -Nome
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
Se não especificado, será gerado um nome de arquivo padrão.

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

### -Nomedo Cofre
Nome do cofre.
O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## Saídas

### System.String

## Notas

## LINKS RELACIONADOS
