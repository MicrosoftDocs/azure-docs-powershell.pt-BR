---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283956"
---
# <span data-ttu-id="7db39-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7db39-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="7db39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7db39-102">SYNOPSIS</span></span>
<span data-ttu-id="7db39-103">Obter tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="7db39-103">Get support tickets.</span></span>

## <span data-ttu-id="7db39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7db39-104">SYNTAX</span></span>

### <span data-ttu-id="7db39-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7db39-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7db39-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db39-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7db39-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7db39-107">DESCRIPTION</span></span>
<span data-ttu-id="7db39-108">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="7db39-108">Gets the list of support tickets.</span></span> <span data-ttu-id="7db39-109">Ele recuperará todos os tíquetes de suporte se você não especificar nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7db39-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="7db39-110">Você também pode filtrar os tíquetes de suporte por status ou CreatedDate usando o parâmetro Filter.</span><span class="sxs-lookup"><span data-stu-id="7db39-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="7db39-111">Aqui estão alguns exemplos de valores de filtro que você pode especificar.</span><span class="sxs-lookup"><span data-stu-id="7db39-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="7db39-112">Situações</span><span class="sxs-lookup"><span data-stu-id="7db39-112">Scenario</span></span>                                                         | <span data-ttu-id="7db39-113">Filtre</span><span class="sxs-lookup"><span data-stu-id="7db39-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="7db39-114">Obter tíquetes que estejam em estado aberto</span><span class="sxs-lookup"><span data-stu-id="7db39-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="7db39-115">"Open status eq ' Open '"</span><span class="sxs-lookup"><span data-stu-id="7db39-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="7db39-116">Obter tíquetes que estejam em estado fechado</span><span class="sxs-lookup"><span data-stu-id="7db39-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="7db39-117">"Status eq" fechado ""</span><span class="sxs-lookup"><span data-stu-id="7db39-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="7db39-118">Obter ingressos que foram criados em ou após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7db39-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="7db39-119">"CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7db39-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="7db39-120">Obter ingressos que foram criados após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7db39-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="7db39-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7db39-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="7db39-122">Obtém ingressos criados após 20 de dezembro de 2019 que estão em estado aberto</span><span class="sxs-lookup"><span data-stu-id="7db39-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="7db39-123">"CreatedDate gt 2019-12-20 e status eq ' Open '"</span><span class="sxs-lookup"><span data-stu-id="7db39-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="7db39-124">Esse cmdlet dá suporte à paginação pelos parâmetros First e Skip.</span><span class="sxs-lookup"><span data-stu-id="7db39-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="7db39-125">Você também pode recuperar um único tíquete de suporte especificando o nome do tíquete.</span><span class="sxs-lookup"><span data-stu-id="7db39-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="7db39-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7db39-126">EXAMPLES</span></span>

### <span data-ttu-id="7db39-127">Exemplo 1: obter os primeiros 2 bilhetes</span><span class="sxs-lookup"><span data-stu-id="7db39-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7db39-128">Exemplo 2: obter primeiros 2 bilhetes após ignorar os 2 primeiros</span><span class="sxs-lookup"><span data-stu-id="7db39-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7db39-129">Exemplo 3: obter um tíquete de suporte por nome</span><span class="sxs-lookup"><span data-stu-id="7db39-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7db39-130">Exemplo 4: obter os primeiros 2 tíquetes de suporte filtrados por status</span><span class="sxs-lookup"><span data-stu-id="7db39-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7db39-131">Exemplo 5: obter todos os ingressos de suporte que estiverem em estado aberto e criados após dez de 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7db39-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="7db39-132">OS</span><span class="sxs-lookup"><span data-stu-id="7db39-132">PARAMETERS</span></span>

### <span data-ttu-id="7db39-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db39-133">-DefaultProfile</span></span>
<span data-ttu-id="7db39-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7db39-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db39-135">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7db39-135">-Filter</span></span>
<span data-ttu-id="7db39-136">Filtro a ser aplicado aos resultados deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7db39-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="7db39-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="7db39-137">-Name</span></span>
<span data-ttu-id="7db39-138">Nome da permissão de suporte que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7db39-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7db39-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7db39-139">-IncludeTotalCount</span></span>
<span data-ttu-id="7db39-140">Relata o número total de objetos no conjunto de dados (um número inteiro) seguido pelos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="7db39-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="7db39-141">Se o cmdlet não puder determinar a contagem total, ele exibirá "contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="7db39-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="7db39-142">O inteiro tem uma propriedade exactidão que indica a confiabilidade do valor total de contagem.</span><span class="sxs-lookup"><span data-stu-id="7db39-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="7db39-143">O valor de precisão varia de 0,0 a 1,0, onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa mais confiável.</span><span class="sxs-lookup"><span data-stu-id="7db39-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="7db39-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="7db39-144">-Skip</span></span>
<span data-ttu-id="7db39-145">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="7db39-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7db39-146">Digite o número de objetos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="7db39-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="7db39-147">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="7db39-147">-First</span></span>
<span data-ttu-id="7db39-148">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="7db39-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7db39-149">Digite o número de objetos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="7db39-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="7db39-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db39-150">CommonParameters</span></span>
<span data-ttu-id="7db39-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db39-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db39-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7db39-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db39-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7db39-153">INPUTS</span></span>

### <span data-ttu-id="7db39-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7db39-154">None</span></span>

## <span data-ttu-id="7db39-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7db39-155">OUTPUTS</span></span>

### <span data-ttu-id="7db39-156">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7db39-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7db39-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7db39-157">NOTES</span></span>

## <span data-ttu-id="7db39-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7db39-158">RELATED LINKS</span></span>
