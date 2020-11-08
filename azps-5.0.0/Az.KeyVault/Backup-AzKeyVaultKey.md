---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126171"
---
# Backup-AzKeyVaultKey

## Sinopse
Faz o backup de uma chave em um cofre de chaves.

## SYNTAX

### ByKeyName (padrão)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **backup-AzKeyVaultKey** faz backup de uma chave especificada em um cofre de chaves, baixando-a e armazenando-a em um arquivo.
Se houver várias versões da chave, todas as versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.
Você pode restaurar uma chave em backup para qualquer cofre de chaves na assinatura da qual foi feito o backup.
Os motivos típicos para usar este cmdlet são: 
- Você deseja fazer a caução de uma cópia da sua chave para que você tenha uma cópia offline em caso de excluir acidentalmente a chave no seu cofre de chaves.
 
- Você criou uma chave usando o Key Vault e agora deseja clonar a chave para uma região diferente do Azure, de modo que você possa usá-la em todas as instâncias do seu aplicativo distribuído.
Use o cmdlet **backup-AzKeyVaultKey** para recuperar a chave no formato criptografado e, em seguida, use o cmdlet Restore-AzKeyVaultKey e especifique um cofre de chaves na segunda região.

## EXEMPLOS

### Exemplo 1: fazer backup de uma chave com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Esse comando recupera a chave chamada MyKey do cofre de chaves chamado MyKeyVault e salva um backup dessa chave em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.

### Exemplo 2: fazer backup de uma chave em um nome de arquivo especificado
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Esse comando recupera a chave chamada MyKey da chave vaultnamed MyKeyVault e salva um backup dessa chave em um arquivo chamado backup. blob.

### Exemplo 3: fazer backup de uma chave recuperada anteriormente para um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando cria um backup da chave chamada $key. Nome no cofre chamado $key. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.

## OS

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
Substituir o arquivo fornecido se ele existir

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
Pacote de chaves para backup, em pipeline a partir da saída de uma chamada de recuperação.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da chave para fazer backup.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Especifica o arquivo de saída no qual o blob de backup é armazenado.
Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.
Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro informando que o arquivo de backup já existe.

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

### -Cofrename
Especifica o nome do cofre de chaves que contém a chave para fazer backup.

```yaml
Type: System.String
Parameter Sets: ByKeyName
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

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

