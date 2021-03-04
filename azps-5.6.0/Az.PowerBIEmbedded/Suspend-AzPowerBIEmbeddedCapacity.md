---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 54c546ed7bac74a13030a9ca2f18276761e2d381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890738"
---
# <span data-ttu-id="50824-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="50824-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="50824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50824-102">SYNOPSIS</span></span>
<span data-ttu-id="50824-103">Suspende uma instância da Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="50824-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="50824-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="50824-104">SYNTAX</span></span>

### <span data-ttu-id="50824-105">ByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="50824-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50824-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50824-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50824-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="50824-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50824-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="50824-108">DESCRIPTION</span></span>
<span data-ttu-id="50824-109">O cmdlet Suspend-AzPowerBIEmbeddedCapacity suspende uma instância da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="50824-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="50824-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50824-110">EXAMPLES</span></span>

### <span data-ttu-id="50824-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50824-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="50824-112">Este comando suspenderá uma capacidade ativa chamada testcapacity no grupo de recursos testgroup</span><span class="sxs-lookup"><span data-stu-id="50824-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="50824-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="50824-113">PARAMETERS</span></span>

### <span data-ttu-id="50824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50824-114">-DefaultProfile</span></span>
<span data-ttu-id="50824-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50824-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50824-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50824-116">-InputObject</span></span>
<span data-ttu-id="50824-117">Objeto Input for Piping</span><span class="sxs-lookup"><span data-stu-id="50824-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50824-118">-Name</span><span class="sxs-lookup"><span data-stu-id="50824-118">-Name</span></span>
<span data-ttu-id="50824-119">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="50824-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50824-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50824-120">-PassThru</span></span>
<span data-ttu-id="50824-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="50824-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="50824-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50824-122">-ResourceGroupName</span></span>
<span data-ttu-id="50824-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="50824-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50824-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50824-124">-ResourceId</span></span>
<span data-ttu-id="50824-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="50824-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50824-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50824-126">-Confirm</span></span>
<span data-ttu-id="50824-127">Solicita que o usuário confirme se deve executar a operação</span><span class="sxs-lookup"><span data-stu-id="50824-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="50824-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50824-128">-WhatIf</span></span>
<span data-ttu-id="50824-129">Descreve as ações que a operação atual executará sem realmente performá-las</span><span class="sxs-lookup"><span data-stu-id="50824-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="50824-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50824-130">CommonParameters</span></span>
<span data-ttu-id="50824-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50824-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50824-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50824-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50824-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50824-133">INPUTS</span></span>

### <span data-ttu-id="50824-134">System.String</span><span class="sxs-lookup"><span data-stu-id="50824-134">System.String</span></span>

### <span data-ttu-id="50824-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="50824-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="50824-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="50824-136">OUTPUTS</span></span>

### <span data-ttu-id="50824-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="50824-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="50824-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="50824-138">NOTES</span></span>

## <span data-ttu-id="50824-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50824-139">RELATED LINKS</span></span>

[<span data-ttu-id="50824-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="50824-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="50824-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="50824-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

