---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425814"
---
# Get-AzsNetworkQuota

## Sinopse
Listar todas as cotas.

## SYNTAX

### Lista (padrão)
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### Obter
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Listar todas as cotas.
Limite a lista passando um nome ou um filtro.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsNetworkQuota
```

Lista todas as cotas de rede.

### --------------------------EXEMPLO 2--------------------------
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

Obtém a cota de rede especificada.

## OS

### -Filtro
Parâmetro de filtro OData.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Local do recurso.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do recurso de cota da rede.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. Network. admin. Models. quota

## INFORMA

## LINKS RELACIONADOS

