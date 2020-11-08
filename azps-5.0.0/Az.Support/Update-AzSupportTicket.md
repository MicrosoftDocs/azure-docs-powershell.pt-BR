---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117150"
---
# <span data-ttu-id="0779f-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0779f-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="0779f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0779f-102">SYNOPSIS</span></span>
<span data-ttu-id="0779f-103">Atualiza o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-103">Updates support ticket.</span></span>

## <span data-ttu-id="0779f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0779f-104">SYNTAX</span></span>

### <span data-ttu-id="0779f-105">UpdateByNameWithContactDetailParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0779f-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0779f-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0779f-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0779f-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="0779f-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0779f-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0779f-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0779f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0779f-109">DESCRIPTION</span></span>
<span data-ttu-id="0779f-110">Use esse cmdlet para atualizar o nível de gravidade, o status ou os detalhes de contato do cliente do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="0779f-111">Observe que a atualização do nível de gravidade ou status de um tíquete de suporte não é permitida quando a permissão é atribuída a um engenheiro de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="0779f-112">Se quiser atualizar o nível de gravidade ou o status após a atribuição do bilhete, entre em contato com o engenheiro de suporte para enviar uma comunicação na permissão.</span><span class="sxs-lookup"><span data-stu-id="0779f-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="0779f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0779f-113">EXAMPLES</span></span>

### <span data-ttu-id="0779f-114">Exemplo 1: atualizar a gravidade do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0779f-115">Exemplo 2: atualizar o status do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0779f-116">Exemplo 3: atualizar detalhes de contato do tíquete de suporte por meio da especificação do objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="0779f-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0779f-117">Exemplo 4: Atualize a gravidade do tíquete de suporte por meio do objeto do tíquete de suporte de tubulação.</span><span class="sxs-lookup"><span data-stu-id="0779f-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0779f-118">Exemplo 5: atualizar detalhes de contato do tíquete de suporte especificando parâmetros de contato individuais.</span><span class="sxs-lookup"><span data-stu-id="0779f-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="0779f-119">Exemplo 6: status da atualização do tíquete de suporte por objeto de tíquete de suporte de tubulação.</span><span class="sxs-lookup"><span data-stu-id="0779f-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="0779f-120">OS</span><span class="sxs-lookup"><span data-stu-id="0779f-120">PARAMETERS</span></span>

### <span data-ttu-id="0779f-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0779f-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="0779f-122">Endereços de email adicionais.</span><span class="sxs-lookup"><span data-stu-id="0779f-122">Additional email addresses.</span></span>
<span data-ttu-id="0779f-123">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="0779f-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="0779f-124">-CustomerContactDetail</span></span>
<span data-ttu-id="0779f-125">Atualize os detalhes de contato no SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="0779f-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="0779f-126">-CustomerCountry</span></span>
<span data-ttu-id="0779f-127">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-127">Customer country.</span></span>
<span data-ttu-id="0779f-128">Deve ser um código de país Alfa-3 ISO válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="0779f-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="0779f-129">-CustomerFirstName</span></span>
<span data-ttu-id="0779f-130">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="0779f-131">-CustomerLastName</span></span>
<span data-ttu-id="0779f-132">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="0779f-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="0779f-134">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-134">Customer phone number.</span></span>
<span data-ttu-id="0779f-135">Isso será necessário se o método de contato preferencial for o telefone.</span><span class="sxs-lookup"><span data-stu-id="0779f-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="0779f-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="0779f-137">Idioma de suporte preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-137">Customer preferred support language.</span></span>
<span data-ttu-id="0779f-138">Deve ser um código de conta de idioma válido para um dos idiomas com suporte listados aqui https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="0779f-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="0779f-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="0779f-140">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-140">Customer preferred time zone.</span></span>
<span data-ttu-id="0779f-141">Deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="0779f-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0779f-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="0779f-143">Endereço de e-mail principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="0779f-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0779f-144">-DefaultProfile</span></span>
<span data-ttu-id="0779f-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0779f-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0779f-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0779f-146">-InputObject</span></span>
<span data-ttu-id="0779f-147">SupportTicket objeto de recurso que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="0779f-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="0779f-148">-Name</span></span>
<span data-ttu-id="0779f-149">Nome do recurso SupportTicket que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="0779f-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="0779f-150">-PreferredContactMethod</span></span>
<span data-ttu-id="0779f-151">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="0779f-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-152">-Severidade</span><span class="sxs-lookup"><span data-stu-id="0779f-152">-Severity</span></span>
<span data-ttu-id="0779f-153">Atualize a gravidade do SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="0779f-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-154">-Status</span><span class="sxs-lookup"><span data-stu-id="0779f-154">-Status</span></span>
<span data-ttu-id="0779f-155">Status de atualização de SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="0779f-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0779f-156">-Confirm</span></span>
<span data-ttu-id="0779f-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0779f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0779f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0779f-158">-WhatIf</span></span>
<span data-ttu-id="0779f-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0779f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0779f-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0779f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0779f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779f-161">CommonParameters</span></span>
<span data-ttu-id="0779f-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779f-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0779f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779f-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0779f-164">INPUTS</span></span>

### <span data-ttu-id="0779f-165">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0779f-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="0779f-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0779f-166">OUTPUTS</span></span>

### <span data-ttu-id="0779f-167">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="0779f-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="0779f-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0779f-168">NOTES</span></span>

## <span data-ttu-id="0779f-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0779f-169">RELATED LINKS</span></span>
