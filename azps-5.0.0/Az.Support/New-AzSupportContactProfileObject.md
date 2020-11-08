---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115165"
---
# <span data-ttu-id="85bff-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="85bff-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="85bff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85bff-102">SYNOPSIS</span></span>
<span data-ttu-id="85bff-103">Cria um objeto de perfil de contato de suporte.</span><span class="sxs-lookup"><span data-stu-id="85bff-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="85bff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85bff-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85bff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85bff-105">DESCRIPTION</span></span>
<span data-ttu-id="85bff-106">Esse é um cmdlet auxiliar que você pode usar para criar um objeto de perfil de contato de suporte ao criar ou atualizar um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="85bff-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="85bff-107">Você deve especificar os seguintes parâmetros que são obrigatórios para a criação de um tíquete de suporte:</span><span class="sxs-lookup"><span data-stu-id="85bff-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="85bff-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85bff-108">EXAMPLES</span></span>

### <span data-ttu-id="85bff-109">Exemplo 1: criar um objeto de contato</span><span class="sxs-lookup"><span data-stu-id="85bff-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="85bff-110">OS</span><span class="sxs-lookup"><span data-stu-id="85bff-110">PARAMETERS</span></span>

### <span data-ttu-id="85bff-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85bff-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="85bff-112">Os endereços de email listados aqui serão copiados em qualquer correspondência sobre o tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="85bff-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="85bff-113">-País</span><span class="sxs-lookup"><span data-stu-id="85bff-113">-Country</span></span>
<span data-ttu-id="85bff-114">País do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-114">Customer country.</span></span>
<span data-ttu-id="85bff-115">Deve ser um código de país Alfa-3 ISO válido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="85bff-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="85bff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bff-116">-DefaultProfile</span></span>
<span data-ttu-id="85bff-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85bff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85bff-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="85bff-118">-FirstName</span></span>
<span data-ttu-id="85bff-119">Nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-119">Customer first name.</span></span>

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

### <span data-ttu-id="85bff-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="85bff-120">-LastName</span></span>
<span data-ttu-id="85bff-121">Sobrenome do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-121">Customer last name.</span></span>

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

### <span data-ttu-id="85bff-122">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="85bff-122">-PhoneNumber</span></span>
<span data-ttu-id="85bff-123">Número de telefone do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-123">Customer phone number.</span></span>
<span data-ttu-id="85bff-124">Isso será necessário se o método de contato preferencial for o telefone.</span><span class="sxs-lookup"><span data-stu-id="85bff-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="85bff-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="85bff-125">-PreferredContactMethod</span></span>
<span data-ttu-id="85bff-126">Método de contato preferencial.</span><span class="sxs-lookup"><span data-stu-id="85bff-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="85bff-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="85bff-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="85bff-128">Idioma de suporte preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-128">Customer preferred support language.</span></span>
<span data-ttu-id="85bff-129">Deve ser um código de conta de idioma válido para um dos idiomas com suporte listados aqui https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="85bff-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="85bff-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="85bff-130">-PreferredTimeZone</span></span>
<span data-ttu-id="85bff-131">Fuso horário preferencial do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-131">Customer preferred time zone.</span></span>
<span data-ttu-id="85bff-132">Deve ser um valor System.TimeZoneInfo.Id válido.</span><span class="sxs-lookup"><span data-stu-id="85bff-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="85bff-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85bff-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="85bff-134">Endereço de e-mail principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="85bff-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="85bff-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85bff-135">-Confirm</span></span>
<span data-ttu-id="85bff-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85bff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85bff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85bff-137">-WhatIf</span></span>
<span data-ttu-id="85bff-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85bff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85bff-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85bff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85bff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bff-140">CommonParameters</span></span>
<span data-ttu-id="85bff-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85bff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bff-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85bff-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bff-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85bff-143">INPUTS</span></span>

### <span data-ttu-id="85bff-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85bff-144">None</span></span>

## <span data-ttu-id="85bff-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85bff-145">OUTPUTS</span></span>

### <span data-ttu-id="85bff-146">Microsoft. Azure. Commands. support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="85bff-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="85bff-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85bff-147">NOTES</span></span>

## <span data-ttu-id="85bff-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85bff-148">RELATED LINKS</span></span>
