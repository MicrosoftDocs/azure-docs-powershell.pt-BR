---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774677"
---
# Get-AzsDisk

## Sinopse
Retorna a lista de discos gerenciados que podem ser migrados no compartilhamento especificado.

## SYNTAX

### Lista (padrão)
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### Obter
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## DESCRITIVO
Retorna uma lista de discos.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
$disks = Get-AzsDisk -location local
```

Retorna uma lista de discos gerenciados no local local.
Por padrão, ele vai usar os primeiros 100 discos

### --------------------------EXEMPLO 2--------------------------
```
$disk = Get-AzsDisk -location local -name $DiskId
```

Obter um disco gerenciado específico.

## OS

### -Contagem
O número máximo de discos a serem retornados.

```yaml
Type: Int32
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
A GUID de disco como identidade.

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SharePath
O compartilhamento de origem ao qual o recurso pertence.

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

### -Início
O índice inicial de discos na consulta.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Os parâmetros do estado do disco.

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

### -Usersubscriptionid
ID da assinatura de locatário à qual o recurso pertence.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. COMPUTE. admin. Models. Disk

## INFORMA

## LINKS RELACIONADOS

