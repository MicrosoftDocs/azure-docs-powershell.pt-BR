---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946202"
---
# New-AzureTrafficManagerProfile

## Sinopse
Cria um perfil do Gerenciador de tráfego.

## SYNTAX

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureTrafficManagerProfile** cria um perfil do Gerenciador de tráfego do Microsoft Azure.

Depois de criar um perfil no qual você define o valor de *LoadBalancingMethod* como "failover", é possível determinar a ordem de failover dos pontos de extremidade adicionados ao seu perfil com o cmdlet Add-AzureTrafficManagerEndpoint.
Para obter mais informações, consulte o exemplo 2 abaixo.

## EXEMPLOS

### Exemplo 1: criar um perfil do Gerenciador de tráfego
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Esse comando cria um perfil do Gerenciador de tráfego chamado MyProfile no domínio do Gerenciador de tráfego especificado com um método de balanceamento de carga de rodízio, um TTL de 30 segundos, protocolo de monitoramento HTTP, monitorando a porta 80 e com o caminho especificado.

### Exemplo 2: reordenar pontos de extremidade para a ordem de failover desejada
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

Este exemplo reordena os pontos de extremidade adicionados ao MyProfile para a ordem de failover desejada.

O primeiro comando obtém o objeto de perfil do Gerenciador de tráfego chamado MyProfile e armazena o objeto na variável $Profile.

O segundo comando re-ordena os pontos de extremidade da matriz de pontos de extremidade para a ordem em que o failover deve ocorrer.

O último comando atualiza o perfil do Gerenciador de tráfego armazenado em $Profile com o novo pedido de ponto de extremidade.

## OS

### -DomainName
Especifica o nome de domínio do perfil do Gerenciador de tráfego.
Deve ser um subdomínio de trafficmanager.net.

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

### -LoadBalancingMethod
Especifica o método de balanceamento de carga a ser usado para distribuir a conexão.
Os valores válidos são: 

- Execução
- Falhas
- RoundRobin

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

### -MonitorPort
Especifica a porta usada para monitorar a integridade do ponto de extremidade.
Os valores válidos são valores inteiros superiores a 0 e menores que ou iguais a 65.535.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Especifica o protocolo a ser usado para monitorar a integridade do ponto de extremidade.
Os valores válidos são: 

- Http

- Https

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

### -MonitorRelativePath
Especifica o caminho relativo ao nome do domínio do ponto de extremidade para investigar o estado de integridade.
O caminho deve atender às seguintes restrições: 

- O caminho deve ter entre 1 e 1000 caracteres.

- Ele deve começar com uma barra de encaminhamento/.

- Ele deve conter nenhum elemento XML \<\> .

- Ele deve conter duas barras,//.

- Ele deve conter nenhum caractere de escape HTML inválidos.
Por exemplo,% XY.

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

### -Nome
Especifica o nome do perfil do Gerenciador de tráfego a ser criado.

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

### -TTL
Especifica o tempo de vida útil (TTL) do DNS que informa os resolvedores DNS locais por quanto tempo armazenar em cache as entradas DNS.
Os valores válidos são inteiros de 30 a 999.999.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
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
Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego.

## INFORMA

## LINKS RELACIONADOS

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


