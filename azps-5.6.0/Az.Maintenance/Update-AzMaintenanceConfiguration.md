---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889656"
---
# <span data-ttu-id="f908c-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f908c-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="f908c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f908c-102">SYNOPSIS</span></span>
<span data-ttu-id="f908c-103">Registro de configuração de patch</span><span class="sxs-lookup"><span data-stu-id="f908c-103">Patch configuration record</span></span>

## <span data-ttu-id="f908c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f908c-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f908c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f908c-105">DESCRIPTION</span></span>
<span data-ttu-id="f908c-106">Registro de configuração de manutenção de patch</span><span class="sxs-lookup"><span data-stu-id="f908c-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f908c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f908c-107">EXAMPLES</span></span>

### <span data-ttu-id="f908c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f908c-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="f908c-109">Registro de configuração de manutenção de patch</span><span class="sxs-lookup"><span data-stu-id="f908c-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f908c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f908c-110">PARAMETERS</span></span>

### <span data-ttu-id="f908c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f908c-111">-AsJob</span></span>
<span data-ttu-id="f908c-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f908c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f908c-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="f908c-113">-Configuration</span></span>
<span data-ttu-id="f908c-114">A configuração de manutenção a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f908c-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f908c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f908c-115">-DefaultProfile</span></span>
<span data-ttu-id="f908c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f908c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f908c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f908c-117">-Name</span></span>
<span data-ttu-id="f908c-118">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="f908c-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="f908c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f908c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f908c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f908c-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="f908c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f908c-121">-Confirm</span></span>
<span data-ttu-id="f908c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f908c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f908c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f908c-123">-WhatIf</span></span>
<span data-ttu-id="f908c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f908c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f908c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f908c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f908c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f908c-126">CommonParameters</span></span>
<span data-ttu-id="f908c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f908c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f908c-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f908c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f908c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f908c-129">INPUTS</span></span>

### <span data-ttu-id="f908c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f908c-130">System.String</span></span>

### <span data-ttu-id="f908c-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f908c-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f908c-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f908c-132">OUTPUTS</span></span>

### <span data-ttu-id="f908c-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f908c-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f908c-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="f908c-134">NOTES</span></span>

## <span data-ttu-id="f908c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f908c-135">RELATED LINKS</span></span>
