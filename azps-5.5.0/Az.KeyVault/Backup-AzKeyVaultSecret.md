---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114816"
---
# Backup-AzKeyVaultSecret

## Sinopse
Fazer o back up de um segredo em um cofre de chaves.

## Sintaxe

### BySecsecname (Padrão)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecsec
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Backup-AzKeyVaultSec ltd** faz backup de um segredo especificado em um cofre de teclas baixando-o e armazenar-o em um arquivo.
Se houver várias versões do segredo, todas as versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Cofre de Teclas do Azure.
Você pode restaurar um backup de um segredo para qualquer cofre de chave na assinatura de onde ele foi feito backup.
Os motivos típicos para usar este cmdlet são:
- Você deseja escrow uma cópia do seu segredo, para que você tenha uma cópia offline caso exclua acidentalmente seu segredo no seu cofre de chaves.
- Você adicionou um segredo a um cofre de chaves e agora deseja clonar o segredo em uma região diferente do Azure, para poder usá-lo em todas as instâncias do seu aplicativo distribuído. Use o cmdlet Backup-AzKeyVaultSecret para recuperar o segredo em formato criptografado e, em seguida, use o cmdlet Restore-AzKeyVaultSecret e especifique um cofre de chave na segunda região. (Observe que as regiões devem pertencer à mesma geografia.)

## Exemplos

### Exemplo 1: Fazer o back up de um segredo com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Esse comando recupera o segredo Chamado MySecsecsec do cofre de teclas chamado MyKeyVault e salva um backup desse segredo em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.

### Exemplo 2: Fazer o back up de um segredo para um nome de arquivo especificado, sobrescrever o arquivo existente sem solicitar
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando recupera o segredo chamado MySecsecsec do cofre de chave MyKeyVault e salva um backup desse segredo em um arquivo chamado Backup.blob.

### Exemplo 3: Fazer o back up de um segredo recuperado anteriormente para um nome de arquivo especificado
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Esse comando usa o nome $secret do cofre do objeto para recuperar o segredo e salva seu backup em um arquivo chamado Backup.blob.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Solicita confirmação antes de sobrescrever o arquivo de saída, se houver.

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
Segredo para ser feito backup, com pipeline a partir da saída de uma chamada de recuperação.

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
Especifica o nome do segredo para fazer o back-up.

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
Especifica o arquivo de saída no qual o blob de backup está armazenado.
Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.
Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro de que o arquivo de backup já existe.

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
Especifica o nome do cofre de chave que contém o segredo para fazer o back-up.

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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecibleIdentityItem

## Saídas

### System.String

## Notas

## LINKS RELACIONADOS

[Set-AzKeyVaultSec cue](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSec cue](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSec cue](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSec cue](./Restore-AzKeyVaultSecret.md)

