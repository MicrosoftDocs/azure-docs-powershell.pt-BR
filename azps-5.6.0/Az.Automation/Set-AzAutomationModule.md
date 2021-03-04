---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892880"
---
# Set-AzAutomationModule

## SYNOPSIS
Atualiza um módulo em Automação.

## SINTAXE

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzAutomationModule** atualiza um módulo no Azure Automation.
Este comando aceita um arquivo compactado que tem uma extensão de nome de arquivo .zip.
O arquivo contém uma pasta que inclui um arquivo que é um dos seguintes tipos: 
- wps_2 módulo, que tem uma extensão de nome de arquivo .psm1 ou .dll 
- wps_2 de módulo, que tem uma extensão de nome de arquivo .psd1 O nome do arquivo .zip, o nome da pasta e o nome do arquivo na pasta devem ser os mesmos.
Especifique o arquivo .zip como uma URL que o serviço de Automação pode acessar.
Se você importar um wps_2 para Automação usando este cmdlet ou o cmdlet New-AzAutomationModule, a operação será assíncrona.
O comando termina se a importação é bem-sucedida ou falha.
Para verificar se foi bem-sucedido, execute o seguinte comando: ModuleName Verifique a propriedade `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` **ProvisioningState** para obter um valor de Succeeded.

## EXEMPLOS

### Exemplo 1: atualizar um módulo
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Este comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de Automação chamada Contoso17.  O módulo é armazenado em um blob do Azure em uma conta de armazenamento chamada contosostorage e em um contêiner denominado módulos.

## PARÂMETROS

### -AutomationAccountName
Especifica o nome da conta de automação para a qual este cmdlet atualiza um módulo.

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
Especifica a URL do arquivo .zip que contém a nova versão de um módulo que esse cmdlet importa.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Especifica a versão do módulo ao qual este cmdlet atualiza a Automação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Especifica o nome de um grupo de recursos para o qual este cmdlet atualiza um módulo.

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

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


