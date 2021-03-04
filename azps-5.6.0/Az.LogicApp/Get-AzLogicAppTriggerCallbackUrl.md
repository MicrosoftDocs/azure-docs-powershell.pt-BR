---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 10408574a36018293fd15ef4f258ef4923f21d8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892765"
---
# <span data-ttu-id="def1e-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="def1e-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="def1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="def1e-102">SYNOPSIS</span></span>
<span data-ttu-id="def1e-103">Obtém uma URL de retorno de chamada de gatilho do Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="def1e-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="def1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="def1e-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="def1e-105">DESCRIPTION</span></span>
<span data-ttu-id="def1e-106">O cmdlet **Get-AzLogicAppTriggerCallbackUrl** obtém uma URL de retorno de chamada de gatilho do Aplicativo Lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="def1e-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="def1e-107">Este cmdlet retorna um **objeto WorkflowTriggerCallbackUrl** que representa a URL de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="def1e-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="def1e-108">Especifique o nome do grupo de recursos, o nome do aplicativo lógico e o nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="def1e-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="def1e-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="def1e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="def1e-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="def1e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="def1e-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="def1e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="def1e-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="def1e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="def1e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="def1e-113">EXAMPLES</span></span>

### <span data-ttu-id="def1e-114">Exemplo 1: Obter uma URL de retorno de chamada de gatilho do Aplicativo Lógico</span><span class="sxs-lookup"><span data-stu-id="def1e-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="def1e-115">Este comando obtém uma URL de retorno de chamada de gatilho do Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="def1e-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="def1e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="def1e-116">PARAMETERS</span></span>

### <span data-ttu-id="def1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def1e-117">-DefaultProfile</span></span>
<span data-ttu-id="def1e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="def1e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="def1e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="def1e-119">-Name</span></span>
<span data-ttu-id="def1e-120">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="def1e-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="def1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="def1e-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="def1e-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="def1e-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="def1e-123">-TriggerName</span></span>
<span data-ttu-id="def1e-124">Especifica o nome de um gatilho.</span><span class="sxs-lookup"><span data-stu-id="def1e-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="def1e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def1e-125">CommonParameters</span></span>
<span data-ttu-id="def1e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def1e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def1e-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def1e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def1e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="def1e-128">INPUTS</span></span>

### <span data-ttu-id="def1e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="def1e-129">System.String</span></span>

## <span data-ttu-id="def1e-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="def1e-130">OUTPUTS</span></span>

### <span data-ttu-id="def1e-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="def1e-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="def1e-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="def1e-132">NOTES</span></span>

## <span data-ttu-id="def1e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="def1e-133">RELATED LINKS</span></span>

[<span data-ttu-id="def1e-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="def1e-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


