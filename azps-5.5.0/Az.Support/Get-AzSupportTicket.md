---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112426"
---
# Get-AzSupportTicket

## Sinopse
Obter tíquetes de suporte.

## Sintaxe

### ListParameterSet (Padrão)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## Descrição
Obtém a lista de tíquetes de suporte. Ele recuperará todos os tíquetes de suporte se você não especificar parâmetros. Você também pode filtrar os tíquetes de suporte por Status ou Data Criada usando o parâmetro Filtro. Aqui estão alguns exemplos de valores de filtro que você pode especificar.

| Cenário                                                         | Filtro                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Obter tíquetes que estão em estado aberto                               | "Status eq 'Abrir'"                               |
| Obter tíquetes que estão no estado fechado                             | "Status eq 'Closed'"                             |
| Obter tíquetes que foram criados em ou após 20 de dezembro de 2019         | "CreatedDate ge 2019-12-20"                      |
| Obter tíquetes que foram criados após 20 de dezembro de 2019               | "CreatedDate gt 2019-12-20"                      |
| Recebe tíquetes criados após 20 de dezembro de 2019 que estão em estado aberto | "CreatedDate gt 2019-12-20 e Status eq 'Open'" |


Esse cmdlet dá suporte à pajação por meio dos parâmetros First e Skip.

Você também pode recuperar um único tíquete de suporte especificando o nome do tíquete. 

## Exemplos

### Exemplo 1: Obter os dois primeiros tíquetes
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exemplo 2: Obter os dois primeiros tíquetes depois de ignorar os dois primeiros
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exemplo 3: Obter um tíquete de suporte por nome
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Exemplo 4: Obter os dois primeiros tíquetes de suporte filtrados por status
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exemplo 5: Obter todos os tíquetes de suporte que estão no estado Aberto e criados após 20 de dezembro de 2019
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Filtro
Filtro a ser aplicado aos resultados deste cmdlet.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do tíquete de suporte que este cmdlet recebe.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Relata o número total de objetos no conjunto de dados (um inteiro) seguido dos objetos selecionados.
Se o cmdlet não puder determinar a contagem total, ele exibirá "Contagem total desconhecida". O inteiro tem uma propriedade Precisão que indica a confiabilidade do valor da contagem total.
O valor da Precisão varia de 0,0 a 1,0 onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa cada vez mais confiável.

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

### -Ignorar
Ignora o número especificado de objetos e obtém os objetos restantes.
Insira o número de objetos a ignorar.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Obtém apenas o número especificado de objetos.
Insira o número de objetos a obter.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## Notas

## LINKS RELACIONADOS
