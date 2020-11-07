---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946092"
---
# Remove-AzureTrafficManagerEndpoint

## Sinopse
Remove um ponto de extremidade de um perfil do Gerenciador de tráfego.

## SYNTAX

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureTrafficManagerEndpoint** remove um ponto de extremidade de um perfil do Gerenciador de tráfego do Microsoft Azure.
Depois de remover um ponto de extremidade, passe o resultado para o cmdlet **set-AzureTrafficManagerProfile** usando o operador pipeline.
Esse cmdlet se conecta ao Azure para salvar suas alterações.

## EXEMPLOS

### Exemplo 1: remover um ponto de extremidade de um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

O primeiro comando usa o cmdlet **Get-AzureTrafficManagerProfile** para obter o perfil chamado ContosoProfile e, em seguida, armazena-o na variável $TrafficManagerProfile.

O segundo comando Remove um ponto de extremidade que tem o nome de domínio Contoso02App.cloudapp.net do perfil do Gerenciador de tráfego que está armazenado em $TrafficManagerProfile.
O comando passa o objeto de perfil para o cmdlet **set-AzureTrafficManagerProfile** para se conectar ao Azure para salvar suas alterações.

## OS

### -DomainName
Especifica o nome de domínio do ponto de extremidade a ser removido.

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

### -Force
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

### -TrafficManagerProfile
Especifica o objeto de perfil do Gerenciador de tráfego do qual o ponto de extremidade será removido.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego, que contém informações sobre o perfil atualizado.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


