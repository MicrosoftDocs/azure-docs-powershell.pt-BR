---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: cd0eab8d5670f8c37d45c8e0e211100749aa7a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901596"
---
# <span data-ttu-id="bfc72-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bfc72-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bfc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc72-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc72-103">Retoma uma instância da Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="bfc72-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bfc72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfc72-104">SYNTAX</span></span>

### <span data-ttu-id="bfc72-105">ByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bfc72-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc72-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc72-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc72-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bfc72-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc72-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfc72-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc72-109">O Resume-AzPowerBIEmbeddedCapacity cmdlet retoma uma instância da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="bfc72-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="bfc72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc72-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc72-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfc72-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="bfc72-112">Este comando retomará uma capacidade pausada denominada testcapacity no testRG do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bfc72-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="bfc72-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfc72-113">PARAMETERS</span></span>

### <span data-ttu-id="bfc72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc72-114">-DefaultProfile</span></span>
<span data-ttu-id="bfc72-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc72-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfc72-116">-InputObject</span></span>
<span data-ttu-id="bfc72-117">Objeto Input for Piping</span><span class="sxs-lookup"><span data-stu-id="bfc72-117">Input object for Piping</span></span>

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

### <span data-ttu-id="bfc72-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc72-118">-Name</span></span>
<span data-ttu-id="bfc72-119">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="bfc72-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="bfc72-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfc72-120">-PassThru</span></span>
<span data-ttu-id="bfc72-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bfc72-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bfc72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc72-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfc72-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="bfc72-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="bfc72-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc72-124">-ResourceId</span></span>
<span data-ttu-id="bfc72-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="bfc72-125">Azure resource ID</span></span>

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

### <span data-ttu-id="bfc72-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfc72-126">-Confirm</span></span>
<span data-ttu-id="bfc72-127">Solicita que o usuário confirme se deve executar a operação</span><span class="sxs-lookup"><span data-stu-id="bfc72-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="bfc72-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc72-128">-WhatIf</span></span>
<span data-ttu-id="bfc72-129">Descreve as ações que a operação atual executará sem realmente performá-las</span><span class="sxs-lookup"><span data-stu-id="bfc72-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="bfc72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc72-130">CommonParameters</span></span>
<span data-ttu-id="bfc72-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc72-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc72-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc72-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfc72-133">INPUTS</span></span>

### <span data-ttu-id="bfc72-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bfc72-134">System.String</span></span>

### <span data-ttu-id="bfc72-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bfc72-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bfc72-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfc72-136">OUTPUTS</span></span>

### <span data-ttu-id="bfc72-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bfc72-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bfc72-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfc72-138">NOTES</span></span>

## <span data-ttu-id="bfc72-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc72-139">RELATED LINKS</span></span>

[<span data-ttu-id="bfc72-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bfc72-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bfc72-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bfc72-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
