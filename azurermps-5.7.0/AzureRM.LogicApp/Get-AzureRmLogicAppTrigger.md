---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: f9f21689a894e46a9cd8d53d591d1cb17099fad8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428202"
---
# <span data-ttu-id="c3398-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="c3398-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="c3398-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3398-102">SYNOPSIS</span></span>
<span data-ttu-id="c3398-103">Obtém os gatilhos de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c3398-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3398-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3398-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3398-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3398-105">DESCRIPTION</span></span>
<span data-ttu-id="c3398-106">O cmdlet **Get-AzureRmLogicAppTrigger** Obtém gatilhos de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c3398-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="c3398-107">Esse cmdlet retorna um objeto **WorkflowTrigger** .</span><span class="sxs-lookup"><span data-stu-id="c3398-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="c3398-108">Especifique o fluxo de trabalho, o grupo de recursos e o gatilho.</span><span class="sxs-lookup"><span data-stu-id="c3398-108">Specify the workflow, resource group, and trigger.</span></span>

<span data-ttu-id="c3398-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c3398-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c3398-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c3398-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c3398-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c3398-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c3398-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="c3398-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c3398-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3398-113">EXAMPLES</span></span>

### <span data-ttu-id="c3398-114">Exemplo 1: obter um gatilho de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="c3398-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="c3398-115">Esse comando obtém o gatilho chamado Trigger01 do aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="c3398-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="c3398-116">Exemplo 2: obter todos os gatilhos de um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="c3398-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="c3398-117">Esse comando obtém os gatilhos do aplicativo lógico chamado LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="c3398-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="c3398-118">OS</span><span class="sxs-lookup"><span data-stu-id="c3398-118">PARAMETERS</span></span>

### <span data-ttu-id="c3398-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3398-119">-DefaultProfile</span></span>
<span data-ttu-id="c3398-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3398-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3398-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3398-121">-Name</span></span>
<span data-ttu-id="c3398-122">Especifica o nome do aplicativo lógico do qual esse cmdlet recebe um gatilho.</span><span class="sxs-lookup"><span data-stu-id="c3398-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3398-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3398-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3398-124">Especifica o nome de um grupo de recursos em que esse cmdlet recebe um gatilho.</span><span class="sxs-lookup"><span data-stu-id="c3398-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3398-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="c3398-125">-TriggerName</span></span>
<span data-ttu-id="c3398-126">Especifica o nome do gatilho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c3398-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3398-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3398-127">CommonParameters</span></span>
<span data-ttu-id="c3398-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3398-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3398-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3398-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3398-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3398-130">INPUTS</span></span>

### <span data-ttu-id="c3398-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c3398-131">None</span></span>
<span data-ttu-id="c3398-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c3398-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3398-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3398-133">OUTPUTS</span></span>

### <span data-ttu-id="c3398-134">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="c3398-134">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="c3398-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3398-135">NOTES</span></span>

## <span data-ttu-id="c3398-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3398-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3398-137">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c3398-137">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="c3398-138">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c3398-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


