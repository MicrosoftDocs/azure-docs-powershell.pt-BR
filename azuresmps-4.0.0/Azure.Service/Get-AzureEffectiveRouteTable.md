---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946353"
---
# Get-AzureEffectiveRouteTable

## Sinopse
Obtém a rota aplicada em uma máquina virtual.

## SYNTAX

### IaaSGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureEffectiveRouteTable** Obtém a rota aplicada em uma máquina virtual.
Esta operação pode demorar vários segundos para ser concluída.

## EXEMPLOS

### Exemplo 1: obter a rota efetiva aplicada a uma máquina virtual
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.
O cmdlet atual Obtém a rota aplicada a essa máquina virtual.

## OS

### -NetworkInterfacename
Especifica o nome do adaptador de rede para o qual este cmdlet obtém rotas efetivas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -RoleInstanceName
Especifica o nome de uma função de PaaS para a qual esse cmdlet obtém rotas efetivas.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Especifica o nome de um serviço na nuvem.
A função de PaaS para a qual este cmdlet obtém rotas efetivas pertence ao serviço que esse parâmetro especifica.

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

### -Slot
Especifica um slot de PaaS.
A função de PaaS para a qual este cmdlet obtém rotas efetivas tem o slot especificado por esse parâmetro.
Os valores válidos são: 

- Preparo
- Preparação 

O valor padrão é produção.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual para o qual este cmdlet obtém rotas efetivas.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network>

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRouteTable](./Get-AzureRouteTable.md)

[New-AzureRouteTable](./New-AzureRouteTable.md)

[Remove-AzureRouteTable](./Remove-AzureRouteTable.md)

[Remove-AzureSubnetRouteTable](./Remove-AzureSubnetRouteTable.md)

[Set-AzureSubnetRouteTable](./Set-AzureSubnetRouteTable.md)


