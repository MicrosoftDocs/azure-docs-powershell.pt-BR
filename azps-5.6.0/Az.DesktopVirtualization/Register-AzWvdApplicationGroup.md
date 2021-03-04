---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: ef1829dec7bdc1c3b41fa9e418246e1d9afcc1f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887143"
---
# <span data-ttu-id="46554-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="46554-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="46554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46554-102">SYNOPSIS</span></span>
<span data-ttu-id="46554-103">Registre um grupo de aplicativos de área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="46554-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="46554-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46554-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="46554-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46554-105">DESCRIPTION</span></span>
<span data-ttu-id="46554-106">Registre um grupo de aplicativos de área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="46554-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="46554-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46554-107">EXAMPLES</span></span>

### <span data-ttu-id="46554-108">Exemplo 1: Registrar um Grupo de Aplicativos de Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="46554-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="46554-109">Este comando registra um Grupo de Aplicativos de Área de Trabalho Virtual do Windows em um Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="46554-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="46554-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46554-110">PARAMETERS</span></span>

### <span data-ttu-id="46554-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="46554-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="46554-112">Caminho ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="46554-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="46554-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46554-113">-DefaultProfile</span></span>
<span data-ttu-id="46554-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46554-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46554-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46554-115">-ResourceGroupName</span></span>
<span data-ttu-id="46554-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="46554-116">Resource Group Name</span></span>

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

### <span data-ttu-id="46554-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46554-117">-SubscriptionId</span></span>
<span data-ttu-id="46554-118">Id da assinatura</span><span class="sxs-lookup"><span data-stu-id="46554-118">Subscription Id</span></span>

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

### <span data-ttu-id="46554-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46554-119">-WorkspaceName</span></span>
<span data-ttu-id="46554-120">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="46554-120">Workspace Name</span></span>

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

### <span data-ttu-id="46554-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46554-121">-Confirm</span></span>
<span data-ttu-id="46554-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46554-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46554-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46554-123">-WhatIf</span></span>
<span data-ttu-id="46554-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46554-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46554-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46554-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46554-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46554-126">CommonParameters</span></span>
<span data-ttu-id="46554-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46554-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46554-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46554-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46554-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46554-129">INPUTS</span></span>

## <span data-ttu-id="46554-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46554-130">OUTPUTS</span></span>

### <span data-ttu-id="46554-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="46554-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="46554-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="46554-132">NOTES</span></span>

<span data-ttu-id="46554-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="46554-133">ALIASES</span></span>

## <span data-ttu-id="46554-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46554-134">RELATED LINKS</span></span>

