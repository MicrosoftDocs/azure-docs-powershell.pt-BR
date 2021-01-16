---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263441"
---
# <span data-ttu-id="7dd1c-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="7dd1c-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="7dd1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd1c-103">Cancele a assinatura do gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="7dd1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dd1c-104">SYNTAX</span></span>

### <span data-ttu-id="7dd1c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7dd1c-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd1c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7dd1c-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dd1c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7dd1c-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd1c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dd1c-108">DESCRIPTION</span></span>
<span data-ttu-id="7dd1c-109">Esse comando cancela a assinatura do gatilho de evento para os eventos de serviço externo especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="7dd1c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dd1c-110">EXAMPLES</span></span>

### <span data-ttu-id="7dd1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dd1c-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="7dd1c-112">Esse comando cancelará a assinatura do gatilho BlobEnetTrigger1 para os eventos especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="7dd1c-113">OS</span><span class="sxs-lookup"><span data-stu-id="7dd1c-113">PARAMETERS</span></span>

### <span data-ttu-id="7dd1c-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7dd1c-114">-DataFactoryName</span></span>
<span data-ttu-id="7dd1c-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-115">The data factory name.</span></span>

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

### <span data-ttu-id="7dd1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd1c-116">-DefaultProfile</span></span>
<span data-ttu-id="7dd1c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd1c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7dd1c-118">-Force</span></span>
<span data-ttu-id="7dd1c-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7dd1c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dd1c-120">-InputObject</span></span>
<span data-ttu-id="7dd1c-121">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-121">The trigger object.</span></span>

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

### <span data-ttu-id="7dd1c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dd1c-122">-Name</span></span>
<span data-ttu-id="7dd1c-123">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-123">The trigger name.</span></span>

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

### <span data-ttu-id="7dd1c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dd1c-124">-PassThru</span></span>
<span data-ttu-id="7dd1c-125">Se especificado, o cmdlet retornará retornará true na exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="7dd1c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd1c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7dd1c-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-127">The resource group name.</span></span>

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

### <span data-ttu-id="7dd1c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dd1c-128">-ResourceId</span></span>
<span data-ttu-id="7dd1c-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7dd1c-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7dd1c-130">-Confirm</span></span>
<span data-ttu-id="7dd1c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd1c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd1c-132">-WhatIf</span></span>
<span data-ttu-id="7dd1c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd1c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd1c-135">CommonParameters</span></span>
<span data-ttu-id="7dd1c-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd1c-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd1c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd1c-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dd1c-138">INPUTS</span></span>

### <span data-ttu-id="7dd1c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd1c-139">System.String</span></span>
<span data-ttu-id="7dd1c-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7dd1c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7dd1c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dd1c-141">OUTPUTS</span></span>

### <span data-ttu-id="7dd1c-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7dd1c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="7dd1c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dd1c-143">NOTES</span></span>

## <span data-ttu-id="7dd1c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dd1c-144">RELATED LINKS</span></span>

