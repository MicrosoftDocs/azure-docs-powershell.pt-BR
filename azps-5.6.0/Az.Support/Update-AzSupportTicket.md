---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 5fac9eac7225364af7c884ab64a80d4299939ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892280"
---
# <span data-ttu-id="5a9de-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5a9de-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="5a9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a9de-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9de-103">Atualizações suportam tíquete.</span><span class="sxs-lookup"><span data-stu-id="5a9de-103">Updates support ticket.</span></span>

## <span data-ttu-id="5a9de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a9de-104">SYNTAX</span></span>

### <span data-ttu-id="5a9de-105">UpdateByNameWithContactDetailParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a9de-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9de-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9de-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9de-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9de-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9de-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9de-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a9de-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a9de-109">DESCRIPTION</span></span>
<span data-ttu-id="5a9de-110">Use este cmdlet para atualizar o nível de gravidade, o status ou os detalhes de contato do cliente de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="5a9de-111">Observe que a atualização do nível de gravidade ou status de um tíquete de suporte não é permitida quando o tíquete é atribuído a um engenheiro de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="5a9de-112">Se você deseja atualizar o nível de gravidade ou o status após a atribuição de tíquete, contate o engenheiro de suporte enviando uma comunicação no tíquete.</span><span class="sxs-lookup"><span data-stu-id="5a9de-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="5a9de-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a9de-113">EXAMPLES</span></span>

### <span data-ttu-id="5a9de-114">Exemplo 1: Atualizar a gravidade do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5a9de-115">Exemplo 2: Atualizar o status do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5a9de-116">Exemplo 3: Atualizar detalhes de contato do tíquete de suporte especificando o objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="5a9de-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5a9de-117">Exemplo 4: Atualize a gravidade do tíquete de suporte por meio da canalização do objeto ticket de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5a9de-118">Exemplo 5: Atualizar detalhes de contato do tíquete de suporte especificando parâmetros de contato individuais.</span><span class="sxs-lookup"><span data-stu-id="5a9de-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5a9de-119">Exemplo 6: atualizar o status do tíquete de suporte canalização do objeto ticket de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="5a9de-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a9de-120">PARAMETERS</span></span>

### <span data-ttu-id="5a9de-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5a9de-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="5a9de-122">Endereços de email adicionais.</span><span class="sxs-lookup"><span data-stu-id="5a9de-122">Additional email addresses.</span></span>
<span data-ttu-id="5a9de-123">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="5a9de-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="5a9de-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="5a9de-124">-CustomerContactDetail</span></span>
<span data-ttu-id="5a9de-125">Atualizar detalhes de contato no SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="5a9de-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="5a9de-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="5a9de-126">-CustomerCountry</span></span>
<span data-ttu-id="5a9de-127">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-127">Customer country.</span></span>
<span data-ttu-id="5a9de-128">Este deve ser um código de país ISO Alpha-3 válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="5a9de-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="5a9de-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="5a9de-129">-CustomerFirstName</span></span>
<span data-ttu-id="5a9de-130">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-130">Customer first name.</span></span>

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

### <span data-ttu-id="5a9de-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="5a9de-131">-CustomerLastName</span></span>
<span data-ttu-id="5a9de-132">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-132">Customer last name.</span></span>

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

### <span data-ttu-id="5a9de-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5a9de-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="5a9de-134">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-134">Customer phone number.</span></span>
<span data-ttu-id="5a9de-135">Isso é necessário se o método de contato preferencial for telefone.</span><span class="sxs-lookup"><span data-stu-id="5a9de-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="5a9de-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="5a9de-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="5a9de-137">Idioma de suporte preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-137">Customer preferred support language.</span></span>
<span data-ttu-id="5a9de-138">Esse deve ser um código de idioma válido para um dos idiomas com suporte listados aqui https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="5a9de-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="5a9de-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="5a9de-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="5a9de-140">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-140">Customer preferred time zone.</span></span>
<span data-ttu-id="5a9de-141">Esse deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="5a9de-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="5a9de-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5a9de-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="5a9de-143">Endereço de email principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a9de-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="5a9de-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9de-144">-DefaultProfile</span></span>
<span data-ttu-id="5a9de-145">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9de-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a9de-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a9de-146">-InputObject</span></span>
<span data-ttu-id="5a9de-147">Objeto de recurso SupportTicket que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="5a9de-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5a9de-148">-Name</span><span class="sxs-lookup"><span data-stu-id="5a9de-148">-Name</span></span>
<span data-ttu-id="5a9de-149">Nome do recurso SupportTicket que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="5a9de-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5a9de-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="5a9de-150">-PreferredContactMethod</span></span>
<span data-ttu-id="5a9de-151">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="5a9de-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="5a9de-152">-Severity</span><span class="sxs-lookup"><span data-stu-id="5a9de-152">-Severity</span></span>
<span data-ttu-id="5a9de-153">Atualizar Severidade do SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="5a9de-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="5a9de-154">-Status</span><span class="sxs-lookup"><span data-stu-id="5a9de-154">-Status</span></span>
<span data-ttu-id="5a9de-155">Atualizar Status do SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="5a9de-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="5a9de-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a9de-156">-Confirm</span></span>
<span data-ttu-id="5a9de-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a9de-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a9de-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a9de-158">-WhatIf</span></span>
<span data-ttu-id="5a9de-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a9de-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a9de-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a9de-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a9de-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9de-161">CommonParameters</span></span>
<span data-ttu-id="5a9de-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a9de-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9de-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a9de-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9de-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a9de-164">INPUTS</span></span>

### <span data-ttu-id="5a9de-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5a9de-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="5a9de-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a9de-166">OUTPUTS</span></span>

### <span data-ttu-id="5a9de-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5a9de-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="5a9de-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a9de-168">NOTES</span></span>

## <span data-ttu-id="5a9de-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a9de-169">RELATED LINKS</span></span>
