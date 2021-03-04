---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 2cebdeab994926d51ff5ff49e6a4a101f3e5c778
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889657"
---
# <span data-ttu-id="cbf49-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbf49-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="cbf49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf49-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf49-103">Excluir registro de configuração</span><span class="sxs-lookup"><span data-stu-id="cbf49-103">Delete Configuration record</span></span>

## <span data-ttu-id="cbf49-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbf49-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf49-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbf49-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf49-106">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="cbf49-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="cbf49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbf49-107">EXAMPLES</span></span>

### <span data-ttu-id="cbf49-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbf49-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="cbf49-109">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="cbf49-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="cbf49-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbf49-110">PARAMETERS</span></span>

### <span data-ttu-id="cbf49-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbf49-111">-AsJob</span></span>
<span data-ttu-id="cbf49-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbf49-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf49-113">-DefaultProfile</span></span>
<span data-ttu-id="cbf49-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf49-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cbf49-115">-Force</span></span>
<span data-ttu-id="cbf49-116">Force remove sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="cbf49-116">Force remove without confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf49-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cbf49-117">-Name</span></span>
<span data-ttu-id="cbf49-118">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="cbf49-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf49-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf49-119">-PassThru</span></span>
<span data-ttu-id="cbf49-120">Retorna o status da operação Remover.</span><span class="sxs-lookup"><span data-stu-id="cbf49-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="cbf49-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cbf49-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf49-122">-ResourceGroupName</span></span>
<span data-ttu-id="cbf49-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbf49-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf49-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbf49-124">-Confirm</span></span>
<span data-ttu-id="cbf49-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf49-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf49-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf49-126">-WhatIf</span></span>
<span data-ttu-id="cbf49-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbf49-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf49-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbf49-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf49-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf49-129">CommonParameters</span></span>
<span data-ttu-id="cbf49-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf49-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf49-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbf49-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf49-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbf49-132">INPUTS</span></span>

### <span data-ttu-id="cbf49-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cbf49-133">System.String</span></span>

## <span data-ttu-id="cbf49-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbf49-134">OUTPUTS</span></span>

### <span data-ttu-id="cbf49-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbf49-135">System.Boolean</span></span>

## <span data-ttu-id="cbf49-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbf49-136">NOTES</span></span>

## <span data-ttu-id="cbf49-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbf49-137">RELATED LINKS</span></span>
