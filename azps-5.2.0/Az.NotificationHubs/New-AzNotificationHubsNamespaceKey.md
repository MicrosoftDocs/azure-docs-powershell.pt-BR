---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258744"
---
# <span data-ttu-id="2c0df-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="2c0df-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="2c0df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c0df-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0df-103">Regenerar a chave de regra de autorização para um namespace.</span><span class="sxs-lookup"><span data-stu-id="2c0df-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="2c0df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c0df-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c0df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c0df-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0df-106">New-AzNotificationHubNamespaceKey cmdlet regenera a chave primária/chave secundária para a regra de autorização de namespace.</span><span class="sxs-lookup"><span data-stu-id="2c0df-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="2c0df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c0df-107">EXAMPLES</span></span>

### <span data-ttu-id="2c0df-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c0df-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2c0df-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="2c0df-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2c0df-110">OS</span><span class="sxs-lookup"><span data-stu-id="2c0df-110">PARAMETERS</span></span>

### <span data-ttu-id="2c0df-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c0df-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0df-112">-DefaultProfile</span></span>
<span data-ttu-id="2c0df-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2c0df-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c0df-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2c0df-114">-Force</span></span>
<span data-ttu-id="2c0df-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c0df-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c0df-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c0df-116">-Namespace</span></span>
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

### <span data-ttu-id="2c0df-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="2c0df-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0df-118">-Resource</span><span class="sxs-lookup"><span data-stu-id="2c0df-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="2c0df-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c0df-119">-Confirm</span></span>
<span data-ttu-id="2c0df-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c0df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c0df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c0df-121">-WhatIf</span></span>
<span data-ttu-id="2c0df-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c0df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c0df-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c0df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c0df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0df-124">CommonParameters</span></span>
<span data-ttu-id="2c0df-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0df-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c0df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0df-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c0df-127">INPUTS</span></span>

### <span data-ttu-id="2c0df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2c0df-128">System.String</span></span>

## <span data-ttu-id="2c0df-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c0df-129">OUTPUTS</span></span>

### <span data-ttu-id="2c0df-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="2c0df-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="2c0df-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c0df-131">NOTES</span></span>

## <span data-ttu-id="2c0df-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c0df-132">RELATED LINKS</span></span>
