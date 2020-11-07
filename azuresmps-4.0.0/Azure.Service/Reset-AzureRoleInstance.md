---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945480"
---
# Reset-AzureRoleInstance

## Sinopse
Solicita uma reinicialização ou reimagem de uma única instância de função ou de todas as instâncias de função de uma função específica.

## SYNTAX

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Reset-AzureRoleInstance** solicita uma reinicialização ou uma reimagem de uma instância de função que está sendo executada em uma implantação.
Esta operação é executada sincronicamente.
Quando você reinicializa uma instância de função, o Azure leva a instância offline, reinicia o sistema operacional subjacente para essa instância e coloca a instância novamente online.
Todos os dados gravados no disco local persistem nas reinicializações.
Todos os dados que estiverem na memória serão perdidos.

A recriação de uma instância de uma instância de função resulta em um comportamento diferente dependendo do tipo de função.
Para uma função de trabalho ou Web, quando a função é renovada, o Azure leva a função offline e grava uma instalação nova do sistema operacional convidado do Azure para a máquina virtual.
A função é então colocada novamente online.
Para uma função de VM, quando a função é renovada, o Azure leva a função offline, reaplica a imagem personalizada que você forneceu para ele e coloca a função online novamente.

O Azure tenta manter dados em qualquer recurso de armazenamento local quando a função é renovada; no entanto, no caso de uma falha transitória de hardware, o recurso de armazenamento local pode ser perdido.
Se o seu aplicativo requer que os dados persistam, é recomendável gravar em uma fonte de dados durável, como uma unidade do Azure.
Todos os dados gravados em um diretório local diferente daquele definido pelo recurso de armazenamento local serão perdidos quando a função for refeita a imagem.

## EXEMPLOS

### Exemplo 1: reinicie uma instância de função
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Esse comando reinicializa a instância de função chamada MyWebRole_IN_0 na implantação de preparo do serviço MySvc01.

### Exemplo 2: reimagem de uma instância de função
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Esse comando renovar as instâncias de função na implantação de preparo do serviço de nuvem do MySvc01.

### Exemplo 3: reimagem de todas as instâncias de função
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Esse comando renovar todas as instâncias de função na implantação de produção do serviço MySvc01.

## OS

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceName
Especifica o nome da instância de função a ser reinicializada ou reinicializada.

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

### -Reboot
Especifica que esse cmdlet reinicializa a instância de função especificada ou, se nenhuma for especificada, todas as instâncias de função.
Você deve incluir o parâmetro *reboot* ou *Reimage* , mas não ambos.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nova imagem
Especifica que esse cmdlet reimagemia a instância de função especificada ou, se nenhuma for especificada, todas as instâncias de função.
Você deve incluir o parâmetro *reboot* ou *Reimage* , mas não ambos.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Especifica o nome do serviço.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Especifica o ambiente de implantação onde as instâncias de função são executadas.
Os valores válidos são: produção e preparação.
Você pode incluir o *deploymentname* ou o parâmetro *slot* , mas não ambos.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Set-AzureRole](./Set-AzureRole.md)


