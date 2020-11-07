---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946223"
---
# New-AzureAutomationModule

## Sinopse

Importa um módulo para a automação.

## SYNTAX

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

O cmdlet **New-AzureAutomationModule** importa um módulo para a automação do Azure.
Um módulo é um arquivo compactado com uma extensão. zip, que contém uma pasta que inclui um dos seguintes tipos de arquivo:

- Um módulo do Windows PowerShell (arquivo psm1). 

- Um manifesto do módulo do Windows PowerShell (arquivo psd1). 

- Um assembly (arquivo dll).

Os nomes do arquivo zip, a pasta no arquivo zip e o arquivo na pasta (. psm1, PSD. 1 ou. dll) devem coincidir.

## EXEMPLOS

### Exemplo 1: importar um módulo
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

Esse comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.
O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e um contêiner chamado modules.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação na qual o módulo será armazenado.

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

### -ContentLink
URL pública, como um site ou um armazenamento de blob do Azure que especifica o caminho para o arquivo de módulo.
Este local deve ser acessível publicamente.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome para o módulo.

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
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -Marcas
Especifica uma ou mais marcas relacionadas ao módulo.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. Module

## INFORMA

## LINKS RELACIONADOS

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Set-AzureAutomationModule](./Set-AzureAutomationModule.md)


