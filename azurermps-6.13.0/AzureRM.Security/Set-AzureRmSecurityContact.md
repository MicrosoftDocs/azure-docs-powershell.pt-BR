---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430029"
---
# <span data-ttu-id="539d0-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="539d0-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="539d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="539d0-102">SYNOPSIS</span></span>
<span data-ttu-id="539d0-103">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="539d0-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="539d0-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="539d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="539d0-105">DESCRIPTION</span></span>
<span data-ttu-id="539d0-106">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="539d0-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="539d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="539d0-107">EXAMPLES</span></span>

### <span data-ttu-id="539d0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="539d0-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="539d0-109">Atualiza um contato de segurança para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="539d0-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="539d0-110">OS</span><span class="sxs-lookup"><span data-stu-id="539d0-110">PARAMETERS</span></span>

### <span data-ttu-id="539d0-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="539d0-111">-AlertAdmin</span></span>
<span data-ttu-id="539d0-112">Alertas para administradores.</span><span class="sxs-lookup"><span data-stu-id="539d0-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539d0-113">-DefaultProfile</span></span>
<span data-ttu-id="539d0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="539d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-115">-Email</span><span class="sxs-lookup"><span data-stu-id="539d0-115">-Email</span></span>
<span data-ttu-id="539d0-116">E-mails.</span><span class="sxs-lookup"><span data-stu-id="539d0-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="539d0-117">-Name</span></span>
<span data-ttu-id="539d0-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="539d0-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="539d0-119">-NotifyOnAlert</span></span>
<span data-ttu-id="539d0-120">Notificações de alerta.</span><span class="sxs-lookup"><span data-stu-id="539d0-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-121">-Telefone</span><span class="sxs-lookup"><span data-stu-id="539d0-121">-Phone</span></span>
<span data-ttu-id="539d0-122">Telefone.</span><span class="sxs-lookup"><span data-stu-id="539d0-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="539d0-123">-Confirm</span></span>
<span data-ttu-id="539d0-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="539d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="539d0-125">-WhatIf</span></span>
<span data-ttu-id="539d0-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="539d0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="539d0-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="539d0-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539d0-128">CommonParameters</span></span>
<span data-ttu-id="539d0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539d0-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539d0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="539d0-131">INPUTS</span></span>

### <span data-ttu-id="539d0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="539d0-132">System.String</span></span>

## <span data-ttu-id="539d0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="539d0-133">OUTPUTS</span></span>

### <span data-ttu-id="539d0-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="539d0-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="539d0-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="539d0-135">NOTES</span></span>

## <span data-ttu-id="539d0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="539d0-136">RELATED LINKS</span></span>
