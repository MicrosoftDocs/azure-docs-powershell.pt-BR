---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427919"
---
# Get-AzureKeyVaultSecret

## Sinopse
Obtém os segredos em um cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByVaultName (padrão)
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureKeyVaultSecret** Obtém segredos em um cofre de chaves.
Esse cmdlet obtém um segredo específico ou todos os segredos em um cofre de chaves.

## EXEMPLOS

### Exemplo 1: obter todas as versões atuais de todos os segredos em um cofre de chaves
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado contoso.

### Exemplo 2: obter todas as versões de um segredo específico
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Este comando obtém todas as versões do segredo chamado ITSecret no cofre de chaves chamado contoso.

### Exemplo 3: obter a versão atual de um segredo específico
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Esse comando obtém a versão atual do segredo chamado ITSecret no cofre de chaves chamado contoso.

### Exemplo 4: obter uma versão específica de um segredo específico
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Esse comando obtém uma versão específica do segredo chamado ITSecret no cofre de chaves chamado contoso.

### Exemplo 5: obter o valor de texto sem formatação da versão atual de um segredo específico
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Esses comandos obtêm a versão atual de um segredo chamado ITSecret e exibem o valor de texto sem formatação desse segredo.

### Exemplo 6: obter todos os segredos que foram excluídos, mas não foram removidos para este cofre de chaves.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Esse comando obtém todos os segredos que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.

### Exemplo 7: Obtém a ITSecret secreta que foi excluída, mas não é eliminada para este cofre de chaves.
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Esse comando obtém o segredo ITSecret que foi excluído anteriormente, mas não é removido, no cofre de chaves chamado contoso.
Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse segredo excluído.

## OS

### -IncludeVersions
Indica que esse cmdlet obtém todas as versões de um segredo.
A versão atual de um segredo é a primeira na lista.
Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .

Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual do segredo com o *nome* especificado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inremovestate
Especifica se os segredos excluídos anteriormente na saída devem ser mostrados.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do segredo a obter.

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves ao qual o segredo pertence.
Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome que esse parâmetro especifica e seu ambiente atual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versão
Especifica a versão secreta.
Esse cmdlet constrói o FQDN de um segredo com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do segredo e na versão secreta.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### String

## EXIBE

### List<Microsoft. Azure. Commands. keyvault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. Secret, List<Microsoft. Azure. Commands. keyvault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedSecret

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Desfazer-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

