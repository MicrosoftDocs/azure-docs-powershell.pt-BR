---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112425"
---
# <span data-ttu-id="2099b-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="2099b-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="2099b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2099b-102">SYNOPSIS</span></span>
<span data-ttu-id="2099b-103">Cria um objeto de perfil de contato de suporte.</span><span class="sxs-lookup"><span data-stu-id="2099b-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="2099b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2099b-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2099b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2099b-105">DESCRIPTION</span></span>
<span data-ttu-id="2099b-106">Este é um cmdlet auxiliar que você pode usar para criar um objeto de perfil de contato de suporte ao criar ou atualizar um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="2099b-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="2099b-107">Você deve especificar os seguintes parâmetros obrigatórios para a criação de um tíquete de suporte:</span><span class="sxs-lookup"><span data-stu-id="2099b-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="2099b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2099b-108">EXAMPLES</span></span>

### <span data-ttu-id="2099b-109">Exemplo 1: Criar um objeto de contato</span><span class="sxs-lookup"><span data-stu-id="2099b-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="2099b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2099b-110">PARAMETERS</span></span>

### <span data-ttu-id="2099b-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2099b-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="2099b-112">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="2099b-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2099b-113">-País/Região</span><span class="sxs-lookup"><span data-stu-id="2099b-113">-Country</span></span>
<span data-ttu-id="2099b-114">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-114">Customer country.</span></span>
<span data-ttu-id="2099b-115">Esse deve ser um código de país ISO Alpha-3 válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="2099b-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="2099b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2099b-116">-DefaultProfile</span></span>
<span data-ttu-id="2099b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2099b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2099b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2099b-118">-FirstName</span></span>
<span data-ttu-id="2099b-119">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-119">Customer first name.</span></span>

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

### <span data-ttu-id="2099b-120">-Sobrenome</span><span class="sxs-lookup"><span data-stu-id="2099b-120">-LastName</span></span>
<span data-ttu-id="2099b-121">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-121">Customer last name.</span></span>

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

### <span data-ttu-id="2099b-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2099b-122">-PhoneNumber</span></span>
<span data-ttu-id="2099b-123">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-123">Customer phone number.</span></span>
<span data-ttu-id="2099b-124">Isso é necessário se o método de contato preferencial for telefone.</span><span class="sxs-lookup"><span data-stu-id="2099b-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="2099b-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="2099b-125">-PreferredContactMethod</span></span>
<span data-ttu-id="2099b-126">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="2099b-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2099b-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="2099b-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="2099b-128">Idioma de suporte preferido do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-128">Customer preferred support language.</span></span>
<span data-ttu-id="2099b-129">Esse deve ser um código de controle de idioma válido para um dos idiomas com suporte listados https://azure.microsoft.com/support/faq/ aqui.</span><span class="sxs-lookup"><span data-stu-id="2099b-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="2099b-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="2099b-130">-PreferredTimeZone</span></span>
<span data-ttu-id="2099b-131">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-131">Customer preferred time zone.</span></span>
<span data-ttu-id="2099b-132">Esse deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="2099b-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="2099b-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2099b-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="2099b-134">Endereço de email principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="2099b-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="2099b-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2099b-135">-Confirm</span></span>
<span data-ttu-id="2099b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2099b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2099b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2099b-137">-WhatIf</span></span>
<span data-ttu-id="2099b-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2099b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2099b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2099b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2099b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2099b-140">CommonParameters</span></span>
<span data-ttu-id="2099b-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2099b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2099b-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2099b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2099b-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="2099b-143">INPUTS</span></span>

### <span data-ttu-id="2099b-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2099b-144">None</span></span>

## <span data-ttu-id="2099b-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="2099b-145">OUTPUTS</span></span>

### <span data-ttu-id="2099b-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="2099b-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="2099b-147">Notas</span><span class="sxs-lookup"><span data-stu-id="2099b-147">NOTES</span></span>

## <span data-ttu-id="2099b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2099b-148">RELATED LINKS</span></span>
