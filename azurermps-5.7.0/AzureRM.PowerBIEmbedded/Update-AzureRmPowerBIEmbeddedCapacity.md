---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426663"
---
# Update-AzureRmPowerBIEmbeddedCapacity

## Sinopse
Modifica uma instância da capacidade inserida do PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Update-AzureRmPowerBIEmbeddedCapacity modifica uma instância da capacidade inserida do PowerBI

## EXEMPLOS

### Exemplo 1
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}

```

Modifica a capacidade chamada testcapacity no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com

## OS

### -Nome
Nome da capacidade inserida do PowerBI

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos do Azure ao qual a capacidade pertence

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -SKU
O nome da SKU para a capacidade.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### -Administrador
Um nome de capacidade separada por vírgulas para definir como administrador na capacidade

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -ResourceId
ResourceId da capacidade inserida do PowerBI.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Objeto de entrada para tubulação

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito

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

### -Confirme
Solicita que o usuário confirme se deseja executar a operação

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Descreve as ações que a operação atual executará sem realmente executá-las

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
