---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115024"
---
# <span data-ttu-id="16ad9-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="16ad9-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="16ad9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="16ad9-103">Regenerar a Chave de Regra de Autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="16ad9-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="16ad9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16ad9-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ad9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="16ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="16ad9-106">New-AzNotificationHubKey cmdlet regenera a Chave Primária/Chave Secundária para a Regra de Autorização do NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="16ad9-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="16ad9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16ad9-107">EXAMPLES</span></span>

### <span data-ttu-id="16ad9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16ad9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="16ad9-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="16ad9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="16ad9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16ad9-110">PARAMETERS</span></span>

### <span data-ttu-id="16ad9-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="16ad9-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="16ad9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ad9-112">-DefaultProfile</span></span>
<span data-ttu-id="16ad9-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="16ad9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16ad9-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="16ad9-114">-Force</span></span>
<span data-ttu-id="16ad9-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="16ad9-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16ad9-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16ad9-116">-Namespace</span></span>
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

### <span data-ttu-id="16ad9-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="16ad9-117">-NotificationHub</span></span>
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

### <span data-ttu-id="16ad9-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="16ad9-118">-PolicyKey</span></span>
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

### <span data-ttu-id="16ad9-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16ad9-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="16ad9-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16ad9-120">-Confirm</span></span>
<span data-ttu-id="16ad9-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16ad9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ad9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ad9-122">-WhatIf</span></span>
<span data-ttu-id="16ad9-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16ad9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ad9-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16ad9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ad9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ad9-125">CommonParameters</span></span>
<span data-ttu-id="16ad9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ad9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ad9-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ad9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ad9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="16ad9-128">INPUTS</span></span>

### <span data-ttu-id="16ad9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="16ad9-129">System.String</span></span>

## <span data-ttu-id="16ad9-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="16ad9-130">OUTPUTS</span></span>

### <span data-ttu-id="16ad9-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="16ad9-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="16ad9-132">Notas</span><span class="sxs-lookup"><span data-stu-id="16ad9-132">NOTES</span></span>

## <span data-ttu-id="16ad9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16ad9-133">RELATED LINKS</span></span>
