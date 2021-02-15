---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113001"
---
# <span data-ttu-id="60a84-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="60a84-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="60a84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60a84-102">SYNOPSIS</span></span>
<span data-ttu-id="60a84-103">Excluir registro de configuração</span><span class="sxs-lookup"><span data-stu-id="60a84-103">Delete Configuration record</span></span>

## <span data-ttu-id="60a84-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60a84-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a84-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="60a84-105">DESCRIPTION</span></span>
<span data-ttu-id="60a84-106">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="60a84-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="60a84-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60a84-107">EXAMPLES</span></span>

### <span data-ttu-id="60a84-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60a84-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="60a84-109">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="60a84-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="60a84-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60a84-110">PARAMETERS</span></span>

### <span data-ttu-id="60a84-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a84-111">-AsJob</span></span>
<span data-ttu-id="60a84-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="60a84-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60a84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a84-113">-DefaultProfile</span></span>
<span data-ttu-id="60a84-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60a84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a84-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="60a84-115">-Force</span></span>
<span data-ttu-id="60a84-116">Forçar a remoção sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="60a84-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="60a84-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="60a84-117">-Name</span></span>
<span data-ttu-id="60a84-118">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="60a84-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="60a84-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60a84-119">-PassThru</span></span>
<span data-ttu-id="60a84-120">Retorna o status da operação Remover.</span><span class="sxs-lookup"><span data-stu-id="60a84-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="60a84-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="60a84-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60a84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a84-122">-ResourceGroupName</span></span>
<span data-ttu-id="60a84-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60a84-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="60a84-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="60a84-124">-Confirm</span></span>
<span data-ttu-id="60a84-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a84-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a84-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a84-126">-WhatIf</span></span>
<span data-ttu-id="60a84-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="60a84-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a84-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60a84-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a84-129">CommonParameters</span></span>
<span data-ttu-id="60a84-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a84-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60a84-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a84-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="60a84-132">INPUTS</span></span>

### <span data-ttu-id="60a84-133">System.String</span><span class="sxs-lookup"><span data-stu-id="60a84-133">System.String</span></span>

## <span data-ttu-id="60a84-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="60a84-134">OUTPUTS</span></span>

### <span data-ttu-id="60a84-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60a84-135">System.Boolean</span></span>

## <span data-ttu-id="60a84-136">Notas</span><span class="sxs-lookup"><span data-stu-id="60a84-136">NOTES</span></span>

## <span data-ttu-id="60a84-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60a84-137">RELATED LINKS</span></span>
