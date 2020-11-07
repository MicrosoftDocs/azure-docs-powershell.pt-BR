---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945434"
---
# Set-AzureTrafficManagerEndpoint

## Sinopse
Atualiza as propriedades de um ponto de extremidade em um perfil do Gerenciador de tráfego.

## SYNTAX

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureTrafficManagerEndpoint** atualiza as propriedades de um ponto de extremidade em um perfil do Gerenciador de tráfego do Microsoft Azure.
Se o ponto de extremidade não existir no perfil atual, esse cmdlet o criará.
Depois de adicionar um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.
Esse cmdlet se conecta ao Azure para salvar suas alterações.

## EXEMPLOS

### Exemplo 1: atualizar um ponto de extremidade para um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.

O segundo comando atualiza o ponto de extremidade no perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.
O ponto de extremidade tem o nome de domínio ContosoApp02.cloudapp.net.
O comando também especifica o status, o tipo, a espessura e o local do ponto de extremidade.
O comando passa o perfil modificado para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.

## OS

### -DomainName
Especifica o nome de domínio do ponto de extremidade a ser modificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Especifica o local do ponto de extremidade que o cmdlet adiciona.
Deve ser um local do Azure.

Esse parâmetro deve conter um valor de pontos de extremidade do tipo "any" ou do tipo "Trafficmanager" em um perfil que tenha o método de balanceamento de carga definido como "performance".
Os valores possíveis são os nomes de região do Azure, conforme listado em  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Especifica o número mínimo de pontos de extremidade que o perfil aninhado deve ter online para que este ponto de extremidade seja considerado online.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Status
Especifica o status do ponto de extremidade de monitoramento.
Os valores válidos são: 

- Possibilita
- Ativo

Se você especificar um valor habilitado, o Gerenciador de tráfego monitorará o ponto de extremidade e o método de balanceamento de carga o considerará ao gerenciar o tráfego.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Especifica o objeto de perfil do Gerenciador de tráfego para o qual modificar o ponto de extremidade.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de ponto de extremidade.
Os valores válidos são: 

- CloudService
- AzureWebsite
- Trafficmanager

- Qualquer 

Se houver mais de um ponto de extremidade AzureWebsite, os pontos de extremidade deverão estar em datacenters diferentes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
Especifica a espessura do ponto de extremidade que o cmdlet adiciona.
O intervalo de valores válido para esse parâmetro é \[ 1, 1000 \] .

Esse parâmetro é usado apenas para políticas de balanceamento de carga do RoundRobin.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego, que contém informações sobre o perfil atualizado.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


