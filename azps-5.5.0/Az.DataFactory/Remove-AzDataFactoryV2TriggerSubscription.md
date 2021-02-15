---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118811"
---
# <span data-ttu-id="2c484-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="2c484-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="2c484-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c484-102">SYNOPSIS</span></span>
<span data-ttu-id="2c484-103">Cancelar a assinatura do gatilho do evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="2c484-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="2c484-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c484-104">SYNTAX</span></span>

### <span data-ttu-id="2c484-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="2c484-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c484-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c484-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c484-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c484-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c484-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c484-108">DESCRIPTION</span></span>
<span data-ttu-id="2c484-109">Esse comando cancela a assinatura do gatilho do evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2c484-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="2c484-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c484-110">EXAMPLES</span></span>

### <span data-ttu-id="2c484-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c484-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="2c484-112">Esse comando cancelará a assinatura do gatilho BlobEnetTriscribe1 para os eventos especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2c484-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="2c484-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c484-113">PARAMETERS</span></span>

### <span data-ttu-id="2c484-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c484-114">-DataFactoryName</span></span>
<span data-ttu-id="2c484-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2c484-115">The data factory name.</span></span>

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

### <span data-ttu-id="2c484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c484-116">-DefaultProfile</span></span>
<span data-ttu-id="2c484-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c484-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2c484-118">-Force</span></span>
<span data-ttu-id="2c484-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c484-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2c484-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c484-120">-InputObject</span></span>
<span data-ttu-id="2c484-121">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="2c484-121">The trigger object.</span></span>

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

### <span data-ttu-id="2c484-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c484-122">-Name</span></span>
<span data-ttu-id="2c484-123">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2c484-123">The trigger name.</span></span>

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

### <span data-ttu-id="2c484-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c484-124">-PassThru</span></span>
<span data-ttu-id="2c484-125">Se especificado, o cmdlet retornará verdadeiro na exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2c484-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="2c484-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c484-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c484-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c484-127">The resource group name.</span></span>

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

### <span data-ttu-id="2c484-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c484-128">-ResourceId</span></span>
<span data-ttu-id="2c484-129">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c484-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2c484-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2c484-130">-Confirm</span></span>
<span data-ttu-id="2c484-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c484-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c484-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c484-132">-WhatIf</span></span>
<span data-ttu-id="2c484-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2c484-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c484-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c484-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c484-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c484-135">CommonParameters</span></span>
<span data-ttu-id="2c484-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c484-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c484-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c484-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c484-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c484-138">INPUTS</span></span>

### <span data-ttu-id="2c484-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2c484-139">System.String</span></span>
<span data-ttu-id="2c484-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="2c484-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2c484-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c484-141">OUTPUTS</span></span>

### <span data-ttu-id="2c484-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriorySubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2c484-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="2c484-143">Notas</span><span class="sxs-lookup"><span data-stu-id="2c484-143">NOTES</span></span>

## <span data-ttu-id="2c484-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c484-144">RELATED LINKS</span></span>

