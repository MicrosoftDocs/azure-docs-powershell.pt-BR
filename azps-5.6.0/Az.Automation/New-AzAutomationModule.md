---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893243"
---
# New-AzAutomationModule

## SYNOPSIS
Importa um módulo para Automação.

## SINTAXE

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzAutomationModule** importa um módulo para a Automação do Azure.
Este comando aceita um arquivo compactado que tem uma extensão de nome de arquivo .zip.
O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos: 
- Windows PowerShell módulo, que tem uma extensão de nome de arquivo .psm1 ou .dll 
- Windows PowerShell de módulo, que tem uma extensão de nome de arquivo .psd1 O nome do arquivo .zip, o nome da pasta e o nome do arquivo na pasta devem ser os mesmos.
Especifique o arquivo .zip como uma URL que o serviço de Automação pode acessar.
Se você importar um Windows PowerShell para Automação usando este cmdlet ou o cmdlet Set-AzAutomationModule, a operação será assíncrona.
O comando termina se a importação é bem-sucedida ou falha.
Para verificar se foi bem-sucedido, execute o seguinte comando: ModuleName Verifique a propriedade `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` **ProvisioningState** para obter um valor de Succeeded.

## EXEMPLOS

### Exemplo 1: Importar um módulo
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Este comando importa um módulo chamado ContosoModule para a conta de automação chamada Contoso17.
O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e em um contêiner denominado módulos.

## PARÂMETROS

### -AutomationAccountName
Especifica o nome da conta de automação para a qual esse cmdlet importa um módulo.

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

### -ContentLinkUri
A url de um pacote zip de módulo

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Name
Especifica o nome do módulo que esse cmdlet importa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos para o qual esse cmdlet importa um módulo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Uri

## SAÍDAS

### Microsoft.Azure.Commands.Automation.Model.Module

## NOTES

## LINKS RELACIONADOS

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


