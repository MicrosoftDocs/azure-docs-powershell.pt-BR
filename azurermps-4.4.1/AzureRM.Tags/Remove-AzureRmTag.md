---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610142"
---
# Remove-AzureRmTag

## Sinopse
Exclui valores ou marcas predefinidas do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmTag** exclui as marcas e os valores predefinidos do Azure de sua assinatura.
Para excluir valores específicos de uma marca predefinida, use o parâmetro *Value* .
Por padrão, **Remove-AzureRmTag** exclui a marca especificada e todos os seus valores. Não é possível excluir uma marca ou um valor que seja aplicado no momento a um recurso ou grupo de recursos.

Antes de usar **Remove-AzureRmTag** , use o parâmetro *Tag* do cmdlet Set-AzureRMResourceGroup para excluir a marca ou os valores do recurso ou do grupo de recursos.

O módulo de marcas do Azure que **Remove-AzureRmTag** faz parte do pode ajudá-lo a gerenciar suas marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.

Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.

## EXEMPLOS

### Exemplo 1: excluir uma marca predefinida
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

Este comando exclui a marca predefinida chamada Department e todos os seus recursos.
Se a marca tiver sido aplicada a recursos ou grupos de recursos, o comando falhará.

### Exemplo 2: excluir um valor de uma marca predefinida
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Esse comando exclui o valor HumanResources da marca de departamento predefinida.
Ele não exclui a marca.
Se o valor tiver sido aplicado a recursos ou grupos de recursos, o comando falhará.

## OS

### -Nome
Especifica o nome da marca a ser excluída.
Por padrão, **Remove-AzureRmTag** remove a marca especificada e todos os seus valores.
Para excluir os valores selecionados, mas não excluir a marca, use o parâmetro *Value* .

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

### -PassThru
Retorna um objeto que representa a marca excluída ou a marca resultante com valor excluído.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valor
Exclui os valores especificados da marca predefinida, mas não exclui a marca.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
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

### Nenhuma

## EXIBE

### None ou Microsoft. Azure. Commands. Tags. Model. PSTag

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmTag](./Get-AzureRmTag.md)

[New-AzureRmTag](./New-AzureRmTag.md)


