---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 1ab801c9eca278d5d117ddca881867371882980c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891209"
---
# <span data-ttu-id="679d9-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="679d9-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="679d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679d9-102">SYNOPSIS</span></span>
<span data-ttu-id="679d9-103">Cancelar a assinatura do gatilho de eventos para eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="679d9-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="679d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="679d9-104">SYNTAX</span></span>

### <span data-ttu-id="679d9-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="679d9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="679d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="679d9-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679d9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="679d9-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679d9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="679d9-108">DESCRIPTION</span></span>
<span data-ttu-id="679d9-109">Esse comando cancela a assinatura do gatilho de evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="679d9-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="679d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="679d9-110">EXAMPLES</span></span>

### <span data-ttu-id="679d9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="679d9-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="679d9-112">Este comando cancelará a assinatura do gatilho BlobEnetTrigger1 para os eventos especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="679d9-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="679d9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="679d9-113">PARAMETERS</span></span>

### <span data-ttu-id="679d9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="679d9-114">-DataFactoryName</span></span>
<span data-ttu-id="679d9-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="679d9-115">The data factory name.</span></span>

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

### <span data-ttu-id="679d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679d9-116">-DefaultProfile</span></span>
<span data-ttu-id="679d9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="679d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679d9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="679d9-118">-Force</span></span>
<span data-ttu-id="679d9-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="679d9-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679d9-120">-InputObject</span></span>
<span data-ttu-id="679d9-121">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="679d9-121">The trigger object.</span></span>

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

### <span data-ttu-id="679d9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="679d9-122">-Name</span></span>
<span data-ttu-id="679d9-123">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="679d9-123">The trigger name.</span></span>

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

### <span data-ttu-id="679d9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="679d9-124">-PassThru</span></span>
<span data-ttu-id="679d9-125">Se especificado, o cmdlet retornará true na exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="679d9-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="679d9-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="679d9-127">The resource group name.</span></span>

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

### <span data-ttu-id="679d9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="679d9-128">-ResourceId</span></span>
<span data-ttu-id="679d9-129">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="679d9-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="679d9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="679d9-130">-Confirm</span></span>
<span data-ttu-id="679d9-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679d9-132">-WhatIf</span></span>
<span data-ttu-id="679d9-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="679d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679d9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="679d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679d9-135">CommonParameters</span></span>
<span data-ttu-id="679d9-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679d9-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679d9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679d9-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679d9-138">INPUTS</span></span>

### <span data-ttu-id="679d9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="679d9-139">System.String</span></span>
<span data-ttu-id="679d9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="679d9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="679d9-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="679d9-141">OUTPUTS</span></span>

### <span data-ttu-id="679d9-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="679d9-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="679d9-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="679d9-143">NOTES</span></span>

## <span data-ttu-id="679d9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="679d9-144">RELATED LINKS</span></span>

