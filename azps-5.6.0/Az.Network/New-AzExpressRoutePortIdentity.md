---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: e3b3b0a0990f8c72fcd18d8828ae97d5c1a8a5aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901456"
---
# <span data-ttu-id="0655a-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0655a-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="0655a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0655a-102">SYNOPSIS</span></span>
<span data-ttu-id="0655a-103">Cria um Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="0655a-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="0655a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0655a-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0655a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0655a-105">DESCRIPTION</span></span>
<span data-ttu-id="0655a-106">O cmdlet **New-AzExpressRoutePortIdentity** cria um objeto local Azure ExpressRoutePort Identity.</span><span class="sxs-lookup"><span data-stu-id="0655a-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="0655a-107">Use **New-AzExpressRoutePort** ou **Set-AzExpressRoutePort** para atribuí-lo ao Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0655a-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="0655a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0655a-108">EXAMPLES</span></span>

### <span data-ttu-id="0655a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0655a-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="0655a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0655a-110">PARAMETERS</span></span>

### <span data-ttu-id="0655a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0655a-111">-DefaultProfile</span></span>
<span data-ttu-id="0655a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0655a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0655a-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="0655a-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="0655a-114">ResourceId da identidade atribuída pelo usuário a ser atribuída ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0655a-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0655a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0655a-115">-Confirm</span></span>
<span data-ttu-id="0655a-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0655a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0655a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0655a-117">-WhatIf</span></span>
<span data-ttu-id="0655a-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0655a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0655a-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0655a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0655a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0655a-120">CommonParameters</span></span>
<span data-ttu-id="0655a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0655a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0655a-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0655a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0655a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0655a-123">INPUTS</span></span>

### <span data-ttu-id="0655a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0655a-124">System.String</span></span>

## <span data-ttu-id="0655a-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0655a-125">OUTPUTS</span></span>

### <span data-ttu-id="0655a-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="0655a-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="0655a-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="0655a-127">NOTES</span></span>

## <span data-ttu-id="0655a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0655a-128">RELATED LINKS</span></span>
[<span data-ttu-id="0655a-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0655a-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0655a-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0655a-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0655a-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0655a-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)