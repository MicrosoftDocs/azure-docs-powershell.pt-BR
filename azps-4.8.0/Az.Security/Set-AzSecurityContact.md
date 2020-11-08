---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110880"
---
# <span data-ttu-id="0f3f1-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0f3f1-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="0f3f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3f1-103">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0f3f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f3f1-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f3f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f3f1-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3f1-106">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0f3f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f3f1-107">EXAMPLES</span></span>

### <span data-ttu-id="0f3f1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f3f1-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="0f3f1-109">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0f3f1-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f3f1-110">PARAMETERS</span></span>

### <span data-ttu-id="0f3f1-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="0f3f1-111">-AlertAdmin</span></span>
<span data-ttu-id="0f3f1-112">Alertas para administradores.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="0f3f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3f1-113">-DefaultProfile</span></span>
<span data-ttu-id="0f3f1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f3f1-115">-Email</span><span class="sxs-lookup"><span data-stu-id="0f3f1-115">-Email</span></span>
<span data-ttu-id="0f3f1-116">E-mails.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-116">E-Mail.</span></span>

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

### <span data-ttu-id="0f3f1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f3f1-117">-Name</span></span>
<span data-ttu-id="0f3f1-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-118">Resource name.</span></span>

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

### <span data-ttu-id="0f3f1-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="0f3f1-119">-NotifyOnAlert</span></span>
<span data-ttu-id="0f3f1-120">Notificações de alerta.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="0f3f1-121">-Telefone</span><span class="sxs-lookup"><span data-stu-id="0f3f1-121">-Phone</span></span>
<span data-ttu-id="0f3f1-122">Telefone.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-122">Phone.</span></span>

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

### <span data-ttu-id="0f3f1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f3f1-123">-Confirm</span></span>
<span data-ttu-id="0f3f1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3f1-125">-WhatIf</span></span>
<span data-ttu-id="0f3f1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f3f1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3f1-128">CommonParameters</span></span>
<span data-ttu-id="0f3f1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3f1-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f3f1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3f1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f3f1-131">INPUTS</span></span>

### <span data-ttu-id="0f3f1-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0f3f1-132">None</span></span>

## <span data-ttu-id="0f3f1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f3f1-133">OUTPUTS</span></span>

### <span data-ttu-id="0f3f1-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0f3f1-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="0f3f1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f3f1-135">NOTES</span></span>

## <span data-ttu-id="0f3f1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f3f1-136">RELATED LINKS</span></span>
