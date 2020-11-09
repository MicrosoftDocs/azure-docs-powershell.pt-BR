---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282002"
---
# <span data-ttu-id="b1f05-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="b1f05-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="b1f05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1f05-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f05-103">Regenerar a chave de regra de autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="b1f05-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="b1f05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1f05-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1f05-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f05-106">New-AzNotificationHubKey cmdlet regenera a chave primária/chave secundária para a regra de autorização NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="b1f05-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="b1f05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1f05-107">EXAMPLES</span></span>

### <span data-ttu-id="b1f05-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1f05-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b1f05-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b1f05-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b1f05-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1f05-110">PARAMETERS</span></span>

### <span data-ttu-id="b1f05-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b1f05-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="b1f05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f05-112">-DefaultProfile</span></span>
<span data-ttu-id="b1f05-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b1f05-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f05-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f05-114">-Force</span></span>
<span data-ttu-id="b1f05-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b1f05-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1f05-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1f05-116">-Namespace</span></span>
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

### <span data-ttu-id="b1f05-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b1f05-117">-NotificationHub</span></span>
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

### <span data-ttu-id="b1f05-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="b1f05-118">-PolicyKey</span></span>
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

### <span data-ttu-id="b1f05-119">-Resource</span><span class="sxs-lookup"><span data-stu-id="b1f05-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="b1f05-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1f05-120">-Confirm</span></span>
<span data-ttu-id="b1f05-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f05-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f05-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f05-122">-WhatIf</span></span>
<span data-ttu-id="b1f05-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1f05-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f05-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1f05-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f05-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f05-125">CommonParameters</span></span>
<span data-ttu-id="b1f05-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f05-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f05-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f05-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f05-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1f05-128">INPUTS</span></span>

### <span data-ttu-id="b1f05-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f05-129">System.String</span></span>

## <span data-ttu-id="b1f05-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1f05-130">OUTPUTS</span></span>

### <span data-ttu-id="b1f05-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b1f05-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b1f05-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1f05-132">NOTES</span></span>

## <span data-ttu-id="b1f05-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1f05-133">RELATED LINKS</span></span>
