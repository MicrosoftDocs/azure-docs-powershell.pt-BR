---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890637"
---
# <span data-ttu-id="d9dbb-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="d9dbb-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="d9dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9dbb-103">Assine o gatilho do evento para eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="d9dbb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d9dbb-104">SYNTAX</span></span>

### <span data-ttu-id="d9dbb-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d9dbb-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9dbb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9dbb-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9dbb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9dbb-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9dbb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d9dbb-108">DESCRIPTION</span></span>
<span data-ttu-id="d9dbb-109">Este comando assina o gatilho de evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="d9dbb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-110">EXAMPLES</span></span>

### <span data-ttu-id="d9dbb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9dbb-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="d9dbb-112">Este comando assinará o gatilho BlobEnetTrigger1 para os eventos especificados na definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="d9dbb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-113">PARAMETERS</span></span>

### <span data-ttu-id="d9dbb-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9dbb-114">-DataFactoryName</span></span>
<span data-ttu-id="d9dbb-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9dbb-116">-DefaultProfile</span></span>
<span data-ttu-id="d9dbb-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9dbb-118">-InputObject</span></span>
<span data-ttu-id="d9dbb-119">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d9dbb-120">-Name</span></span>
<span data-ttu-id="d9dbb-121">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9dbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9dbb-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9dbb-124">-ResourceId</span></span>
<span data-ttu-id="d9dbb-125">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9dbb-126">-Confirm</span></span>
<span data-ttu-id="d9dbb-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9dbb-128">-WhatIf</span></span>
<span data-ttu-id="d9dbb-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9dbb-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9dbb-131">CommonParameters</span></span>
<span data-ttu-id="d9dbb-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9dbb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9dbb-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9dbb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9dbb-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-134">INPUTS</span></span>

### <span data-ttu-id="d9dbb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d9dbb-135">System.String</span></span>
<span data-ttu-id="d9dbb-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d9dbb-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d9dbb-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-137">OUTPUTS</span></span>

### <span data-ttu-id="d9dbb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d9dbb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="d9dbb-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="d9dbb-139">NOTES</span></span>

## <span data-ttu-id="d9dbb-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9dbb-140">RELATED LINKS</span></span>

