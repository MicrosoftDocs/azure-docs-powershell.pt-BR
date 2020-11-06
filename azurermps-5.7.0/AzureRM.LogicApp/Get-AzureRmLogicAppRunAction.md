---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: a4a9f95ec855137921e7e9318cdd52d81d8918f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426683"
---
# <span data-ttu-id="90ce7-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="90ce7-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="90ce7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="90ce7-103">Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="90ce7-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90ce7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90ce7-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ce7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="90ce7-106">O cmdlet **Get-AzureRmLogicAppRunAction** Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="90ce7-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="90ce7-107">Esse cmdlet retorna objetos **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="90ce7-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="90ce7-108">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="90ce7-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="90ce7-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="90ce7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="90ce7-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="90ce7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="90ce7-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="90ce7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="90ce7-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="90ce7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="90ce7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90ce7-113">EXAMPLES</span></span>

### <span data-ttu-id="90ce7-114">Exemplo 1: obter uma ação de um aplicativo lógico executado</span><span class="sxs-lookup"><span data-stu-id="90ce7-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="90ce7-115">Esse comando obtém uma ação específica do aplicativo lógico do aplicativo lógico chamado LogicApp05 para a execução nomeada LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="90ce7-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="90ce7-116">Exemplo 2: obter todas as ações de uma execução de aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="90ce7-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="90ce7-117">Esse comando obtém todas as ações da aplicação lógica de uma execução nomeada LogicAppRun56 de um aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="90ce7-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="90ce7-118">OS</span><span class="sxs-lookup"><span data-stu-id="90ce7-118">PARAMETERS</span></span>

### <span data-ttu-id="90ce7-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="90ce7-119">-ActionName</span></span>
<span data-ttu-id="90ce7-120">Especifica o nome de uma ação em um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="90ce7-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="90ce7-121">Esse cmdlet obtém a ação que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="90ce7-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ce7-122">-DefaultProfile</span></span>
<span data-ttu-id="90ce7-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="90ce7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90ce7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="90ce7-124">-Name</span></span>
<span data-ttu-id="90ce7-125">Especifica o nome de um aplicativo lógico para o qual esse cmdlet recebe uma ação.</span><span class="sxs-lookup"><span data-stu-id="90ce7-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="90ce7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ce7-126">-ResourceGroupName</span></span>
<span data-ttu-id="90ce7-127">Especifica o nome de um grupo de recursos em que esse cmdlet recebe uma ação.</span><span class="sxs-lookup"><span data-stu-id="90ce7-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="90ce7-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="90ce7-128">-RunName</span></span>
<span data-ttu-id="90ce7-129">Especifica o nome de uma execução de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="90ce7-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="90ce7-130">Esse cmdlet obtém uma ação para a execução que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="90ce7-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="90ce7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ce7-131">CommonParameters</span></span>
<span data-ttu-id="90ce7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ce7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ce7-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ce7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ce7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90ce7-134">INPUTS</span></span>

### <span data-ttu-id="90ce7-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="90ce7-135">None</span></span>
<span data-ttu-id="90ce7-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="90ce7-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90ce7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90ce7-137">OUTPUTS</span></span>

### <span data-ttu-id="90ce7-138">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="90ce7-138">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="90ce7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90ce7-139">NOTES</span></span>

## <span data-ttu-id="90ce7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90ce7-140">RELATED LINKS</span></span>

[<span data-ttu-id="90ce7-141">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="90ce7-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="90ce7-142">Parar-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="90ce7-142">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)

