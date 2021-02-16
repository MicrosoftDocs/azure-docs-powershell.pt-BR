---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118261"
---
# <span data-ttu-id="7ac74-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ac74-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7ac74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ac74-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac74-103">Atualiza uma identidade atribuída a um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ac74-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="7ac74-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ac74-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac74-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ac74-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac74-106">O cmdlet **Set-AzExpressRoutePortIdentity** atualiza um objeto local do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ac74-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="7ac74-107">Use **Set-AzExpressRoutePort para** atribuí-lo ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ac74-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="7ac74-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ac74-108">EXAMPLES</span></span>

### <span data-ttu-id="7ac74-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ac74-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="7ac74-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ac74-110">PARAMETERS</span></span>

### <span data-ttu-id="7ac74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac74-111">-DefaultProfile</span></span>
<span data-ttu-id="7ac74-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ac74-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ac74-113">-ExpressRoutePort</span></span>
<span data-ttu-id="7ac74-114">O ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ac74-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="7ac74-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7ac74-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7ac74-116">ResourceId da identidade atribuída pelo usuário a ser atribuída ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ac74-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7ac74-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7ac74-117">-Confirm</span></span>
<span data-ttu-id="7ac74-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac74-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac74-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac74-119">-WhatIf</span></span>
<span data-ttu-id="7ac74-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7ac74-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac74-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ac74-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac74-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac74-122">CommonParameters</span></span>
<span data-ttu-id="7ac74-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac74-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac74-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac74-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac74-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ac74-125">INPUTS</span></span>

### <span data-ttu-id="7ac74-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ac74-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="7ac74-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7ac74-127">System.String</span></span>

## <span data-ttu-id="7ac74-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ac74-128">OUTPUTS</span></span>

### <span data-ttu-id="7ac74-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ac74-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7ac74-130">Notas</span><span class="sxs-lookup"><span data-stu-id="7ac74-130">NOTES</span></span>

## <span data-ttu-id="7ac74-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ac74-131">RELATED LINKS</span></span>
[<span data-ttu-id="7ac74-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ac74-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7ac74-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ac74-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7ac74-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ac74-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
