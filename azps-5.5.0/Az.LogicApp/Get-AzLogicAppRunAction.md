---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111809"
---
# <span data-ttu-id="e816c-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e816c-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="e816c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e816c-102">SYNOPSIS</span></span>

<span data-ttu-id="e816c-103">Obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e816c-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="e816c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e816c-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e816c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e816c-105">DESCRIPTION</span></span>

<span data-ttu-id="e816c-106">O **cmdlet Get-AzAppRunAction** obtém uma ação de um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e816c-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e816c-107">Este cmdlet retorna objetos **WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="e816c-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e816c-108">Especifique o aplicativo lógico, o grupo de recursos e execute.</span><span class="sxs-lookup"><span data-stu-id="e816c-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="e816c-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e816c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e816c-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="e816c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e816c-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e816c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e816c-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="e816c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e816c-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e816c-113">EXAMPLES</span></span>

### <span data-ttu-id="e816c-114">Exemplo 1: Executar uma ação de um aplicativo Lógico</span><span class="sxs-lookup"><span data-stu-id="e816c-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="e816c-115">Este comando obtém uma ação específica do Aplicativo Lógico do aplicativo lógico chamado LogicApp05 para a executar com o identificador 0858592518423369718380498702CU26.</span><span class="sxs-lookup"><span data-stu-id="e816c-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="e816c-116">Exemplo 2: Executar todas as ações de um Aplicativo Lógico</span><span class="sxs-lookup"><span data-stu-id="e816c-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="e816c-117">Esse comando obtém todas as ações do Aplicativo Lógico de uma executar com o identificador 08585925184423369718380498702CU26 de um aplicativo lógico chamado LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="e816c-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="e816c-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e816c-118">PARAMETERS</span></span>

### <span data-ttu-id="e816c-119">-Nomeda Ação</span><span class="sxs-lookup"><span data-stu-id="e816c-119">-ActionName</span></span>

<span data-ttu-id="e816c-120">Especifica o nome de uma ação em um aplicativo lógico executado.</span><span class="sxs-lookup"><span data-stu-id="e816c-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e816c-121">Este cmdlet obtém a ação especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e816c-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e816c-122">-DefaultProfile</span></span>

<span data-ttu-id="e816c-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e816c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="e816c-124">-FollowNextPageLink</span></span>

<span data-ttu-id="e816c-125">Indica que o cmdlet deve seguir os próximos links de página.</span><span class="sxs-lookup"><span data-stu-id="e816c-125">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="e816c-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="e816c-127">Especifica quantas vezes seguir os próximos links de página se o FollowNextPageLink for usado.</span><span class="sxs-lookup"><span data-stu-id="e816c-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e816c-128">-Name</span></span>

<span data-ttu-id="e816c-129">Especifica o nome de um aplicativo lógico para o qual este cmdlet obtém uma ação.</span><span class="sxs-lookup"><span data-stu-id="e816c-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e816c-130">-ResourceGroupName</span></span>

<span data-ttu-id="e816c-131">Especifica o nome de um grupo de recursos no qual este cmdlet obtém uma ação.</span><span class="sxs-lookup"><span data-stu-id="e816c-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="e816c-132">-RunName</span></span>

<span data-ttu-id="e816c-133">Especifica o nome de uma executar um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e816c-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e816c-134">Este cmdlet obtém uma ação para a executar especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e816c-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e816c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e816c-135">CommonParameters</span></span>

<span data-ttu-id="e816c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e816c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e816c-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e816c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e816c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="e816c-138">INPUTS</span></span>

### <span data-ttu-id="e816c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e816c-139">System.String</span></span>

## <span data-ttu-id="e816c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e816c-140">OUTPUTS</span></span>

### <span data-ttu-id="e816c-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e816c-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e816c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e816c-142">NOTES</span></span>

## <span data-ttu-id="e816c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e816c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e816c-144">Get-AzHistoryAppRun</span><span class="sxs-lookup"><span data-stu-id="e816c-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e816c-145">Stop-AzAppRun</span><span class="sxs-lookup"><span data-stu-id="e816c-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
