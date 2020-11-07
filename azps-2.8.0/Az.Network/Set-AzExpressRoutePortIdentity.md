---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 330264eaaffd9d81da2ed8dbcc7c892477ffb7e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772208"
---
# <span data-ttu-id="d2b1f-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b1f-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="d2b1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b1f-103">Atualiza uma identidade atribuída a um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="d2b1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2b1f-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b1f-106">O cmdlet **set-AzExpressRoutePortIdentity** atualiza um objeto ExpressRoutePort do Azure local.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="d2b1f-107">Use **set-AzExpressRoutePort** para atribuí-lo ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="d2b1f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2b1f-108">EXAMPLES</span></span>

### <span data-ttu-id="d2b1f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2b1f-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="d2b1f-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="d2b1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b1f-111">-DefaultProfile</span></span>
<span data-ttu-id="d2b1f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b1f-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d2b1f-113">-ExpressRoutePort</span></span>
<span data-ttu-id="d2b1f-114">O ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d2b1f-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="d2b1f-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="d2b1f-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="d2b1f-116">ResourceId da identidade atribuída pelo usuário a ser atribuído ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="d2b1f-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2b1f-117">-Confirm</span></span>
<span data-ttu-id="d2b1f-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2b1f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b1f-119">-WhatIf</span></span>
<span data-ttu-id="d2b1f-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2b1f-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2b1f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b1f-122">CommonParameters</span></span>
<span data-ttu-id="d2b1f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b1f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b1f-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b1f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b1f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2b1f-125">INPUTS</span></span>

### <span data-ttu-id="d2b1f-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d2b1f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="d2b1f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d2b1f-127">System.String</span></span>

## <span data-ttu-id="d2b1f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2b1f-128">OUTPUTS</span></span>

### <span data-ttu-id="d2b1f-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d2b1f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d2b1f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2b1f-130">NOTES</span></span>

## <span data-ttu-id="d2b1f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2b1f-131">RELATED LINKS</span></span>
[<span data-ttu-id="d2b1f-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b1f-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d2b1f-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b1f-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d2b1f-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d2b1f-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
