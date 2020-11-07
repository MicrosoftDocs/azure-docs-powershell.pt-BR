---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943543"
---
# <span data-ttu-id="407a5-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="407a5-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="407a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="407a5-102">SYNOPSIS</span></span>
<span data-ttu-id="407a5-103">Retoma uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="407a5-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="407a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="407a5-104">SYNTAX</span></span>

### <span data-ttu-id="407a5-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="407a5-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="407a5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="407a5-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="407a5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="407a5-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="407a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="407a5-108">DESCRIPTION</span></span>
<span data-ttu-id="407a5-109">O cmdlet Resume-AzPowerBIEmbeddedCapacity retoma uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="407a5-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="407a5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="407a5-110">EXAMPLES</span></span>

### <span data-ttu-id="407a5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="407a5-111">Example 1</span></span>
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

<span data-ttu-id="407a5-112">Esse comando retomará uma capacidade pausada chamada testcapacity no testRG do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="407a5-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="407a5-113">OS</span><span class="sxs-lookup"><span data-stu-id="407a5-113">PARAMETERS</span></span>

### <span data-ttu-id="407a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407a5-114">-DefaultProfile</span></span>
<span data-ttu-id="407a5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="407a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="407a5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="407a5-116">-InputObject</span></span>
<span data-ttu-id="407a5-117">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="407a5-117">Input object for Piping</span></span>

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

### <span data-ttu-id="407a5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="407a5-118">-Name</span></span>
<span data-ttu-id="407a5-119">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="407a5-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="407a5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="407a5-120">-PassThru</span></span>
<span data-ttu-id="407a5-121">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="407a5-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="407a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="407a5-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="407a5-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="407a5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="407a5-124">-ResourceId</span></span>
<span data-ttu-id="407a5-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="407a5-125">Azure resource ID</span></span>

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

### <span data-ttu-id="407a5-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="407a5-126">-Confirm</span></span>
<span data-ttu-id="407a5-127">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="407a5-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="407a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="407a5-128">-WhatIf</span></span>
<span data-ttu-id="407a5-129">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="407a5-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="407a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407a5-130">CommonParameters</span></span>
<span data-ttu-id="407a5-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="407a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407a5-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="407a5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407a5-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="407a5-133">INPUTS</span></span>

### <span data-ttu-id="407a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="407a5-134">System.String</span></span>

### <span data-ttu-id="407a5-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="407a5-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="407a5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="407a5-136">OUTPUTS</span></span>

### <span data-ttu-id="407a5-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="407a5-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="407a5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="407a5-138">NOTES</span></span>

## <span data-ttu-id="407a5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="407a5-139">RELATED LINKS</span></span>

[<span data-ttu-id="407a5-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="407a5-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="407a5-141">Suspender-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="407a5-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
