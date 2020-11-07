---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946477"
---
# Remove-AzureEnvironment

## Sinopse
Exclui um ambiente do Azure do Windows PowerShell.

## SYNTAX

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureEnvironment** exclui um ambiente do Azure do seu perfil móvel, portanto, o Windows PowerShell não consegue encontrá-lo.
Esse cmdlet não exclui o ambiente do Microsoft Azure ou muda o ambiente real de qualquer forma.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## EXEMPLOS

### Exemplo 1: excluir um ambiente
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Esse comando exclui o ambiente ContosoEnv do Windows PowerShell.

### Exemplo 2: excluir vários ambientes
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Esse comando exclui ambientes cujos nomes começam com "contoso" do Windows PowerShell.

## OS

### -Force
Suprime o prompt de confirmação.

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
Especifica o nome do ambiente a ser removido.
Esse parâmetro é obrigatório.
Esse valor de parâmetro diferencia maiúsculas de minúsculas.
Caracteres curinga não são permitidos.

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

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


