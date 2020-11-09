---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280551"
---
# <span data-ttu-id="6473f-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6473f-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="6473f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6473f-102">SYNOPSIS</span></span>
<span data-ttu-id="6473f-103">Registrar um grupo de aplicativos de área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="6473f-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6473f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6473f-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6473f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6473f-105">DESCRIPTION</span></span>
<span data-ttu-id="6473f-106">Registrar um grupo de aplicativos de área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="6473f-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="6473f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6473f-107">EXAMPLES</span></span>

### <span data-ttu-id="6473f-108">Exemplo 1: registrar um grupo de aplicativos de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="6473f-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6473f-109">Esse comando registra um grupo de aplicativos de área de trabalho virtual do Windows em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6473f-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="6473f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6473f-110">PARAMETERS</span></span>

### <span data-ttu-id="6473f-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="6473f-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="6473f-112">Caminho ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="6473f-112">ApplicationGroupPath Path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6473f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6473f-113">-DefaultProfile</span></span>
<span data-ttu-id="6473f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6473f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6473f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6473f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6473f-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6473f-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6473f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6473f-117">-SubscriptionId</span></span>
<span data-ttu-id="6473f-118">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="6473f-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6473f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6473f-119">-WorkspaceName</span></span>
<span data-ttu-id="6473f-120">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="6473f-120">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6473f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6473f-121">-Confirm</span></span>
<span data-ttu-id="6473f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6473f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6473f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6473f-123">-WhatIf</span></span>
<span data-ttu-id="6473f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6473f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6473f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6473f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6473f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6473f-126">CommonParameters</span></span>
<span data-ttu-id="6473f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6473f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6473f-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6473f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6473f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6473f-129">INPUTS</span></span>

## <span data-ttu-id="6473f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6473f-130">OUTPUTS</span></span>

### <span data-ttu-id="6473f-131">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6473f-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="6473f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6473f-132">NOTES</span></span>

<span data-ttu-id="6473f-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6473f-133">ALIASES</span></span>

## <span data-ttu-id="6473f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6473f-134">RELATED LINKS</span></span>

