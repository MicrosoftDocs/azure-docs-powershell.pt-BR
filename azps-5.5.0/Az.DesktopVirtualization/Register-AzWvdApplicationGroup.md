---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117695"
---
# <span data-ttu-id="966ff-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="966ff-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="966ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="966ff-102">SYNOPSIS</span></span>
<span data-ttu-id="966ff-103">Registre um grupo de aplicativos da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="966ff-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="966ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="966ff-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="966ff-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="966ff-105">DESCRIPTION</span></span>
<span data-ttu-id="966ff-106">Registre um grupo de aplicativos da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="966ff-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="966ff-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="966ff-107">EXAMPLES</span></span>

### <span data-ttu-id="966ff-108">Exemplo 1: Registrar um Grupo de Aplicativos da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="966ff-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="966ff-109">Esse comando registra um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="966ff-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="966ff-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="966ff-110">PARAMETERS</span></span>

### <span data-ttu-id="966ff-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="966ff-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="966ff-112">Caminho ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="966ff-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="966ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966ff-113">-DefaultProfile</span></span>
<span data-ttu-id="966ff-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="966ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="966ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="966ff-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="966ff-116">Resource Group Name</span></span>

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

### <span data-ttu-id="966ff-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="966ff-117">-SubscriptionId</span></span>
<span data-ttu-id="966ff-118">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="966ff-118">Subscription Id</span></span>

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

### <span data-ttu-id="966ff-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="966ff-119">-WorkspaceName</span></span>
<span data-ttu-id="966ff-120">Nome do Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="966ff-120">Workspace Name</span></span>

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

### <span data-ttu-id="966ff-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="966ff-121">-Confirm</span></span>
<span data-ttu-id="966ff-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="966ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966ff-123">-WhatIf</span></span>
<span data-ttu-id="966ff-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="966ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="966ff-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="966ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966ff-126">CommonParameters</span></span>
<span data-ttu-id="966ff-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966ff-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="966ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966ff-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="966ff-129">INPUTS</span></span>

## <span data-ttu-id="966ff-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="966ff-130">OUTPUTS</span></span>

### <span data-ttu-id="966ff-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="966ff-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="966ff-132">Notas</span><span class="sxs-lookup"><span data-stu-id="966ff-132">NOTES</span></span>

<span data-ttu-id="966ff-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="966ff-133">ALIASES</span></span>

## <span data-ttu-id="966ff-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="966ff-134">RELATED LINKS</span></span>

