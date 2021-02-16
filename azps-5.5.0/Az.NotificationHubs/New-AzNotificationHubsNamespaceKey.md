---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118237"
---
# <span data-ttu-id="287fd-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="287fd-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="287fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="287fd-102">SYNOPSIS</span></span>
<span data-ttu-id="287fd-103">Regenerar a Chave de Regra de Autorização para um Namespace.</span><span class="sxs-lookup"><span data-stu-id="287fd-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="287fd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="287fd-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287fd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="287fd-105">DESCRIPTION</span></span>
<span data-ttu-id="287fd-106">New-AzNotificationHubNamespaceKey cmdlet regenera a Chave Primária/Chave Secundária para a Regra de Autorização do Namespace.</span><span class="sxs-lookup"><span data-stu-id="287fd-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="287fd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="287fd-107">EXAMPLES</span></span>

### <span data-ttu-id="287fd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="287fd-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="287fd-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="287fd-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="287fd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="287fd-110">PARAMETERS</span></span>

### <span data-ttu-id="287fd-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="287fd-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="287fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287fd-112">-DefaultProfile</span></span>
<span data-ttu-id="287fd-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="287fd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="287fd-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="287fd-114">-Force</span></span>
<span data-ttu-id="287fd-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="287fd-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="287fd-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="287fd-116">-Namespace</span></span>
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

### <span data-ttu-id="287fd-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="287fd-117">-PolicyKey</span></span>
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

### <span data-ttu-id="287fd-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="287fd-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="287fd-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="287fd-119">-Confirm</span></span>
<span data-ttu-id="287fd-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287fd-121">-WhatIf</span></span>
<span data-ttu-id="287fd-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="287fd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287fd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="287fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287fd-124">CommonParameters</span></span>
<span data-ttu-id="287fd-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287fd-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287fd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287fd-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="287fd-127">INPUTS</span></span>

### <span data-ttu-id="287fd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="287fd-128">System.String</span></span>

## <span data-ttu-id="287fd-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="287fd-129">OUTPUTS</span></span>

### <span data-ttu-id="287fd-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="287fd-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="287fd-131">Notas</span><span class="sxs-lookup"><span data-stu-id="287fd-131">NOTES</span></span>

## <span data-ttu-id="287fd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="287fd-132">RELATED LINKS</span></span>
