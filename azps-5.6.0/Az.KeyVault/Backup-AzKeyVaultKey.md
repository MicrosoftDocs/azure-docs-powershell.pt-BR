---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888513"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Backs up a key in a key vault.

## SINTAXE

### ByKeyName (Padrão)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Backup-AzKeyVaultKey** faz backup de uma chave especificada em um cofre de chaves baixando-a e armazenar-a em um arquivo.
Se houver várias versões da chave, todas as versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Azure Key Vault.
Você pode restaurar uma chave de backup para qualquer cofre de chaves na assinatura da sua assinatura.
Os motivos típicos para usar esse cmdlet são: 
- Você deseja escrow uma cópia da sua chave, para que você tenha uma cópia offline caso você exclua acidentalmente sua chave no cofre de chaves.
 
- Você criou uma chave usando o Cofre de Chaves e agora deseja clonar a chave em uma região diferente do Azure, para que possa usá-la de todas as instâncias do seu aplicativo distribuído.
Use o cmdlet **Backup-AzKeyVaultKey** para recuperar a chave em formato criptografado e, em seguida, use o cmdlet Restore-AzKeyVaultKey e especifique um cofre de chaves na segunda região.

## EXEMPLOS

### Exemplo 1: Fazer o back up de uma chave com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Este comando recupera a chave chamada MyKey do cofre de chaves chamado MyKeyVault e salva um backup dessa chave em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.

### Exemplo 2: Fazer o back up de uma chave para um nome de arquivo especificado
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Este comando recupera a chave chamada MyKey do cofre de chaves chamado MyKeyVault e salva um backup dessa chave em um arquivo chamado Backup.blob.

### Exemplo 3: Fazer o back up de uma chave recuperada anteriormente para um nome de arquivo especificado, sobrescrevendo o arquivo de destino sem solicitar.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Este comando cria um backup da chave chamada $key. Nome no cofre chamado $key. VaultName para um arquivo chamado Backup.blob, sobrescrevendo silenciosamente o arquivo se ele já existir.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -HsmName
Nome do HSM. O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Pacote chave para fazer o back-up, canalizou a partir da saída de uma chamada de recuperação.

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

### -Name
Especifica o nome da chave para fazer o back-up.

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
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

### -VaultName
Especifica o nome do cofre de chaves que contém a chave para fazer o back-up.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## SAÍDAS

### System.String

## NOTES

## LINKS RELACIONADOS

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

