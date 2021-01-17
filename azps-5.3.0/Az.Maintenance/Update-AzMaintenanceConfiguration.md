---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429763"
---
# <span data-ttu-id="f7597-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7597-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="f7597-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7597-102">SYNOPSIS</span></span>
<span data-ttu-id="f7597-103">Registro de configuração de patch</span><span class="sxs-lookup"><span data-stu-id="f7597-103">Patch configuration record</span></span>

## <span data-ttu-id="f7597-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7597-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7597-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7597-105">DESCRIPTION</span></span>
<span data-ttu-id="f7597-106">Registro de configuração de manutenção de patch</span><span class="sxs-lookup"><span data-stu-id="f7597-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f7597-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7597-107">EXAMPLES</span></span>

### <span data-ttu-id="f7597-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7597-108">Example 1</span></span>
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

<span data-ttu-id="f7597-109">Registro de configuração de manutenção de patch</span><span class="sxs-lookup"><span data-stu-id="f7597-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="f7597-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7597-110">PARAMETERS</span></span>

### <span data-ttu-id="f7597-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7597-111">-AsJob</span></span>
<span data-ttu-id="f7597-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f7597-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7597-113">-Configuração</span><span class="sxs-lookup"><span data-stu-id="f7597-113">-Configuration</span></span>
<span data-ttu-id="f7597-114">A configuração de manutenção a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f7597-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="f7597-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7597-115">-DefaultProfile</span></span>
<span data-ttu-id="f7597-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7597-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7597-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7597-117">-Name</span></span>
<span data-ttu-id="f7597-118">O nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="f7597-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="f7597-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7597-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7597-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7597-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="f7597-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f7597-121">-Confirm</span></span>
<span data-ttu-id="f7597-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7597-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7597-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7597-123">-WhatIf</span></span>
<span data-ttu-id="f7597-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7597-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7597-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7597-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7597-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7597-126">CommonParameters</span></span>
<span data-ttu-id="f7597-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7597-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7597-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7597-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7597-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7597-129">INPUTS</span></span>

### <span data-ttu-id="f7597-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7597-130">System.String</span></span>

### <span data-ttu-id="f7597-131">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7597-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f7597-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7597-132">OUTPUTS</span></span>

### <span data-ttu-id="f7597-133">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7597-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f7597-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7597-134">NOTES</span></span>

## <span data-ttu-id="f7597-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7597-135">RELATED LINKS</span></span>
