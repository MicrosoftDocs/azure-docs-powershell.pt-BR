---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 93c15d2675cc0e3e5fe0b37bc5af331ce97e7d8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885567"
---
# <span data-ttu-id="eccad-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eccad-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eccad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eccad-102">SYNOPSIS</span></span>
<span data-ttu-id="eccad-103">Exclui uma instância da Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="eccad-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="eccad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eccad-104">SYNTAX</span></span>

### <span data-ttu-id="eccad-105">ByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eccad-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eccad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eccad-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eccad-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eccad-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eccad-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eccad-108">DESCRIPTION</span></span>
<span data-ttu-id="eccad-109">O Remove-AzPowerBIEmbeddedCapacity cmdlet exclui uma instância da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="eccad-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="eccad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eccad-110">EXAMPLES</span></span>

### <span data-ttu-id="eccad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eccad-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="eccad-112">Este comando removerá a capacidade denominada testcapacity no testRG do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="eccad-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="eccad-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eccad-113">PARAMETERS</span></span>

### <span data-ttu-id="eccad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccad-114">-DefaultProfile</span></span>
<span data-ttu-id="eccad-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eccad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eccad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eccad-116">-InputObject</span></span>
<span data-ttu-id="eccad-117">Objeto Input for Piping</span><span class="sxs-lookup"><span data-stu-id="eccad-117">Input object for Piping</span></span>

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

### <span data-ttu-id="eccad-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eccad-118">-Name</span></span>
<span data-ttu-id="eccad-119">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="eccad-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="eccad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eccad-120">-PassThru</span></span>
<span data-ttu-id="eccad-121">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="eccad-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="eccad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccad-122">-ResourceGroupName</span></span>
<span data-ttu-id="eccad-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="eccad-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="eccad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eccad-124">-ResourceId</span></span>
<span data-ttu-id="eccad-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="eccad-125">Azure resource ID</span></span>

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

### <span data-ttu-id="eccad-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eccad-126">-Confirm</span></span>
<span data-ttu-id="eccad-127">Solicita que o usuário confirme se deve executar a operação</span><span class="sxs-lookup"><span data-stu-id="eccad-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="eccad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eccad-128">-WhatIf</span></span>
<span data-ttu-id="eccad-129">Descreve as ações que a operação atual executará sem realmente performá-las</span><span class="sxs-lookup"><span data-stu-id="eccad-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="eccad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccad-130">CommonParameters</span></span>
<span data-ttu-id="eccad-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eccad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccad-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eccad-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccad-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eccad-133">INPUTS</span></span>

### <span data-ttu-id="eccad-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eccad-134">System.String</span></span>

### <span data-ttu-id="eccad-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eccad-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eccad-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eccad-136">OUTPUTS</span></span>

### <span data-ttu-id="eccad-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eccad-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eccad-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="eccad-138">NOTES</span></span>

## <span data-ttu-id="eccad-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eccad-139">RELATED LINKS</span></span>

[<span data-ttu-id="eccad-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eccad-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="eccad-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eccad-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
