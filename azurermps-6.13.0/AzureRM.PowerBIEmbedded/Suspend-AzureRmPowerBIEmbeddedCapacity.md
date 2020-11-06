---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602588"
---
# <span data-ttu-id="dcc23-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dcc23-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dcc23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcc23-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc23-103">Suspende uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="dcc23-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcc23-104">SYNTAX</span></span>

### <span data-ttu-id="dcc23-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcc23-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc23-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc23-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc23-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dcc23-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc23-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcc23-108">DESCRIPTION</span></span>
<span data-ttu-id="dcc23-109">O cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity suspende uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="dcc23-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="dcc23-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcc23-110">EXAMPLES</span></span>

### <span data-ttu-id="dcc23-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcc23-111">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="dcc23-112">Esse comando suspenderá uma capacidade ativa nomeada testcapacity no modo de teste do mymodo de origem</span><span class="sxs-lookup"><span data-stu-id="dcc23-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="dcc23-113">OS</span><span class="sxs-lookup"><span data-stu-id="dcc23-113">PARAMETERS</span></span>

### <span data-ttu-id="dcc23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc23-114">-DefaultProfile</span></span>
<span data-ttu-id="dcc23-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc23-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcc23-116">-InputObject</span></span>
<span data-ttu-id="dcc23-117">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="dcc23-117">Input object for Piping</span></span>

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

### <span data-ttu-id="dcc23-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcc23-118">-Name</span></span>
<span data-ttu-id="dcc23-119">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="dcc23-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="dcc23-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcc23-120">-PassThru</span></span>
<span data-ttu-id="dcc23-121">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="dcc23-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dcc23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc23-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcc23-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="dcc23-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="dcc23-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc23-124">-ResourceId</span></span>
<span data-ttu-id="dcc23-125">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="dcc23-125">Azure resource ID</span></span>

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

### <span data-ttu-id="dcc23-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcc23-126">-Confirm</span></span>
<span data-ttu-id="dcc23-127">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="dcc23-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dcc23-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc23-128">-WhatIf</span></span>
<span data-ttu-id="dcc23-129">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="dcc23-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dcc23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc23-130">CommonParameters</span></span>
<span data-ttu-id="dcc23-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc23-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc23-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc23-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcc23-133">INPUTS</span></span>

### <span data-ttu-id="dcc23-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc23-134">System.String</span></span>

### <span data-ttu-id="dcc23-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dcc23-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="dcc23-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dcc23-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dcc23-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcc23-137">OUTPUTS</span></span>

### <span data-ttu-id="dcc23-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dcc23-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dcc23-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcc23-139">NOTES</span></span>

## <span data-ttu-id="dcc23-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcc23-140">RELATED LINKS</span></span>

[<span data-ttu-id="dcc23-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dcc23-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="dcc23-142">Currículo-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dcc23-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

