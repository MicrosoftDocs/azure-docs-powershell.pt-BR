---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280506"
---
# Backup-AzManagedHsmKey

## Sinopse
Faz backup de uma chave em um HSM gerenciado.

## SYNTAX

### ByKeyName (padrão)
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **backup-AzManagedHsmKey** faz backup de uma chave especificada em um HSM gerenciado, baixando-a e armazenando-a em um arquivo.
Se houver várias versões da chave, todas as versões serão incluídas no backup.
Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Azure Managed HSM.
Você pode restaurar uma chave em backup para qualquer HSM gerenciado na assinatura da qual foi feito o backup.
Os motivos típicos para usar este cmdlet são: 
- Você deseja fazer a caução de uma cópia da sua chave para que tenha uma cópia offline em caso de excluir acidentalmente a chave no HSM gerenciado.
 
- Você criou uma chave usando HSM gerenciado e agora deseja clonar a chave em uma região diferente do Azure, de modo que você possa usá-la em todas as instâncias do seu aplicativo distribuído.
Use o cmdlet **backup-AzManagedHsmKey** para recuperar a chave no formato criptografado e, em seguida, use o cmdlet Restore-AzManagedHsmKey e ESPECIFIQUE um HSM gerenciado na segunda região.

## EXEMPLOS

### Exemplo 1: fazer backup de uma chave com um nome de arquivo gerado automaticamente
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

Esse comando recupera a chave chamada TestKey do HSM gerenciado chamado testmhsm e salva um backup dessa chave em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.

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

### -HsmName
Nome do HSM. O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.

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
Nome da chave.
O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.

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
Arquivo de saída.
O arquivo de saída para armazenar o blob de chave de backup em.
Se não estiver presente, um nome de arquivo padrão será escolhido.

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

[Add-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Remove-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[Desfazer-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[Update-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)