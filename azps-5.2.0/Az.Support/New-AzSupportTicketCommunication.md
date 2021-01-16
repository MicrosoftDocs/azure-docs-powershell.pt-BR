---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259632"
---
# <span data-ttu-id="054be-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="054be-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="054be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="054be-102">SYNOPSIS</span></span>
<span data-ttu-id="054be-103">Cria uma nova comunicação de permissão de suporte.</span><span class="sxs-lookup"><span data-stu-id="054be-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="054be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="054be-104">SYNTAX</span></span>

### <span data-ttu-id="054be-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="054be-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="054be-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="054be-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="054be-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="054be-107">DESCRIPTION</span></span>
<span data-ttu-id="054be-108">Adiciona uma nova comunicação de cliente a um tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="054be-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="054be-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="054be-109">EXAMPLES</span></span>

### <span data-ttu-id="054be-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="054be-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="054be-111">OS</span><span class="sxs-lookup"><span data-stu-id="054be-111">PARAMETERS</span></span>

### <span data-ttu-id="054be-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="054be-112">-AsJob</span></span>
<span data-ttu-id="054be-113">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="054be-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="054be-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="054be-114">-Body</span></span>
<span data-ttu-id="054be-115">Corpo da comunicação.</span><span class="sxs-lookup"><span data-stu-id="054be-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054be-116">-DefaultProfile</span></span>
<span data-ttu-id="054be-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="054be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="054be-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="054be-118">-Name</span></span>
<span data-ttu-id="054be-119">Nome do recurso de comunicação.</span><span class="sxs-lookup"><span data-stu-id="054be-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-120">-Remetente</span><span class="sxs-lookup"><span data-stu-id="054be-120">-Sender</span></span>
<span data-ttu-id="054be-121">Endereço de email do remetente.</span><span class="sxs-lookup"><span data-stu-id="054be-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="054be-122">-Assunto</span><span class="sxs-lookup"><span data-stu-id="054be-122">-Subject</span></span>
<span data-ttu-id="054be-123">Assunto da comunicação.</span><span class="sxs-lookup"><span data-stu-id="054be-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="054be-124">-SupportTicketName</span></span>
<span data-ttu-id="054be-125">Nome do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="054be-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="054be-126">-SupportTicketObject</span></span>
<span data-ttu-id="054be-127">Objeto de tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="054be-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054be-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="054be-128">-Confirm</span></span>
<span data-ttu-id="054be-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="054be-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="054be-130">-WhatIf</span></span>
<span data-ttu-id="054be-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="054be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="054be-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="054be-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054be-133">CommonParameters</span></span>
<span data-ttu-id="054be-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="054be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054be-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="054be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054be-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="054be-136">INPUTS</span></span>

### <span data-ttu-id="054be-137">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="054be-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="054be-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="054be-138">OUTPUTS</span></span>

### <span data-ttu-id="054be-139">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="054be-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="054be-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="054be-140">NOTES</span></span>

## <span data-ttu-id="054be-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="054be-141">RELATED LINKS</span></span>
