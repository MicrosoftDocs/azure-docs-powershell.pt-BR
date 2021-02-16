---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117753"
---
# <span data-ttu-id="3ff32-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3ff32-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="3ff32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff32-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff32-103">Assine o gatilho do evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="3ff32-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3ff32-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ff32-104">SYNTAX</span></span>

### <span data-ttu-id="3ff32-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="3ff32-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ff32-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ff32-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff32-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff32-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff32-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff32-108">DESCRIPTION</span></span>
<span data-ttu-id="3ff32-109">Esse comando assina o gatilho do evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3ff32-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3ff32-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ff32-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff32-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ff32-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="3ff32-112">Esse comando assinará o gatilho BlobEnetTrigregação1 para os eventos especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3ff32-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="3ff32-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ff32-113">PARAMETERS</span></span>

### <span data-ttu-id="3ff32-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3ff32-114">-DataFactoryName</span></span>
<span data-ttu-id="3ff32-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3ff32-115">The data factory name.</span></span>

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

### <span data-ttu-id="3ff32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff32-116">-DefaultProfile</span></span>
<span data-ttu-id="3ff32-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff32-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff32-118">-InputObject</span></span>
<span data-ttu-id="3ff32-119">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="3ff32-119">The trigger object.</span></span>

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

### <span data-ttu-id="3ff32-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff32-120">-Name</span></span>
<span data-ttu-id="3ff32-121">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3ff32-121">The trigger name.</span></span>

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

### <span data-ttu-id="3ff32-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff32-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ff32-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ff32-123">The resource group name.</span></span>

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

### <span data-ttu-id="3ff32-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff32-124">-ResourceId</span></span>
<span data-ttu-id="3ff32-125">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff32-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3ff32-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3ff32-126">-Confirm</span></span>
<span data-ttu-id="3ff32-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff32-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff32-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff32-128">-WhatIf</span></span>
<span data-ttu-id="3ff32-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3ff32-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff32-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ff32-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff32-131">CommonParameters</span></span>
<span data-ttu-id="3ff32-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff32-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff32-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff32-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ff32-134">INPUTS</span></span>

### <span data-ttu-id="3ff32-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3ff32-135">System.String</span></span>
<span data-ttu-id="3ff32-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="3ff32-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3ff32-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ff32-137">OUTPUTS</span></span>

### <span data-ttu-id="3ff32-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriorySubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3ff32-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="3ff32-139">Notas</span><span class="sxs-lookup"><span data-stu-id="3ff32-139">NOTES</span></span>

## <span data-ttu-id="3ff32-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff32-140">RELATED LINKS</span></span>

