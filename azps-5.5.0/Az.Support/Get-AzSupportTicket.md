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
# <span data-ttu-id="f8b05-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f8b05-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="f8b05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b05-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b05-103">Obter tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="f8b05-103">Get support tickets.</span></span>

## <span data-ttu-id="f8b05-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8b05-104">SYNTAX</span></span>

### <span data-ttu-id="f8b05-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f8b05-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8b05-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b05-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f8b05-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8b05-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b05-108">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="f8b05-108">Gets the list of support tickets.</span></span> <span data-ttu-id="f8b05-109">Ele recuperará todos os tíquetes de suporte se você não especificar parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8b05-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="f8b05-110">Você também pode filtrar os tíquetes de suporte por Status ou Data Criada usando o parâmetro Filtro.</span><span class="sxs-lookup"><span data-stu-id="f8b05-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="f8b05-111">Aqui estão alguns exemplos de valores de filtro que você pode especificar.</span><span class="sxs-lookup"><span data-stu-id="f8b05-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="f8b05-112">Cenário</span><span class="sxs-lookup"><span data-stu-id="f8b05-112">Scenario</span></span>                                                         | <span data-ttu-id="f8b05-113">Filtro</span><span class="sxs-lookup"><span data-stu-id="f8b05-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="f8b05-114">Obter tíquetes que estão em estado aberto</span><span class="sxs-lookup"><span data-stu-id="f8b05-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="f8b05-115">"Status eq 'Abrir'"</span><span class="sxs-lookup"><span data-stu-id="f8b05-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="f8b05-116">Obter tíquetes que estão no estado fechado</span><span class="sxs-lookup"><span data-stu-id="f8b05-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="f8b05-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="f8b05-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="f8b05-118">Obter tíquetes que foram criados em ou após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f8b05-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="f8b05-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="f8b05-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="f8b05-120">Obter tíquetes que foram criados após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f8b05-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="f8b05-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="f8b05-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="f8b05-122">Recebe tíquetes criados após 20 de dezembro de 2019 que estão em estado aberto</span><span class="sxs-lookup"><span data-stu-id="f8b05-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="f8b05-123">"CreatedDate gt 2019-12-20 e Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="f8b05-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="f8b05-124">Esse cmdlet dá suporte à pajação por meio dos parâmetros First e Skip.</span><span class="sxs-lookup"><span data-stu-id="f8b05-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="f8b05-125">Você também pode recuperar um único tíquete de suporte especificando o nome do tíquete.</span><span class="sxs-lookup"><span data-stu-id="f8b05-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="f8b05-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8b05-126">EXAMPLES</span></span>

### <span data-ttu-id="f8b05-127">Exemplo 1: Obter os dois primeiros tíquetes</span><span class="sxs-lookup"><span data-stu-id="f8b05-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f8b05-128">Exemplo 2: Obter os dois primeiros tíquetes depois de ignorar os dois primeiros</span><span class="sxs-lookup"><span data-stu-id="f8b05-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f8b05-129">Exemplo 3: Obter um tíquete de suporte por nome</span><span class="sxs-lookup"><span data-stu-id="f8b05-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f8b05-130">Exemplo 4: Obter os dois primeiros tíquetes de suporte filtrados por status</span><span class="sxs-lookup"><span data-stu-id="f8b05-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="f8b05-131">Exemplo 5: Obter todos os tíquetes de suporte que estão no estado Aberto e criados após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f8b05-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="f8b05-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8b05-132">PARAMETERS</span></span>

### <span data-ttu-id="f8b05-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b05-133">-DefaultProfile</span></span>
<span data-ttu-id="f8b05-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b05-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b05-135">-Filtro</span><span class="sxs-lookup"><span data-stu-id="f8b05-135">-Filter</span></span>
<span data-ttu-id="f8b05-136">Filtro a ser aplicado aos resultados deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8b05-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="f8b05-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b05-137">-Name</span></span>
<span data-ttu-id="f8b05-138">Nome do tíquete de suporte que este cmdlet recebe.</span><span class="sxs-lookup"><span data-stu-id="f8b05-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8b05-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f8b05-139">-IncludeTotalCount</span></span>
<span data-ttu-id="f8b05-140">Relata o número total de objetos no conjunto de dados (um inteiro) seguido dos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="f8b05-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="f8b05-141">Se o cmdlet não puder determinar a contagem total, ele exibirá "Contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="f8b05-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="f8b05-142">O inteiro tem uma propriedade Precisão que indica a confiabilidade do valor da contagem total.</span><span class="sxs-lookup"><span data-stu-id="f8b05-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="f8b05-143">O valor da Precisão varia de 0,0 a 1,0 onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa cada vez mais confiável.</span><span class="sxs-lookup"><span data-stu-id="f8b05-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="f8b05-144">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="f8b05-144">-Skip</span></span>
<span data-ttu-id="f8b05-145">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="f8b05-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="f8b05-146">Insira o número de objetos a ignorar.</span><span class="sxs-lookup"><span data-stu-id="f8b05-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="f8b05-147">-First</span><span class="sxs-lookup"><span data-stu-id="f8b05-147">-First</span></span>
<span data-ttu-id="f8b05-148">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="f8b05-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="f8b05-149">Insira o número de objetos a obter.</span><span class="sxs-lookup"><span data-stu-id="f8b05-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="f8b05-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b05-150">CommonParameters</span></span>
<span data-ttu-id="f8b05-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b05-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b05-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b05-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b05-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="f8b05-153">INPUTS</span></span>

### <span data-ttu-id="f8b05-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f8b05-154">None</span></span>

## <span data-ttu-id="f8b05-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="f8b05-155">OUTPUTS</span></span>

### <span data-ttu-id="f8b05-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="f8b05-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="f8b05-157">Notas</span><span class="sxs-lookup"><span data-stu-id="f8b05-157">NOTES</span></span>

## <span data-ttu-id="f8b05-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b05-158">RELATED LINKS</span></span>
