---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112806"
---
# New-AzPublicIpAddress

## Sinopse
Cria um endereço IP público.

## Sintaxe

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzPublicIpAddress** cria um endereço IP público.

## Exemplos

### Exemplo 1: Criar um novo endereço IP público
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso. Um endereço IP público é imediatamente alocado a esse recurso, pois o -AllocationMethod é especificado como "Estático". Se for especificado como "Dinâmico", um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como um VM ou balanceador de carga).

### Exemplo 2: Criar um endereço IP público com um FQDN reverso
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

Esse comando cria um novo recurso de endereço IP público. Com o parâmetro -ReverseFqdn, o Azure cria um registro DNS PTR (busca reversa) para o endereço IP público atribuído a esse recurso, apontando para o $customFqdn especificado no comando. Como um pré-requisito, o $customFqdn (digamos webapp.contoso.com) deve ter um registro CNAME DNS (forward-lookup) apontando para $dnsPrefix.$location.cloudapp.azure.com.

### Exemplo 3: Criar um novo endereço IP público com IpTag
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso. Um endereço IP público é imediatamente alocado a esse recurso, pois o -AllocationMethod é especificado como "Estático". Se for especificado como "Dinâmico", um endereço IP público será alocado somente quando você iniciar (ou criar) o recurso associado (como um VM ou balanceador de carga). Um Iptag é usado para específicas as Marcas associadas ao recurso. O Iptag pode ser especificado usando New-AzPublicIpTag e passado como entrada por -IpTags.

### Exemplo 4: Criar um novo endereço IP público a partir de um Prefixo
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

Esse comando cria um novo recurso de endereço IP público. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso. Um endereço IP público é imediatamente atribuído a esse recurso a partir do publicIpPrefix especificado.
Essa opção só tem suporte para a SKU 'Padrão' e a Alocação EstáticaMethod.

### Exemplo 5: Criar um novo endereço IP público global
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

Esse comando cria um novo recurso de endereço IP público global. Um registro DNS é criado para $dnsPrefix.$location.cloudapp.azure.com apontando para o endereço IP público desse recurso. Um endereço IP público global é imediatamente atribuído a esse recurso.
Essa opção só tem suporte para a SKU 'Padrão' e a Alocação EstáticaMethod.

## Parâmetros

### -AllocationMethod
Especifica o método com o qual atribuir o endereço IP público.
Os valores aceitáveis para este parâmetro são: Estático ou Dinâmico.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
Executar cmdlet em segundo plano

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -DomainNameLabel
Especifica o nome DNS relativo de um endereço IP público.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Forçar
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Especifica o tempo ocioso em minutos.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
Especifica a versão do endereço IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Lista IpTag.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica a região na qual criar um endereço IP público.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do endereço IP público que este cmdlet cria.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpPrefix
Especifica a PSPublicIpPrefix a partir da qual o endereço IP público deve ser alocado.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual se cria um endereço IP público.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseFqdn
Especifica um FQDN (nome de domínio totalmente qualificado) reverso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
O nome SKU do IP público.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pares de valor-chave na forma de uma tabela hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
A camada de SKU ip pública.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zona
Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]

### Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix

### System.Int32

### System.String[]

### System.Collections.Hashtable

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## Notas

## LINKS RELACIONADOS

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
