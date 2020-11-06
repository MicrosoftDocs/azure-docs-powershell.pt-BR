---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 5e0766039a9becb65aaec13d08e46f751893b8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432160"
---
# Get-AzureRmTag

## Sinopse
Obtém marcas predefinidas do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmTag** tem marcas predefinidas do Azure na sua assinatura.
Esse cmdlet retorna informações básicas sobre as marcas ou informações detalhadas sobre marcas e seus valores.
Todos os objetos de saída incluem uma propriedade Count que representa o número de recursos e grupos de recursos aos quais as marcas e os valores foram aplicados.

O módulo de marcas do Azure que **Get-AzureRMTag** é parte de pode ajudá-lo a gerenciar marcas predefinidas do Azure.
Uma marca do Azure é um par nome-valor que você pode usar para categorizar seus recursos e grupos de recursos do Azure, por exemplo, por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos e grupos.

Você pode definir e aplicar marcas em uma única etapa, mas as marcas predefinidas permitem estabelecer nomes e valores padrão, consistentes, previsíveis para as marcas na sua assinatura.
Se a assinatura incluir marcas predefinidas, não será possível aplicar marcas ou valores indefinidos a nenhum recurso ou grupo de recursos na assinatura.

Para criar uma marca predefinida, use o cmdlet New-AzureRmTag.
Para aplicar uma marca predefinida a um grupo de recursos, use o parâmetro *tag* do cmdlet New-AzureRmTag.
Para pesquisar grupos de recursos para um nome de marca ou nome ou valor específico, use o parâmetro *tag* do cmdlet Get-AzureRMResourceGroup.

## EXEMPLOS

### Exemplo 1: obter todas as marcas predefinidas
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Este comando obtém todas as marcas predefinidas na assinatura.
A propriedade Count mostra quantas vezes a marca foi aplicada a recursos e grupos de recursos na assinatura.

### Exemplo 2: obter uma marca por nome
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Esse comando obtém informações detalhadas sobre a marca do departamento e seus valores.
A propriedade Count mostra quantas vezes a marca e cada um dos seus valores foram aplicados a recursos e grupos de recursos na assinatura.

### Exemplo 3: obter valores de todas as marcas
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Esse comando usa o parâmetro *detalhado* para obter informações detalhadas sobre todas as marcas predefinidas na assinatura.
Usar o parâmetro *detailed* é o equivalente a usar o parâmetro *Name* para cada marca.

## OS

### -Detalhado
Indica que essa operação adiciona informações sobre valores de marca à saída.

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

### -Nome
Especifica o nome da marca a ser obtida.
Por padrão, **Get-AzureRmTag** Obtém informações básicas sobre todas as marcas predefinidas na assinatura.
Quando você especifica o parâmetro *Name* , o parâmetro *detalhado* não tem efeito.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. Tags. Model. PSTag, Microsoft. Azure. Commands. Tags

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmTag](./New-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


