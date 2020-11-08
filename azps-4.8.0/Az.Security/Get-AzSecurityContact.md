---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110905"
---
# <span data-ttu-id="a8f10-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a8f10-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="a8f10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8f10-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f10-103">Obtém contatos de segurança que foram configurados nesta assinatura</span><span class="sxs-lookup"><span data-stu-id="a8f10-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="a8f10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8f10-104">SYNTAX</span></span>

### <span data-ttu-id="a8f10-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8f10-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f10-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a8f10-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f10-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a8f10-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8f10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8f10-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f10-109">Obtém contatos de segurança que foram configurados nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="a8f10-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="a8f10-110">O contato de segurança pode receber notificações sobre alertas de segurança que acontecem na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a8f10-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="a8f10-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8f10-111">EXAMPLES</span></span>

### <span data-ttu-id="a8f10-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8f10-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a8f10-113">Obtém todos os contatos de segurança configurados na assinatura</span><span class="sxs-lookup"><span data-stu-id="a8f10-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="a8f10-114">OS</span><span class="sxs-lookup"><span data-stu-id="a8f10-114">PARAMETERS</span></span>

### <span data-ttu-id="a8f10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f10-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f10-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f10-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8f10-117">-Name</span></span>
<span data-ttu-id="a8f10-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a8f10-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f10-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f10-119">-ResourceId</span></span>
<span data-ttu-id="a8f10-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a8f10-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f10-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f10-121">CommonParameters</span></span>
<span data-ttu-id="a8f10-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f10-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f10-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8f10-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f10-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8f10-124">INPUTS</span></span>

### <span data-ttu-id="a8f10-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a8f10-125">System.String</span></span>

## <span data-ttu-id="a8f10-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8f10-126">OUTPUTS</span></span>

### <span data-ttu-id="a8f10-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a8f10-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a8f10-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8f10-128">NOTES</span></span>

## <span data-ttu-id="a8f10-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8f10-129">RELATED LINKS</span></span>
