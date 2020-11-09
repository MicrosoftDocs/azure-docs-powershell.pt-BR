---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281094"
---
# <span data-ttu-id="89447-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="89447-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="89447-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89447-102">SYNOPSIS</span></span>
<span data-ttu-id="89447-103">Assine o gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="89447-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="89447-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89447-104">SYNTAX</span></span>

### <span data-ttu-id="89447-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="89447-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89447-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89447-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89447-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89447-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89447-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89447-108">DESCRIPTION</span></span>
<span data-ttu-id="89447-109">Esse comando assina o gatilho de evento para os eventos de serviço externo especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="89447-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="89447-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89447-110">EXAMPLES</span></span>

### <span data-ttu-id="89447-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89447-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="89447-112">Esse comando irá assinar o gatilho BlobEnetTrigger1 para os eventos especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="89447-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="89447-113">OS</span><span class="sxs-lookup"><span data-stu-id="89447-113">PARAMETERS</span></span>

### <span data-ttu-id="89447-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="89447-114">-DataFactoryName</span></span>
<span data-ttu-id="89447-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="89447-115">The data factory name.</span></span>

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

### <span data-ttu-id="89447-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89447-116">-DefaultProfile</span></span>
<span data-ttu-id="89447-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89447-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89447-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89447-118">-InputObject</span></span>
<span data-ttu-id="89447-119">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="89447-119">The trigger object.</span></span>

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

### <span data-ttu-id="89447-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="89447-120">-Name</span></span>
<span data-ttu-id="89447-121">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="89447-121">The trigger name.</span></span>

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

### <span data-ttu-id="89447-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89447-122">-ResourceGroupName</span></span>
<span data-ttu-id="89447-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89447-123">The resource group name.</span></span>

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

### <span data-ttu-id="89447-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89447-124">-ResourceId</span></span>
<span data-ttu-id="89447-125">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="89447-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="89447-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89447-126">-Confirm</span></span>
<span data-ttu-id="89447-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89447-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89447-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89447-128">-WhatIf</span></span>
<span data-ttu-id="89447-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89447-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89447-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89447-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89447-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89447-131">CommonParameters</span></span>
<span data-ttu-id="89447-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89447-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89447-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89447-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89447-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89447-134">INPUTS</span></span>

### <span data-ttu-id="89447-135">System. String</span><span class="sxs-lookup"><span data-stu-id="89447-135">System.String</span></span>
<span data-ttu-id="89447-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="89447-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="89447-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89447-137">OUTPUTS</span></span>

### <span data-ttu-id="89447-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="89447-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="89447-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89447-139">NOTES</span></span>

## <span data-ttu-id="89447-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89447-140">RELATED LINKS</span></span>

