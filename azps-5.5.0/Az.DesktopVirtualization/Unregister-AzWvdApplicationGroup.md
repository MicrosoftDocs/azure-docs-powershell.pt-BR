---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115344"
---
# <span data-ttu-id="d16d9-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="d16d9-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="d16d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d16d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d16d9-103">Desosterre o grupo de aplicativos da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="d16d9-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="d16d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d16d9-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d16d9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d16d9-105">DESCRIPTION</span></span>
<span data-ttu-id="d16d9-106">Desosterre o grupo de aplicativos da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="d16d9-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="d16d9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d16d9-107">EXAMPLES</span></span>

### <span data-ttu-id="d16d9-108">Exemplo 1: Não registro em um Grupo de Aplicativos da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="d16d9-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="d16d9-109">Este comando desasterra um Grupo de Aplicativos da Área de Trabalho Virtual do Windows para um Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="d16d9-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="d16d9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d16d9-110">PARAMETERS</span></span>

### <span data-ttu-id="d16d9-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="d16d9-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="d16d9-112">Caminho ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16d9-112">ResourceGroupName Path</span></span>

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

### <span data-ttu-id="d16d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16d9-113">-DefaultProfile</span></span>
<span data-ttu-id="d16d9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d16d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d16d9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16d9-115">-ResourceGroupName</span></span>
<span data-ttu-id="d16d9-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d16d9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d16d9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d16d9-117">-SubscriptionId</span></span>
<span data-ttu-id="d16d9-118">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="d16d9-118">Subscription Id</span></span>

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

### <span data-ttu-id="d16d9-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d16d9-119">-WorkspaceName</span></span>
<span data-ttu-id="d16d9-120">Nome do Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d16d9-120">Workspace Name</span></span>

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

### <span data-ttu-id="d16d9-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d16d9-121">-Confirm</span></span>
<span data-ttu-id="d16d9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d16d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d16d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d16d9-123">-WhatIf</span></span>
<span data-ttu-id="d16d9-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d16d9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d16d9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d16d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d16d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16d9-126">CommonParameters</span></span>
<span data-ttu-id="d16d9-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16d9-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d16d9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16d9-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="d16d9-129">INPUTS</span></span>

## <span data-ttu-id="d16d9-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="d16d9-130">OUTPUTS</span></span>

### <span data-ttu-id="d16d9-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d16d9-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="d16d9-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d16d9-132">NOTES</span></span>

<span data-ttu-id="d16d9-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="d16d9-133">ALIASES</span></span>

## <span data-ttu-id="d16d9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d16d9-134">RELATED LINKS</span></span>

