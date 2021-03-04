---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889738"
---
# <span data-ttu-id="90cbb-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="90cbb-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="90cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="90cbb-103">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="90cbb-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="90cbb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90cbb-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90cbb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="90cbb-106">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="90cbb-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="90cbb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90cbb-107">EXAMPLES</span></span>

### <span data-ttu-id="90cbb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90cbb-108">Example 1</span></span>
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

<span data-ttu-id="90cbb-109">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="90cbb-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="90cbb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90cbb-110">PARAMETERS</span></span>

### <span data-ttu-id="90cbb-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="90cbb-111">-AlertAdmin</span></span>
<span data-ttu-id="90cbb-112">Alertas para administradores.</span><span class="sxs-lookup"><span data-stu-id="90cbb-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="90cbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90cbb-113">-DefaultProfile</span></span>
<span data-ttu-id="90cbb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90cbb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90cbb-115">-Email</span><span class="sxs-lookup"><span data-stu-id="90cbb-115">-Email</span></span>
<span data-ttu-id="90cbb-116">Email.</span><span class="sxs-lookup"><span data-stu-id="90cbb-116">E-Mail.</span></span>

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

### <span data-ttu-id="90cbb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90cbb-117">-Name</span></span>
<span data-ttu-id="90cbb-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="90cbb-118">Resource name.</span></span>

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

### <span data-ttu-id="90cbb-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="90cbb-119">-NotifyOnAlert</span></span>
<span data-ttu-id="90cbb-120">Notificações de alerta.</span><span class="sxs-lookup"><span data-stu-id="90cbb-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="90cbb-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="90cbb-121">-Phone</span></span>
<span data-ttu-id="90cbb-122">Telefone.</span><span class="sxs-lookup"><span data-stu-id="90cbb-122">Phone.</span></span>

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

### <span data-ttu-id="90cbb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90cbb-123">-Confirm</span></span>
<span data-ttu-id="90cbb-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90cbb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90cbb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90cbb-125">-WhatIf</span></span>
<span data-ttu-id="90cbb-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90cbb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90cbb-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90cbb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90cbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90cbb-128">CommonParameters</span></span>
<span data-ttu-id="90cbb-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90cbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90cbb-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90cbb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90cbb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90cbb-131">INPUTS</span></span>

### <span data-ttu-id="90cbb-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="90cbb-132">None</span></span>

## <span data-ttu-id="90cbb-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90cbb-133">OUTPUTS</span></span>

### <span data-ttu-id="90cbb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="90cbb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="90cbb-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="90cbb-135">NOTES</span></span>

## <span data-ttu-id="90cbb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90cbb-136">RELATED LINKS</span></span>
