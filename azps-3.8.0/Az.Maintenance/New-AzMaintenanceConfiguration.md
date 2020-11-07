---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944220"
---
# <span data-ttu-id="53223-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53223-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="53223-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53223-102">SYNOPSIS</span></span>
<span data-ttu-id="53223-103">Criar ou atualizar o registro de configuração</span><span class="sxs-lookup"><span data-stu-id="53223-103">Create or Update configuration record</span></span>

## <span data-ttu-id="53223-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53223-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53223-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53223-105">DESCRIPTION</span></span>
<span data-ttu-id="53223-106">Criar ou atualizar o registro de configuração</span><span class="sxs-lookup"><span data-stu-id="53223-106">Create or Update configuration record</span></span>

## <span data-ttu-id="53223-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53223-107">EXAMPLES</span></span>

### <span data-ttu-id="53223-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53223-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="53223-109">Criar uma configuração de manutenção com o host de escopo</span><span class="sxs-lookup"><span data-stu-id="53223-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="53223-110">OS</span><span class="sxs-lookup"><span data-stu-id="53223-110">PARAMETERS</span></span>

### <span data-ttu-id="53223-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53223-111">-AsJob</span></span>
<span data-ttu-id="53223-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="53223-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53223-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53223-113">-DefaultProfile</span></span>
<span data-ttu-id="53223-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53223-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53223-115">-Extensionproperty</span><span class="sxs-lookup"><span data-stu-id="53223-115">-ExtensionProperty</span></span>
<span data-ttu-id="53223-116">As propriedades de extensão por recurso.</span><span class="sxs-lookup"><span data-stu-id="53223-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53223-117">-Local</span><span class="sxs-lookup"><span data-stu-id="53223-117">-Location</span></span>
<span data-ttu-id="53223-118">O local de configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="53223-118">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53223-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="53223-119">-MaintenanceScope</span></span>
<span data-ttu-id="53223-120">O escopo de manutenção.</span><span class="sxs-lookup"><span data-stu-id="53223-120">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53223-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="53223-121">-Name</span></span>
<span data-ttu-id="53223-122">O nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="53223-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="53223-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53223-123">-ResourceGroupName</span></span>
<span data-ttu-id="53223-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53223-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="53223-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="53223-125">-Tag</span></span>
<span data-ttu-id="53223-126">As marcas ARM.</span><span class="sxs-lookup"><span data-stu-id="53223-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53223-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53223-127">-Confirm</span></span>
<span data-ttu-id="53223-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53223-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53223-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53223-129">-WhatIf</span></span>
<span data-ttu-id="53223-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53223-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53223-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53223-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53223-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53223-132">CommonParameters</span></span>
<span data-ttu-id="53223-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53223-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53223-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53223-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53223-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53223-135">INPUTS</span></span>

### <span data-ttu-id="53223-136">System. String</span><span class="sxs-lookup"><span data-stu-id="53223-136">System.String</span></span>

## <span data-ttu-id="53223-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53223-137">OUTPUTS</span></span>

### <span data-ttu-id="53223-138">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53223-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="53223-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53223-139">NOTES</span></span>

## <span data-ttu-id="53223-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53223-140">RELATED LINKS</span></span>
