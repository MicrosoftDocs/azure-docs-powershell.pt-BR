---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889125"
---
# <span data-ttu-id="7616f-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="7616f-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="7616f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7616f-102">SYNOPSIS</span></span>
<span data-ttu-id="7616f-103">Obter comunicações de tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="7616f-103">Get support ticket communications.</span></span>

## <span data-ttu-id="7616f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7616f-104">SYNTAX</span></span>

### <span data-ttu-id="7616f-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7616f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="7616f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7616f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="7616f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7616f-107">DESCRIPTION</span></span>
<span data-ttu-id="7616f-108">Obtém comunicações para um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="7616f-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="7616f-109">Ele recuperará todas as comunicações de um tíquete se você não especificar outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7616f-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="7616f-110">Você também pode filtrar as comunicações por CreatedDate ou CommunicationType usando o parâmetro Filter.</span><span class="sxs-lookup"><span data-stu-id="7616f-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="7616f-111">Aqui estão alguns exemplos de valores de filtro que você pode especificar.</span><span class="sxs-lookup"><span data-stu-id="7616f-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="7616f-112">Cenário</span><span class="sxs-lookup"><span data-stu-id="7616f-112">Scenario</span></span>                                                        | <span data-ttu-id="7616f-113">Filter</span><span class="sxs-lookup"><span data-stu-id="7616f-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7616f-114">Obter comunicações da Web</span><span class="sxs-lookup"><span data-stu-id="7616f-114">Get Web communications</span></span>                                          | <span data-ttu-id="7616f-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="7616f-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="7616f-116">Obter comunicações telefônicas</span><span class="sxs-lookup"><span data-stu-id="7616f-116">Get Phone communications</span></span>                                        | <span data-ttu-id="7616f-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="7616f-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="7616f-118">Obter comunicações que foram criadas em ou após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7616f-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="7616f-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7616f-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="7616f-120">Obter comunicações que foram criadas após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7616f-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="7616f-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7616f-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="7616f-122">Obtém comunicações da Web criadas após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7616f-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="7616f-123">"CreatedDate gt 2019-12-20 e CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="7616f-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="7616f-124">Este cmdlet dá suporte à paja por meio dos parâmetros First e Skip.</span><span class="sxs-lookup"><span data-stu-id="7616f-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="7616f-125">Você também pode recuperar uma comunicação de tíquete de suporte único especificando o nome da comunicação.</span><span class="sxs-lookup"><span data-stu-id="7616f-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="7616f-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7616f-126">EXAMPLES</span></span>

### <span data-ttu-id="7616f-127">Exemplo 1: Recuperar todas as comunicações para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="7616f-128">Exemplo 2: Recuperar uma única comunicação pelo nome de um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="7616f-129">Exemplo 3: Recuperar as duas primeiras comunicações para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="7616f-130">Exemplo 4: recuperar as próximas 2 comunicações após ignorar as duas primeiras comunicações para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="7616f-131">Exemplo 5: Recuperar todas as comunicações da Web para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="7616f-132">Exemplo 6: Recuperar todas as comunicações criadas em ou após 20 de dezembro de 2019 para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="7616f-133">Exemplo 7: Recuperar todas as comunicações da Web criadas em ou após 20 de dezembro de 2019 para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="7616f-134">Exemplo 8: recuperar todas as comunicações para um tíquete de suporte canalização do objeto ticket de suporte</span><span class="sxs-lookup"><span data-stu-id="7616f-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="7616f-135">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7616f-135">PARAMETERS</span></span>

### <span data-ttu-id="7616f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7616f-136">-DefaultProfile</span></span>
<span data-ttu-id="7616f-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7616f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7616f-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="7616f-138">-Filter</span></span>
<span data-ttu-id="7616f-139">Filtro a ser aplicado aos resultados deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7616f-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7616f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="7616f-140">-Name</span></span>
<span data-ttu-id="7616f-141">Nome da comunicação.</span><span class="sxs-lookup"><span data-stu-id="7616f-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7616f-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="7616f-142">-SupportTicketName</span></span>
<span data-ttu-id="7616f-143">Nome do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="7616f-143">Support ticket name.</span></span>

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

### <span data-ttu-id="7616f-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="7616f-144">-SupportTicketObject</span></span>
<span data-ttu-id="7616f-145">Objeto Ticket de suporte.</span><span class="sxs-lookup"><span data-stu-id="7616f-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7616f-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7616f-146">-IncludeTotalCount</span></span>
<span data-ttu-id="7616f-147">Relata o número total de objetos no conjunto de dados (um inteiro) seguido pelos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="7616f-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="7616f-148">Se o cmdlet não puder determinar a contagem total, ele exibirá "Contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="7616f-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="7616f-149">O inteiro tem uma propriedade Accuracy que indica a confiabilidade do valor total da contagem.</span><span class="sxs-lookup"><span data-stu-id="7616f-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="7616f-150">O valor de Precisão varia de 0,0 a 1,0 onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa cada vez mais confiável.</span><span class="sxs-lookup"><span data-stu-id="7616f-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="7616f-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="7616f-151">-Skip</span></span>
<span data-ttu-id="7616f-152">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="7616f-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7616f-153">Insira o número de objetos a ignorar.</span><span class="sxs-lookup"><span data-stu-id="7616f-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="7616f-154">-First</span><span class="sxs-lookup"><span data-stu-id="7616f-154">-First</span></span>
<span data-ttu-id="7616f-155">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="7616f-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7616f-156">Insira o número de objetos a obter.</span><span class="sxs-lookup"><span data-stu-id="7616f-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="7616f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7616f-157">CommonParameters</span></span>
<span data-ttu-id="7616f-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7616f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7616f-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7616f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7616f-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7616f-160">INPUTS</span></span>

### <span data-ttu-id="7616f-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7616f-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7616f-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7616f-162">OUTPUTS</span></span>

### <span data-ttu-id="7616f-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="7616f-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="7616f-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="7616f-164">NOTES</span></span>

## <span data-ttu-id="7616f-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7616f-165">RELATED LINKS</span></span>
