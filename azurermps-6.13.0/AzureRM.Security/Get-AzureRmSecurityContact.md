---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609740"
---
# <span data-ttu-id="bc553-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bc553-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="bc553-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc553-102">SYNOPSIS</span></span>
<span data-ttu-id="bc553-103">Obtém contatos de segurança que foram configurados nesta assinatura</span><span class="sxs-lookup"><span data-stu-id="bc553-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc553-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc553-104">SYNTAX</span></span>

### <span data-ttu-id="bc553-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc553-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc553-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="bc553-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc553-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bc553-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc553-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc553-108">DESCRIPTION</span></span>
<span data-ttu-id="bc553-109">Obtém contatos de segurança que foram configurados nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="bc553-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="bc553-110">O contato de segurança pode receber notificações sobre alertas de segurança que acontecem na assinatura.</span><span class="sxs-lookup"><span data-stu-id="bc553-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="bc553-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc553-111">EXAMPLES</span></span>

### <span data-ttu-id="bc553-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc553-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="bc553-113">Obtém todos os contatos de segurança configurados na assinatura</span><span class="sxs-lookup"><span data-stu-id="bc553-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="bc553-114">OS</span><span class="sxs-lookup"><span data-stu-id="bc553-114">PARAMETERS</span></span>

### <span data-ttu-id="bc553-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc553-115">-DefaultProfile</span></span>
<span data-ttu-id="bc553-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc553-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc553-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc553-117">-Name</span></span>
<span data-ttu-id="bc553-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc553-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc553-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc553-119">-ResourceId</span></span>
<span data-ttu-id="bc553-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc553-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc553-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc553-121">CommonParameters</span></span>
<span data-ttu-id="bc553-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc553-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc553-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc553-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc553-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc553-124">INPUTS</span></span>

### <span data-ttu-id="bc553-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bc553-125">System.String</span></span>

## <span data-ttu-id="bc553-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc553-126">OUTPUTS</span></span>

### <span data-ttu-id="bc553-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bc553-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="bc553-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc553-128">NOTES</span></span>

## <span data-ttu-id="bc553-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc553-129">RELATED LINKS</span></span>
