---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439932"
---
# Remove-AzureKeyVaultSecret

## Sinopse
Exclui um segredo em um cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Remove-AzureKeyVaultSecret exclui um segredo em um cofre de chaves.
Se o segredo foi excluído acidentalmente, o segredo pode ser recuperado usando Undo-AzureKeyVaultSecretRemoval por um usuário com permissões "recuperar" especiais.
Esse cmdlet tem um valor alto para a propriedade **ConfirmImpact** .

## EXEMPLOS

### Exemplo 1: remover um segredo de um cofre de chaves
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso. '

### Exemplo 2: remover um segredo de um cofre de chaves sem confirmação do usuário
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

Esse comando Remove o segredo nomeado FinanceSecret do cofre de chaves chamado contoso.
O comando especifica os parâmetros de *forçar* e *confirmação* e, portanto, o cmdlet não solicita a confirmação.

### Exemplo 3: limpar o segredo excluído do cofre de chaves permanentemente
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

Esse comando premove o segredo nomeado FinanceSecret do cofre da chave chamado contoso permanentemente.
A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário para esse cofre de chaves.

## OS

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

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

### -Inremovestate
Se presente, remove o segredo anteriormente excluído permanentemente.

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

### -Nome
Especifica o nome de um segredo.
Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna um objeto **Microsoft. Azure. Commands. keyvault. Models. Secret** .
Por padrão, esse cmdlet não gera nenhuma saída.

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
Especifica o nome do cofre de chaves ao qual o segredo pertence.
Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.

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
O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.
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

### Microsoft. Azure. Commands. keyvault. Models. DeletedSecret
Esse cmdlet retornará um valor apenas se você especificar o parâmetro *PassThru* .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Desfazer-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

