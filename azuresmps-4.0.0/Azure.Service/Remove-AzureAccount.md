---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945870"
---
# Remove-AzureAccount

## Sinopse
Exclui uma conta do Azure do Windows PowerShell.

## SYNTAX

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureAccount** exclui uma conta do Azure e suas assinaturas do arquivo de dados de assinatura em seu perfil de usuário móvel.
Ele não exclui a conta do Microsoft Azure ou muda a conta real de qualquer forma.

Usar esse cmdlet é muito parecido com o logoff da sua conta do Azure.
E, se você quiser entrar na conta novamente, use o **Add-AzureAccount** ou **Import-AzurePublishSettingsFile** para adicionar a conta ao Windows PowerShell novamente.

Você também pode usar o cmdlet **Remove-AzureAccount** para alterar a maneira como os cmdlets do Azure PowerShell entram na sua conta do Azure.
Se a sua conta tiver um certificado de gerenciamento da **importação-AzurePublishSettingsFile** e um token de acesso de **Add-AzureAccount** , os cmdlets do PowerShell do Azure usarão apenas o token de acesso; Eles ignoram o certificado de gerenciamento.
Para usar o certificado de gerenciamento, execute **Remove-AzureAccount**.
Quando **Remove-AzureAccount** encontra um certificado de gerenciamento e um token de acesso, ele exclui somente o token de acesso, em vez de excluir a conta.
O certificado de gerenciamento ainda existe, portanto, a conta ainda está disponível para o Windows PowerShell.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: remover uma conta
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Esse comando Remove o admin@contoso.com do arquivo de dados da sua assinatura.
Quando o comando é concluído, a conta não está mais disponível para o Windows PowerShell.

## OS

### -Force
Suprime o prompt de confirmação.
Por padrão, **Remove-AzureAccount** solicita que você antes de remover a conta do Windows PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da conta a ser removida.
O valor do parâmetro diferencia maiúsculas de minúsculas.
Não há suporte para caracteres curinga.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna $True se o comando tiver êxito e $False se falhar.
Por padrão, esse cmdlet não retorna nenhuma saída.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### None ou System. Boolean
Se você usar o parâmetro *PassThru* , esse cmdlet retornará um valor booliano.
Caso contrário, ele não retorna nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


