---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261364"
---
# Backup-AzKeyVaultSecret

## Sinopse
Faz o backup de um segredo em um cofre de chaves.

## SYNTAX

### BySecretName (padrão)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **backup-AzKeyVaultSecret** faz backup de um segredo especificado em um cofre de chaves, baixando-o e armazenando-o em um arquivo.
Se houver várias versões do segredo, todas as versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.
Você pode restaurar um segredo em backup para qualquer cofre de chaves na assinatura do qual foi feito o backup.
Os motivos típicos para usar este cmdlet são:
- Você deseja fazer a caução de uma cópia do seu segredo, para que você tenha uma cópia offline, caso você exclua acidentalmente seu segredo no seu cofre de chaves.
- Você adicionou um segredo a um cofre de chaves e agora deseja clonar o segredo para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído. Use o cmdlet Backup-AzKeyVaultSecret para recuperar o segredo no formato criptografado e use o cmdlet Restore-AzKeyVaultSecret e especifique um cofre de chaves na segunda região. (Observe que as regiões devem pertencer à mesma geografia.)

## EXEMPLOS

### Exemplo 1: fazer backup de um segredo com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Esse comando recupera o segredo nomeado MySecret do cofre de chaves chamado MyKeyVault e salva um backup desse segredo em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.

### Exemplo 2: fazer backup de um segredo em um nome de arquivo especificado, substituindo o arquivo existente sem avisar
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando recupera o segredo chamado MySecret da chave vaultnamed MyKeyVault e salva um backup desse segredo em um arquivo chamado backup. blob.

### Exemplo 3: fazer backup de um segredo anteriormente recuperado para um nome de arquivo especificado
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Esse comando usa o nome e o nome do cofre do objeto de $secret para recuperar o segredo e salva o backup em um arquivo chamado backup. blob.

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
Solicita confirmação antes de substituir o arquivo de saída, se houver.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Segredo para backup, em pipeline a partir da saída de uma chamada de recuperação.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do segredo para fazer backup.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

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
Especifica o nome do cofre de chaves que contém o segredo para fazer backup.

```yaml
Type: System.String
Parameter Sets: BySecretName
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

