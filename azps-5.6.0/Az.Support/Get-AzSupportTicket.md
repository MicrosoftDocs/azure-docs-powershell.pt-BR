---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892687"
---
# <span data-ttu-id="cdc11-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="cdc11-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="cdc11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc11-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc11-103">Obter tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="cdc11-103">Get support tickets.</span></span>

## <span data-ttu-id="cdc11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cdc11-104">SYNTAX</span></span>

### <span data-ttu-id="cdc11-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cdc11-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cdc11-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdc11-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cdc11-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cdc11-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc11-108">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="cdc11-108">Gets the list of support tickets.</span></span> <span data-ttu-id="cdc11-109">Ele recuperará todos os tíquetes de suporte se você não especificar parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cdc11-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="cdc11-110">Você também pode filtrar os tíquetes de suporte por Status ou CreatedDate usando o parâmetro Filter.</span><span class="sxs-lookup"><span data-stu-id="cdc11-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="cdc11-111">Aqui estão alguns exemplos de valores de filtro que você pode especificar.</span><span class="sxs-lookup"><span data-stu-id="cdc11-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="cdc11-112">Cenário</span><span class="sxs-lookup"><span data-stu-id="cdc11-112">Scenario</span></span>                                                         | <span data-ttu-id="cdc11-113">Filter</span><span class="sxs-lookup"><span data-stu-id="cdc11-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="cdc11-114">Obter tíquetes que estão em estado aberto</span><span class="sxs-lookup"><span data-stu-id="cdc11-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="cdc11-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="cdc11-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="cdc11-116">Obter tíquetes que estão em estado fechado</span><span class="sxs-lookup"><span data-stu-id="cdc11-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="cdc11-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="cdc11-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="cdc11-118">Obter tíquetes criados em ou após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="cdc11-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="cdc11-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="cdc11-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="cdc11-120">Obter tíquetes criados após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="cdc11-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="cdc11-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="cdc11-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="cdc11-122">Obtém tíquetes criados após 20 de dezembro de 2019 que estão em estado aberto</span><span class="sxs-lookup"><span data-stu-id="cdc11-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="cdc11-123">"CreatedDate gt 2019-12-20 e Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="cdc11-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="cdc11-124">Este cmdlet dá suporte à paja por meio dos parâmetros First e Skip.</span><span class="sxs-lookup"><span data-stu-id="cdc11-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="cdc11-125">Você também pode recuperar um único tíquete de suporte especificando o nome do tíquete.</span><span class="sxs-lookup"><span data-stu-id="cdc11-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="cdc11-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdc11-126">EXAMPLES</span></span>

### <span data-ttu-id="cdc11-127">Exemplo 1: Obter os dois primeiros tíquetes</span><span class="sxs-lookup"><span data-stu-id="cdc11-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="cdc11-128">Exemplo 2: Obter os dois primeiros tíquetes após ignorar os dois primeiros</span><span class="sxs-lookup"><span data-stu-id="cdc11-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="cdc11-129">Exemplo 3: Obter um tíquete de suporte pelo nome</span><span class="sxs-lookup"><span data-stu-id="cdc11-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="cdc11-130">Exemplo 4: Obter os dois primeiros tíquetes de suporte filtrados por status</span><span class="sxs-lookup"><span data-stu-id="cdc11-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="cdc11-131">Exemplo 5: Obter todos os tíquetes de suporte que estão no estado Open e criados após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="cdc11-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="cdc11-132">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cdc11-132">PARAMETERS</span></span>

### <span data-ttu-id="cdc11-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc11-133">-DefaultProfile</span></span>
<span data-ttu-id="cdc11-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc11-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc11-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="cdc11-135">-Filter</span></span>
<span data-ttu-id="cdc11-136">Filtro a ser aplicado aos resultados deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdc11-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="cdc11-137">-Name</span><span class="sxs-lookup"><span data-stu-id="cdc11-137">-Name</span></span>
<span data-ttu-id="cdc11-138">Nome do tíquete de suporte que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="cdc11-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cdc11-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cdc11-139">-IncludeTotalCount</span></span>
<span data-ttu-id="cdc11-140">Relata o número total de objetos no conjunto de dados (um inteiro) seguido pelos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="cdc11-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="cdc11-141">Se o cmdlet não puder determinar a contagem total, ele exibirá "Contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="cdc11-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="cdc11-142">O inteiro tem uma propriedade Accuracy que indica a confiabilidade do valor total da contagem.</span><span class="sxs-lookup"><span data-stu-id="cdc11-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="cdc11-143">O valor de Precisão varia de 0,0 a 1,0 onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa cada vez mais confiável.</span><span class="sxs-lookup"><span data-stu-id="cdc11-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="cdc11-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="cdc11-144">-Skip</span></span>
<span data-ttu-id="cdc11-145">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="cdc11-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="cdc11-146">Insira o número de objetos a ignorar.</span><span class="sxs-lookup"><span data-stu-id="cdc11-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="cdc11-147">-First</span><span class="sxs-lookup"><span data-stu-id="cdc11-147">-First</span></span>
<span data-ttu-id="cdc11-148">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="cdc11-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="cdc11-149">Insira o número de objetos a obter.</span><span class="sxs-lookup"><span data-stu-id="cdc11-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="cdc11-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc11-150">CommonParameters</span></span>
<span data-ttu-id="cdc11-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc11-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc11-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdc11-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc11-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc11-153">INPUTS</span></span>

### <span data-ttu-id="cdc11-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cdc11-154">None</span></span>

## <span data-ttu-id="cdc11-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cdc11-155">OUTPUTS</span></span>

### <span data-ttu-id="cdc11-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="cdc11-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="cdc11-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="cdc11-157">NOTES</span></span>

## <span data-ttu-id="cdc11-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdc11-158">RELATED LINKS</span></span>
