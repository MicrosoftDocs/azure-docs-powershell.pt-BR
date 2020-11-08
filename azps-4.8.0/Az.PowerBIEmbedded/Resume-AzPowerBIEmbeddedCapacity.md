---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111958"
---
# <span data-ttu-id="d8ac1-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d8ac1-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d8ac1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ac1-103">Retoma uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d8ac1-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d8ac1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8ac1-104">SYNTAX</span></span>

### <span data-ttu-id="d8ac1-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8ac1-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ac1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8ac1-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ac1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8ac1-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ac1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8ac1-108">DESCRIPTION</span></span>
<span data-ttu-id="d8ac1-109">O cmdlet Resume-AzPowerBIEmbeddedCapacity retoma uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="d8ac1-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d8ac1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8ac1-110">EXAMPLES</span></span>

### <span data-ttu-id="d8ac1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8ac1-111">Example 1</span></span>
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

<span data-ttu-id="d8ac1-112">Esse comando retomará uma capacidade pausada chamada testcapacity no testRG do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8ac1-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="d8ac1-113">OS</span><span class="sxs-lookup"><span data-stu-id="d8ac1-113">PARAMETERS</span></span>

### <span data-ttu-id="d8ac1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ac1-114">-DefaultProfile</span></span>
<span data-ttu-id="d8ac1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ac1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ac1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8ac1-116">-InputObject</span></span>
<span data-ttu-id="d8ac1-117">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="d8ac1-117">Input object for Piping</span></span>

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

### <span data-ttu-id="d8ac1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8ac1-118">-Name</span></span>
<span data-ttu-id="d8ac1-119">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="d8ac1-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d8ac1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8ac1-120">-PassThru</span></span>
<span data-ttu-id="d8ac1-121">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="d8ac1-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d8ac1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ac1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8ac1-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="d8ac1-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="d8ac1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8ac1-124">-ResourceId</span></span>
<span data-ttu-id="d8ac1-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="d8ac1-125">Azure resource ID</span></span>

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

### <span data-ttu-id="d8ac1-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8ac1-126">-Confirm</span></span>
<span data-ttu-id="d8ac1-127">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="d8ac1-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d8ac1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ac1-128">-WhatIf</span></span>
<span data-ttu-id="d8ac1-129">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="d8ac1-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d8ac1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ac1-130">CommonParameters</span></span>
<span data-ttu-id="d8ac1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ac1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ac1-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ac1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ac1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8ac1-133">INPUTS</span></span>

### <span data-ttu-id="d8ac1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ac1-134">System.String</span></span>

### <span data-ttu-id="d8ac1-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d8ac1-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d8ac1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8ac1-136">OUTPUTS</span></span>

### <span data-ttu-id="d8ac1-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d8ac1-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d8ac1-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8ac1-138">NOTES</span></span>

## <span data-ttu-id="d8ac1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8ac1-139">RELATED LINKS</span></span>

[<span data-ttu-id="d8ac1-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d8ac1-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d8ac1-141">Suspender-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d8ac1-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
