---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945819"
---
# Set-AzureServiceProject

## Sinopse
Define a localização, a assinatura, o slot e a conta de armazenamento padrão para o serviço atual.

## SYNTAX

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureServiceProject** define o local de implantação, o slot, a conta de armazenamento e a assinatura do serviço atual.
Esses valores são usados sempre que o serviço é publicado na nuvem.

## EXEMPLOS

### Exemplo 1: configurações básicas
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Define o local de implantação do serviço para a região norte central dos EUA.
Define o slot de implantação como produção. Define a conta de armazenamento que será usada para testar a definição do serviço para myStorageAccount.
Define a assinatura que hospedará o serviço para a minha assinatura.
Sempre que o serviço for publicado na nuvem, ele será hospedado em um Data Center na região do Norte Central dos EUA, ele atualizará o slot de implantação e usará a assinatura especificada e a conta de armazenamento.

## OS

### -Local
A região em que o serviço será hospedado.
Esse valor é usado sempre que o serviço for publicado na nuvem.
Os valores possíveis são: em qualquer lugar da Ásia, em qualquer lugar da Europa, em qualquer lugar, na Ásia Oriental, no leste dos EUA, centro-norte da América do Sul, centro-oeste dos EUA, Sudeste Asiático, West Europe, West US.

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

### -PassThru
Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.
Por padrão, esse cmdlet não gera nenhuma saída.

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

### -Slot
O slot (produção ou preparação) em que o serviço será hospedado.
Esse valor é usado sempre que o serviço for publicado na nuvem.
Os valores possíveis são: produção, preparação.

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

### -Armazenamento
A conta de armazenamento a ser usada ao carregar o pacote de serviço para a nuvem.
Se a conta de armazenamento não existir, ela será criada quando o serviço for publicado na nuvem.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA
* nó-dev, php-dev, Python-dev

## LINKS RELACIONADOS

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Publicar-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


