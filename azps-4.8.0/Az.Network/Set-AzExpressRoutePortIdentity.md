---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114785"
---
# <span data-ttu-id="7cad1-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7cad1-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7cad1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cad1-102">SYNOPSIS</span></span>
<span data-ttu-id="7cad1-103">Atualiza uma identidade atribuída a um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7cad1-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="7cad1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cad1-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cad1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cad1-105">DESCRIPTION</span></span>
<span data-ttu-id="7cad1-106">O cmdlet **set-AzExpressRoutePortIdentity** atualiza um objeto ExpressRoutePort do Azure local.</span><span class="sxs-lookup"><span data-stu-id="7cad1-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="7cad1-107">Use **set-AzExpressRoutePort** para atribuí-lo ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7cad1-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="7cad1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cad1-108">EXAMPLES</span></span>

### <span data-ttu-id="7cad1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7cad1-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="7cad1-110">OS</span><span class="sxs-lookup"><span data-stu-id="7cad1-110">PARAMETERS</span></span>

### <span data-ttu-id="7cad1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cad1-111">-DefaultProfile</span></span>
<span data-ttu-id="7cad1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cad1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cad1-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7cad1-113">-ExpressRoutePort</span></span>
<span data-ttu-id="7cad1-114">O ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7cad1-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cad1-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7cad1-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7cad1-116">ResourceId da identidade atribuída pelo usuário a ser atribuído ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7cad1-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7cad1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7cad1-117">-Confirm</span></span>
<span data-ttu-id="7cad1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cad1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cad1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cad1-119">-WhatIf</span></span>
<span data-ttu-id="7cad1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7cad1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cad1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cad1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cad1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cad1-122">CommonParameters</span></span>
<span data-ttu-id="7cad1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cad1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cad1-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cad1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cad1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cad1-125">INPUTS</span></span>

### <span data-ttu-id="7cad1-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7cad1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="7cad1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7cad1-127">System.String</span></span>

## <span data-ttu-id="7cad1-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cad1-128">OUTPUTS</span></span>

### <span data-ttu-id="7cad1-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7cad1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7cad1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cad1-130">NOTES</span></span>

## <span data-ttu-id="7cad1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cad1-131">RELATED LINKS</span></span>
[<span data-ttu-id="7cad1-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7cad1-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7cad1-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7cad1-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7cad1-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7cad1-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
