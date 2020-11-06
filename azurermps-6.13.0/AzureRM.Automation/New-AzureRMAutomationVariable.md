---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 4036261cd333194a71d302e57e97a1f017554da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426463"
---
# New-AzureRmAutomationVariable

## Sinopse
Cria uma variável de automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmAutomationVariable** cria uma variável na automação do Azure.
Para criptografar a variável, especifique o parâmetro *Encrypted* .
Não é possível modificar o estado criptografado de uma variável após a criação.

## EXEMPLOS

### Exemplo 1: criar uma variável com um valor simples
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

Esse comando cria uma variável chamada StringVariable22 com um valor de cadeia de caracteres na conta de automação chamada Contoso17.

### Exemplo 2: criar uma variável com um valor complexo
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

O primeiro comando obtém uma máquina virtual usando o cmdlet Get-AzureVM.
O comando o armazena na variável $VirtualMachine.
O segundo comando cria uma variável chamada ComplexVariable01 na conta de automação chamada Contoso17.
Esse comando usa um objeto complexo para seu valor, nesse caso, a máquina virtual no $VirtualMachine.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação na qual armazenar a variável.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Descrição
Especifica uma descrição para a variável.

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

### -Criptografado
Especifica se esse cmdlet criptografa o valor da variável para armazenamento.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome para a variável.

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
Especifica o grupo de recursos para o qual esse cmdlet cria uma variável.

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

### -Valor
Especifica um valor para a variável.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Boolean

### System. Object

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. Variable

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmAutomationVariable](./Get-AzureRMAutomationVariable.md)

[Remove-AzureRmAutomationVariable](./Remove-AzureRMAutomationVariable.md)

[Set-AzureRmAutomationVariable](./Set-AzureRMAutomationVariable.md)


