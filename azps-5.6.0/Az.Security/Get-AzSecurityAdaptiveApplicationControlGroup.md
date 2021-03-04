---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893118"
---
# <span data-ttu-id="e516b-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="e516b-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="e516b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e516b-102">SYNOPSIS</span></span>
<span data-ttu-id="e516b-103">Obtém um grupo de VM/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e516b-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="e516b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e516b-104">SYNTAX</span></span>

### <span data-ttu-id="e516b-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e516b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e516b-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e516b-106">DESCRIPTION</span></span>
<span data-ttu-id="e516b-107">Controles de aplicativo adaptáveis são calculados automaticamente pelo Centro de Segurança do Azure, use este cmdlet para obter um grupo de VM/servidor de controle de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e516b-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="e516b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e516b-108">EXAMPLES</span></span>

### <span data-ttu-id="e516b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e516b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="e516b-110">Obtém um grupo de VM/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e516b-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="e516b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e516b-111">PARAMETERS</span></span>

### <span data-ttu-id="e516b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e516b-112">-DefaultProfile</span></span>
<span data-ttu-id="e516b-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e516b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e516b-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="e516b-114">-AscLocation</span></span>
<span data-ttu-id="e516b-115">O local onde o ASC armazena os dados da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e516b-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="e516b-116">pode ser recuperado de Obter locais.</span><span class="sxs-lookup"><span data-stu-id="e516b-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e516b-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e516b-117">-GroupName</span></span>
<span data-ttu-id="e516b-118">Nome de um grupo de VM/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e516b-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e516b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e516b-119">-SubscriptionId</span></span>
<span data-ttu-id="e516b-120">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e516b-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="e516b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e516b-121">CommonParameters</span></span>
<span data-ttu-id="e516b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e516b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e516b-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e516b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e516b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e516b-124">INPUTS</span></span>

### <span data-ttu-id="e516b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e516b-125">System.String</span></span>

## <span data-ttu-id="e516b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e516b-126">OUTPUTS</span></span>

### <span data-ttu-id="e516b-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="e516b-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="e516b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="e516b-128">NOTES</span></span>

## <span data-ttu-id="e516b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e516b-129">RELATED LINKS</span></span>