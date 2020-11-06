---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: f426dc06d08e10d0811382b00e2072f65ebf1b0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599902"
---
# <span data-ttu-id="ba957-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="ba957-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="ba957-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba957-102">SYNOPSIS</span></span>
<span data-ttu-id="ba957-103">Regenerar a chave de regra de autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="ba957-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="ba957-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba957-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba957-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba957-105">DESCRIPTION</span></span>
<span data-ttu-id="ba957-106">New-AzNotificationHubKey cmdlet regenera a chave primária/chave secundária para a regra de autorização NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="ba957-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="ba957-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba957-107">EXAMPLES</span></span>

### <span data-ttu-id="ba957-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba957-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ba957-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="ba957-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ba957-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba957-110">PARAMETERS</span></span>

### <span data-ttu-id="ba957-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba957-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="ba957-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba957-112">-DefaultProfile</span></span>
<span data-ttu-id="ba957-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ba957-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba957-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ba957-114">-Force</span></span>
<span data-ttu-id="ba957-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba957-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ba957-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba957-116">-Namespace</span></span>
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

### <span data-ttu-id="ba957-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba957-117">-NotificationHub</span></span>
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

### <span data-ttu-id="ba957-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="ba957-118">-PolicyKey</span></span>
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

### <span data-ttu-id="ba957-119">-Resource</span><span class="sxs-lookup"><span data-stu-id="ba957-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="ba957-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba957-120">-Confirm</span></span>
<span data-ttu-id="ba957-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba957-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba957-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba957-122">-WhatIf</span></span>
<span data-ttu-id="ba957-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba957-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba957-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba957-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba957-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba957-125">CommonParameters</span></span>
<span data-ttu-id="ba957-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba957-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba957-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba957-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba957-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba957-128">INPUTS</span></span>

### <span data-ttu-id="ba957-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ba957-129">System.String</span></span>

## <span data-ttu-id="ba957-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba957-130">OUTPUTS</span></span>

### <span data-ttu-id="ba957-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="ba957-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="ba957-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba957-132">NOTES</span></span>

## <span data-ttu-id="ba957-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba957-133">RELATED LINKS</span></span>
