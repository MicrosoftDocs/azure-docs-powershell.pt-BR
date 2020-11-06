---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c99626e1323f10e98dcef1efc7ae622aab5f6b5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597092"
---
# <span data-ttu-id="4a565-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="4a565-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="4a565-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a565-102">SYNOPSIS</span></span>
<span data-ttu-id="4a565-103">Assine o gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="4a565-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="4a565-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a565-104">SYNTAX</span></span>

### <span data-ttu-id="4a565-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a565-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a565-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a565-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a565-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a565-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a565-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a565-108">DESCRIPTION</span></span>
<span data-ttu-id="4a565-109">Esse comando assina o gatilho de evento para os eventos de serviço externo especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="4a565-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="4a565-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a565-110">EXAMPLES</span></span>

### <span data-ttu-id="4a565-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a565-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="4a565-112">Esse comando irá assinar o gatilho BlobEnetTrigger1 para os eventos especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="4a565-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="4a565-113">OS</span><span class="sxs-lookup"><span data-stu-id="4a565-113">PARAMETERS</span></span>

### <span data-ttu-id="4a565-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4a565-114">-DataFactoryName</span></span>
<span data-ttu-id="4a565-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4a565-115">The data factory name.</span></span>

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

### <span data-ttu-id="4a565-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a565-116">-DefaultProfile</span></span>
<span data-ttu-id="4a565-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a565-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a565-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a565-118">-InputObject</span></span>
<span data-ttu-id="4a565-119">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="4a565-119">The trigger object.</span></span>

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

### <span data-ttu-id="4a565-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a565-120">-Name</span></span>
<span data-ttu-id="4a565-121">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="4a565-121">The trigger name.</span></span>

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

### <span data-ttu-id="4a565-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a565-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a565-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a565-123">The resource group name.</span></span>

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

### <span data-ttu-id="4a565-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a565-124">-ResourceId</span></span>
<span data-ttu-id="4a565-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="4a565-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4a565-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a565-126">-Confirm</span></span>
<span data-ttu-id="4a565-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a565-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a565-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a565-128">-WhatIf</span></span>
<span data-ttu-id="4a565-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a565-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a565-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a565-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a565-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a565-131">CommonParameters</span></span>
<span data-ttu-id="4a565-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a565-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a565-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a565-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a565-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a565-134">INPUTS</span></span>

### <span data-ttu-id="4a565-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4a565-135">System.String</span></span>
<span data-ttu-id="4a565-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4a565-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4a565-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a565-137">OUTPUTS</span></span>

### <span data-ttu-id="4a565-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4a565-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="4a565-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a565-139">NOTES</span></span>

## <span data-ttu-id="4a565-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a565-140">RELATED LINKS</span></span>

