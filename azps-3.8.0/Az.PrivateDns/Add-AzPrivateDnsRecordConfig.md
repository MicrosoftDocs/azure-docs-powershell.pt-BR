---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: a6150f6f54db57abbcd643c99729d41254db7d27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940900"
---
# Add-AzPrivateDnsRecordConfig

## Sinopse
Adiciona um registro DNS privado a um objeto de conjunto de registros local.

## SYNTAX

### A (padrão)
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AAAA
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PTR
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LOCALIZADO
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CNAME
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Add-AzPrivateDnsRecordConfig adiciona um registro DNS (sistema de nomes de domínio) privado a um objeto RecordSet. O objeto RecordSet é um objeto offline, e as alterações feitas a ele não alteram as respostas DNS particulares até que você execute o cmdlet Set-AzPrivateDnsRecordSet para persistir a alteração no serviço DNS privado do Microsoft Azure. Os registros SOA são criados quando uma zona DNS privada é criada e são removidas quando a zona DNS privada é excluída. Você não pode adicionar ou remover registros SOA, mas pode editá-los. Você pode passar o objeto RecordSet para esse cmdlet como um parâmetro ou usando o operador pipeline.

## EXEMPLOS

### Exemplo 1: adicionar um registro a a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro a a um conjunto de registros existente.

### Exemplo 2: adicionar um registro AAAA a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro AAAAA a um conjunto de registros existente.

### Exemplo 3: adicionar um registro CNAME a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro CNAME a um conjunto de registros existente.

### Exemplo 4: adicionar um registro MX a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro MX a um conjunto de registros existente.

### Exemplo 5: adicionar um registro PTR a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro PTR a um conjunto de registros existente.

### Exemplo 6: adicionar um registro SRV a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro SRV a um conjunto de registros existente.

### Exemplo 7: adicionar um registro TXT a um conjunto de registros
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

Este exemplo adiciona um registro TXT a um conjunto de registros existente.

## OS

### -CNAME
O nome canônico do registro CNAME a ser adicionado.
Não deve ser relativo ao nome da zona.
Não deve ter um ponto de terminação

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exchange
O host do mail Exchange para o registro MX a ser adicionado.
Não deve ser relativo ao nome da zona.
Não deve ter um ponto de terminação

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv4Address
O endereço IPv4 do registro a a ser adicionado.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv6Address
O endereço IPv6 para o registro AAAA a ser adicionado.

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Porta
O número da porta do registro SRV a ser adicionado.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Preferência
O valor de preferência para o registro MX a ser adicionado.

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
O registro SRV do valor de prioridade a ser adicionado.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ptrdname
O host de destino para o registro PTR a ser adicionado.
Não deve ser relativo ao nome da zona.
Não deve ter um ponto de terminação

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
O conjunto de registros no qual adicionar o registro.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Destino
O host de destino para o registro SRV a ser adicionado.
Não deve ser relativo ao nome da zona.
Não deve ter um ponto de terminação

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valor
O valor de texto do registro TXT a ser adicionado.

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
O valor de peso para o registro SRV a ser adicionado.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet

## EXIBE

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet

## INFORMA

## LINKS RELACIONADOS
