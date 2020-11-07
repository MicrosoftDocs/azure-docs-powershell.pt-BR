---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946376"
---
# Add-AzureTrafficManagerEndpoint

## Sinopse
Adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego.

## SYNTAX

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureTrafficManagerEndpoint** adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego do Microsoft Azure.
Depois de adicionar um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.
Esse cmdlet se conecta ao Azure para salvar suas alterações.

## EXEMPLOS

### Exemplo 1: adicionar um ponto de extremidade a um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.

O segundo comando adiciona um ponto de extremidade ao perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.
O ponto de extremidade tem o nome de domínio Contoso02App.couldapp.net.
O comando também especifica se ele está habilitado e seu tipo.
O comando passa o objeto de perfil para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.

### Exemplo 2: adicionar um ponto de extremidade com local e peso especificado
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Esse comando adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego.
O ponto de extremidade tem o nome de domínio Contoso02App.couldapp.net.
O comando também especifica se ele está habilitado e seu tipo.
O comando também especifica a espessura e o local da empresa.
O comando passa o objeto de perfil para **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.

## OS

### -DomainName
Especifica o nome de domínio do ponto de extremidade a ser adicionado.

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
Os valores possíveis são os nomes de região do Azure, conforme listado em https://azure.microsoft.com/regions/ .

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Especifica o objeto de perfil do Gerenciador de tráfego ao qual adicionar o ponto de extremidade.

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

Required: True
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

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


