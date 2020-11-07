---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941661"
---
# <span data-ttu-id="94e8e-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="94e8e-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="94e8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="94e8e-103">Cria um ExpressRoutePortIdentity do Azure.</span><span class="sxs-lookup"><span data-stu-id="94e8e-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="94e8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94e8e-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94e8e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="94e8e-106">O cmdlet **New-AzExpressRoutePortIdentity** cria um objeto de identidade ExpressRoutePort do Azure local.</span><span class="sxs-lookup"><span data-stu-id="94e8e-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="94e8e-107">Use **New-AzExpressRoutePort** ou **set-AzExpressRoutePort** para atribuí-lo ao Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="94e8e-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="94e8e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94e8e-108">EXAMPLES</span></span>

### <span data-ttu-id="94e8e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94e8e-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="94e8e-110">OS</span><span class="sxs-lookup"><span data-stu-id="94e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="94e8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e8e-111">-DefaultProfile</span></span>
<span data-ttu-id="94e8e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94e8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e8e-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="94e8e-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="94e8e-114">ResourceId da identidade atribuída pelo usuário a ser atribuído ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="94e8e-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="94e8e-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94e8e-115">-Confirm</span></span>
<span data-ttu-id="94e8e-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94e8e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e8e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e8e-117">-WhatIf</span></span>
<span data-ttu-id="94e8e-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94e8e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e8e-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94e8e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e8e-120">CommonParameters</span></span>
<span data-ttu-id="94e8e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e8e-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e8e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e8e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94e8e-123">INPUTS</span></span>

### <span data-ttu-id="94e8e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="94e8e-124">System.String</span></span>

## <span data-ttu-id="94e8e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94e8e-125">OUTPUTS</span></span>

### <span data-ttu-id="94e8e-126">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="94e8e-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="94e8e-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94e8e-127">NOTES</span></span>

## <span data-ttu-id="94e8e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94e8e-128">RELATED LINKS</span></span>
[<span data-ttu-id="94e8e-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="94e8e-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="94e8e-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="94e8e-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="94e8e-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="94e8e-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)