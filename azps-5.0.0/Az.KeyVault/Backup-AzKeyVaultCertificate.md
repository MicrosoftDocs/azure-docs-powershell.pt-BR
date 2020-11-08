---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126173"
---
# Backup-AzKeyVaultCertificate

## Sinopse
Faz backup de um certificado em um cofre de chaves.

## SYNTAX

### ByCertificateName (padrão)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **backup-AzKeyVaultCertificate** faz backup de um certificado especificado em um cofre de chaves, fazendo o download dele e armazenando-o em um arquivo.
Se o certificado tiver várias versões, todas as suas versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.
Você pode restaurar um certificado de backup para qualquer cofre de chaves na assinatura a partir da qual o backup foi feito, desde que o cofre esteja na mesma Geografia do Azure.
Os motivos típicos para usar este cmdlet são: 
- Você deseja manter uma cópia offline do certificado caso você exclua acidentalmente o original do cofre.
 
- Você criou um certificado usando o Key Vault e agora deseja clonar o objeto para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído.
Use o cmdlet **backup-AzKeyVaultCertificate** para recuperar o certificado em formato criptografado e, em seguida, use o cmdlet **Restore-AzKeyVaultCertificate** e especifique um cofre de chaves na segunda região.

## EXEMPLOS

### Exemplo 1: fazer backup de um certificado com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Esse comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.

### Exemplo 2: fazer backup de um certificado em um nome de arquivo especificado
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Esse comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo chamado backup. blob.

### Exemplo 3: fazer backup de um certificado recuperado anteriormente em um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Esse comando cria um backup do certificado chamado $cert. Nome no cofre chamado $cert. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Segredo para backup, em pipeline a partir da saída de uma chamada de recuperação.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do segredo.
O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Arquivo de saída.
O arquivo de saída para armazenar o backup do certificado.
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

### -Cofrename
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
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

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS
