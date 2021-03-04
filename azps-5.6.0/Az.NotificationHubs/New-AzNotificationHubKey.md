---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 8c6b24dd2d208ea4465138f1e901b030ee5c30e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885294"
---
# <span data-ttu-id="488fc-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="488fc-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="488fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="488fc-102">SYNOPSIS</span></span>
<span data-ttu-id="488fc-103">Regenerar a Chave de Regra de Autorização para um NotificationHub .</span><span class="sxs-lookup"><span data-stu-id="488fc-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="488fc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="488fc-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="488fc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="488fc-105">DESCRIPTION</span></span>
<span data-ttu-id="488fc-106">New-AzNotificationHubKey cmdlet regenera a Chave Primária/Chave Secundária para a Regra de Autorização notificationHub.</span><span class="sxs-lookup"><span data-stu-id="488fc-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="488fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="488fc-107">EXAMPLES</span></span>

### <span data-ttu-id="488fc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="488fc-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="488fc-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="488fc-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="488fc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="488fc-110">PARAMETERS</span></span>

### <span data-ttu-id="488fc-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="488fc-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="488fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488fc-112">-DefaultProfile</span></span>
<span data-ttu-id="488fc-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="488fc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="488fc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="488fc-114">-Force</span></span>
<span data-ttu-id="488fc-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="488fc-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="488fc-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="488fc-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="488fc-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="488fc-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="488fc-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="488fc-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488fc-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="488fc-119">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="488fc-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="488fc-120">-Confirm</span></span>
<span data-ttu-id="488fc-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="488fc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="488fc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="488fc-122">-WhatIf</span></span>
<span data-ttu-id="488fc-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="488fc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="488fc-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="488fc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="488fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488fc-125">CommonParameters</span></span>
<span data-ttu-id="488fc-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="488fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488fc-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488fc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488fc-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="488fc-128">INPUTS</span></span>

### <span data-ttu-id="488fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="488fc-129">System.String</span></span>

## <span data-ttu-id="488fc-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="488fc-130">OUTPUTS</span></span>

### <span data-ttu-id="488fc-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="488fc-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="488fc-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="488fc-132">NOTES</span></span>

## <span data-ttu-id="488fc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="488fc-133">RELATED LINKS</span></span>
