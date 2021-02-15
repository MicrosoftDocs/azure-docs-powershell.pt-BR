---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114055"
---
# <span data-ttu-id="5c301-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5c301-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5c301-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c301-102">SYNOPSIS</span></span>
<span data-ttu-id="5c301-103">Retoma uma instância da Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="5c301-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="5c301-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c301-104">SYNTAX</span></span>

### <span data-ttu-id="5c301-105">ByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c301-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c301-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c301-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c301-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5c301-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c301-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c301-108">DESCRIPTION</span></span>
<span data-ttu-id="5c301-109">O Resume-AzPowerBIEmbeddedCapacity cmdlet retoma uma instância da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="5c301-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="5c301-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c301-110">EXAMPLES</span></span>

### <span data-ttu-id="5c301-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c301-111">Example 1</span></span>
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

<span data-ttu-id="5c301-112">Esse comando retomará uma capacidade pausada chamada testcapacity no testeRG do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c301-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="5c301-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c301-113">PARAMETERS</span></span>

### <span data-ttu-id="5c301-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c301-114">-DefaultProfile</span></span>
<span data-ttu-id="5c301-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c301-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c301-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c301-116">-InputObject</span></span>
<span data-ttu-id="5c301-117">Objeto de entrada para Piping</span><span class="sxs-lookup"><span data-stu-id="5c301-117">Input object for Piping</span></span>

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

### <span data-ttu-id="5c301-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c301-118">-Name</span></span>
<span data-ttu-id="5c301-119">Nome da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="5c301-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="5c301-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c301-120">-PassThru</span></span>
<span data-ttu-id="5c301-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5c301-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5c301-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c301-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c301-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="5c301-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="5c301-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c301-124">-ResourceId</span></span>
<span data-ttu-id="5c301-125">ID de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="5c301-125">Azure resource ID</span></span>

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

### <span data-ttu-id="5c301-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5c301-126">-Confirm</span></span>
<span data-ttu-id="5c301-127">Solicita que o usuário confirme se a operação será realizada</span><span class="sxs-lookup"><span data-stu-id="5c301-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="5c301-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c301-128">-WhatIf</span></span>
<span data-ttu-id="5c301-129">Descreve as ações que a operação atual executará sem realmente executa-las</span><span class="sxs-lookup"><span data-stu-id="5c301-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="5c301-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c301-130">CommonParameters</span></span>
<span data-ttu-id="5c301-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c301-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c301-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c301-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c301-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="5c301-133">INPUTS</span></span>

### <span data-ttu-id="5c301-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5c301-134">System.String</span></span>

### <span data-ttu-id="5c301-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5c301-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5c301-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="5c301-136">OUTPUTS</span></span>

### <span data-ttu-id="5c301-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5c301-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5c301-138">Notas</span><span class="sxs-lookup"><span data-stu-id="5c301-138">NOTES</span></span>

## <span data-ttu-id="5c301-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c301-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c301-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5c301-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="5c301-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5c301-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
