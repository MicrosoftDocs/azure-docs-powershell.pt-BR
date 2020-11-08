---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111686"
---
# <span data-ttu-id="185d5-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="185d5-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="185d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="185d5-102">SYNOPSIS</span></span>
<span data-ttu-id="185d5-103">Obtém um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="185d5-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="185d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="185d5-104">SYNTAX</span></span>

### <span data-ttu-id="185d5-105">ListWorkflows (padrão)</span><span class="sxs-lookup"><span data-stu-id="185d5-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="185d5-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="185d5-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="185d5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="185d5-107">DESCRIPTION</span></span>
<span data-ttu-id="185d5-108">O cmdlet **Get-AzLogicApp** Obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="185d5-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="185d5-109">Esse cmdlet retorna um objeto de **fluxo de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="185d5-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="185d5-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="185d5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="185d5-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="185d5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="185d5-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="185d5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="185d5-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="185d5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="185d5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="185d5-114">EXAMPLES</span></span>

### <span data-ttu-id="185d5-115">Exemplo 1: obter um aplicativo lógico de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="185d5-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="185d5-116">Esse comando obtém um aplicativo lógico do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="185d5-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="185d5-117">OS</span><span class="sxs-lookup"><span data-stu-id="185d5-117">PARAMETERS</span></span>

### <span data-ttu-id="185d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185d5-118">-DefaultProfile</span></span>
<span data-ttu-id="185d5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="185d5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="185d5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="185d5-120">-Name</span></span>
<span data-ttu-id="185d5-121">Especifica o nome do aplicativo lógico que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="185d5-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="185d5-123">Especifica o nome de um grupo de recursos em que esse cmdlet obtém um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="185d5-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185d5-124">-Versão</span><span class="sxs-lookup"><span data-stu-id="185d5-124">-Version</span></span>
<span data-ttu-id="185d5-125">Especifica a versão de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="185d5-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185d5-126">CommonParameters</span></span>
<span data-ttu-id="185d5-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185d5-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185d5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185d5-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="185d5-129">INPUTS</span></span>

### <span data-ttu-id="185d5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="185d5-130">System.String</span></span>

## <span data-ttu-id="185d5-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="185d5-131">OUTPUTS</span></span>

### <span data-ttu-id="185d5-132">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="185d5-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="185d5-133">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="185d5-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="185d5-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="185d5-134">NOTES</span></span>

## <span data-ttu-id="185d5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="185d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="185d5-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="185d5-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="185d5-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="185d5-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="185d5-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="185d5-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="185d5-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="185d5-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


