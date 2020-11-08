---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113172"
---
# <span data-ttu-id="19ed8-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="19ed8-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="19ed8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="19ed8-103">Obter suporte a comunicações de permissão.</span><span class="sxs-lookup"><span data-stu-id="19ed8-103">Get support ticket communications.</span></span>

## <span data-ttu-id="19ed8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19ed8-104">SYNTAX</span></span>

### <span data-ttu-id="19ed8-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="19ed8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="19ed8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19ed8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="19ed8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="19ed8-108">Obtém comunicações para um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="19ed8-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="19ed8-109">Ele recuperará todas as comunicações para um tíquete se você não especificar outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="19ed8-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="19ed8-110">Você também pode filtrar as comunicações por CreatedDate ou Communicationtype usando o parâmetro Filter.</span><span class="sxs-lookup"><span data-stu-id="19ed8-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="19ed8-111">Aqui estão alguns exemplos de valores de filtro que você pode especificar.</span><span class="sxs-lookup"><span data-stu-id="19ed8-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="19ed8-112">Situações</span><span class="sxs-lookup"><span data-stu-id="19ed8-112">Scenario</span></span>                                                        | <span data-ttu-id="19ed8-113">Filtre</span><span class="sxs-lookup"><span data-stu-id="19ed8-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="19ed8-114">Obter comunicações da Web</span><span class="sxs-lookup"><span data-stu-id="19ed8-114">Get Web communications</span></span>                                          | <span data-ttu-id="19ed8-115">"Communicationtype EQ" Web ""</span><span class="sxs-lookup"><span data-stu-id="19ed8-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="19ed8-116">Obter comunicações por telefone</span><span class="sxs-lookup"><span data-stu-id="19ed8-116">Get Phone communications</span></span>                                        | <span data-ttu-id="19ed8-117">"Communicationtype EQ" Phone ""</span><span class="sxs-lookup"><span data-stu-id="19ed8-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="19ed8-118">Obter comunicações criadas em ou após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="19ed8-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="19ed8-119">"CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="19ed8-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="19ed8-120">Obter comunicações criadas após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="19ed8-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="19ed8-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="19ed8-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="19ed8-122">A comunicação da Web é criada após 20 de dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="19ed8-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="19ed8-123">"CreatedDate gt 2019-12-20 e Communicationtype EQ ' Web '"</span><span class="sxs-lookup"><span data-stu-id="19ed8-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="19ed8-124">Esse cmdlet dá suporte à paginação pelos parâmetros First e Skip.</span><span class="sxs-lookup"><span data-stu-id="19ed8-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="19ed8-125">Você também pode recuperar uma única comunicação de tíquete de suporte especificando o nome de comunicação.</span><span class="sxs-lookup"><span data-stu-id="19ed8-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="19ed8-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19ed8-126">EXAMPLES</span></span>

### <span data-ttu-id="19ed8-127">Exemplo 1: recuperar todas as comunicações para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="19ed8-128">Exemplo 2: recuperar uma única comunicação por ele é o nome de um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="19ed8-129">Exemplo 3: recuperar as primeiras 2 comunicações para obter um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="19ed8-130">Exemplo 4: recuperar as próximas 2 comunicações após ignorar as 2 primeiras comunicações para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="19ed8-131">Exemplo 5: recuperar todas as comunicações da Web para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="19ed8-132">Exemplo 6: recuperar todas as comunicações criadas em ou após dez de 20 de dezembro de 2019 para um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="19ed8-133">Exemplo 7: recuperar todas as comunicações da Web criadas em ou após dez de 20 de dezembro de 2019 para obter um tíquete de suporte</span><span class="sxs-lookup"><span data-stu-id="19ed8-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="19ed8-134">Exemplo 8: recuperar todas as comunicações para um tíquete de suporte por meio do objeto de tíquete de suporte de tubulação</span><span class="sxs-lookup"><span data-stu-id="19ed8-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="19ed8-135">OS</span><span class="sxs-lookup"><span data-stu-id="19ed8-135">PARAMETERS</span></span>

### <span data-ttu-id="19ed8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ed8-136">-DefaultProfile</span></span>
<span data-ttu-id="19ed8-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19ed8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ed8-138">-Filtro</span><span class="sxs-lookup"><span data-stu-id="19ed8-138">-Filter</span></span>
<span data-ttu-id="19ed8-139">Filtro a ser aplicado aos resultados deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19ed8-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="19ed8-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="19ed8-140">-Name</span></span>
<span data-ttu-id="19ed8-141">Nome da comunicação.</span><span class="sxs-lookup"><span data-stu-id="19ed8-141">Communication name.</span></span>

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

### <span data-ttu-id="19ed8-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="19ed8-142">-SupportTicketName</span></span>
<span data-ttu-id="19ed8-143">Nome do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="19ed8-143">Support ticket name.</span></span>

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

### <span data-ttu-id="19ed8-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="19ed8-144">-SupportTicketObject</span></span>
<span data-ttu-id="19ed8-145">Objeto de tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="19ed8-145">Support ticket object.</span></span>

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

### <span data-ttu-id="19ed8-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="19ed8-146">-IncludeTotalCount</span></span>
<span data-ttu-id="19ed8-147">Relata o número total de objetos no conjunto de dados (um número inteiro) seguido pelos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="19ed8-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="19ed8-148">Se o cmdlet não puder determinar a contagem total, ele exibirá "contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="19ed8-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="19ed8-149">O inteiro tem uma propriedade exactidão que indica a confiabilidade do valor total de contagem.</span><span class="sxs-lookup"><span data-stu-id="19ed8-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="19ed8-150">O valor de precisão varia de 0,0 a 1,0, onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa mais confiável.</span><span class="sxs-lookup"><span data-stu-id="19ed8-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="19ed8-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="19ed8-151">-Skip</span></span>
<span data-ttu-id="19ed8-152">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="19ed8-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="19ed8-153">Digite o número de objetos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="19ed8-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="19ed8-154">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="19ed8-154">-First</span></span>
<span data-ttu-id="19ed8-155">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="19ed8-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="19ed8-156">Digite o número de objetos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="19ed8-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="19ed8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ed8-157">CommonParameters</span></span>
<span data-ttu-id="19ed8-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ed8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ed8-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19ed8-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ed8-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19ed8-160">INPUTS</span></span>

### <span data-ttu-id="19ed8-161">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="19ed8-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="19ed8-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19ed8-162">OUTPUTS</span></span>

### <span data-ttu-id="19ed8-163">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="19ed8-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="19ed8-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19ed8-164">NOTES</span></span>

## <span data-ttu-id="19ed8-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19ed8-165">RELATED LINKS</span></span>
