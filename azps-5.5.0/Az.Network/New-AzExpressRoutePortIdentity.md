---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114139"
---
# <span data-ttu-id="76155-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="76155-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="76155-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76155-102">SYNOPSIS</span></span>
<span data-ttu-id="76155-103">Cria um Azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="76155-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="76155-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76155-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76155-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="76155-105">DESCRIPTION</span></span>
<span data-ttu-id="76155-106">O cmdlet **New-AzExpressRoutePortIdentity cria** um objeto local de Identidade do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="76155-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="76155-107">Use **New-AzExpressRoutePort** **ou Set-AzExpressRoutePort** para atribuí-lo ao Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="76155-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="76155-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76155-108">EXAMPLES</span></span>

### <span data-ttu-id="76155-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76155-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="76155-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76155-110">PARAMETERS</span></span>

### <span data-ttu-id="76155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76155-111">-DefaultProfile</span></span>
<span data-ttu-id="76155-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76155-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76155-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="76155-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="76155-114">ResourceId da identidade atribuída pelo usuário a ser atribuída ao ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="76155-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="76155-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76155-115">-Confirm</span></span>
<span data-ttu-id="76155-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76155-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76155-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76155-117">-WhatIf</span></span>
<span data-ttu-id="76155-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76155-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76155-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76155-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76155-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76155-120">CommonParameters</span></span>
<span data-ttu-id="76155-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76155-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76155-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76155-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76155-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="76155-123">INPUTS</span></span>

### <span data-ttu-id="76155-124">System.String</span><span class="sxs-lookup"><span data-stu-id="76155-124">System.String</span></span>

## <span data-ttu-id="76155-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="76155-125">OUTPUTS</span></span>

### <span data-ttu-id="76155-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="76155-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="76155-127">Notas</span><span class="sxs-lookup"><span data-stu-id="76155-127">NOTES</span></span>

## <span data-ttu-id="76155-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76155-128">RELATED LINKS</span></span>
[<span data-ttu-id="76155-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="76155-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="76155-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="76155-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="76155-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="76155-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)