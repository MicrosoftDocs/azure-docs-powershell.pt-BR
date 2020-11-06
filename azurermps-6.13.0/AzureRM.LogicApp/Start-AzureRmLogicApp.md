---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: 316df4d265b32fc87388b701f096df61df246d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610303"
---
# <span data-ttu-id="3e6f1-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3e6f1-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="3e6f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6f1-103">Executa um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e6f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e6f1-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6f1-106">O cmdlet **Start-AzureRmLogicApp** executa um aplicativo lógico usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="3e6f1-107">Especifique um nome, um grupo de recursos e um gatilho.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="3e6f1-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3e6f1-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3e6f1-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3e6f1-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3e6f1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e6f1-112">EXAMPLES</span></span>

### <span data-ttu-id="3e6f1-113">Exemplo 1: executar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="3e6f1-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="3e6f1-114">Esse comando executa o aplicativo lógica no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3e6f1-115">OS</span><span class="sxs-lookup"><span data-stu-id="3e6f1-115">PARAMETERS</span></span>

### <span data-ttu-id="3e6f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6f1-116">-DefaultProfile</span></span>
<span data-ttu-id="3e6f1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3e6f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e6f1-118">-Name</span></span>
<span data-ttu-id="3e6f1-119">Especifica o nome do aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3e6f1-120">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e6f1-120">-Parameters</span></span>
<span data-ttu-id="3e6f1-121">Especifica um objeto da coleção Parameters do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="3e6f1-122">Especifique uma tabela de hash, dicionário \<string\> ou dicionário \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="3e6f1-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e6f1-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3e6f1-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="3e6f1-125">-TriggerName</span></span>
<span data-ttu-id="3e6f1-126">Especifica o nome do gatilho do aplicativo lógico que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3e6f1-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e6f1-127">-Confirm</span></span>
<span data-ttu-id="3e6f1-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6f1-129">-WhatIf</span></span>
<span data-ttu-id="3e6f1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6f1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6f1-132">CommonParameters</span></span>
<span data-ttu-id="3e6f1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6f1-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6f1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6f1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e6f1-135">INPUTS</span></span>

### <span data-ttu-id="3e6f1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3e6f1-136">System.String</span></span>

## <span data-ttu-id="3e6f1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e6f1-137">OUTPUTS</span></span>

### <span data-ttu-id="3e6f1-138">System. void</span><span class="sxs-lookup"><span data-stu-id="3e6f1-138">System.Void</span></span>

## <span data-ttu-id="3e6f1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e6f1-139">NOTES</span></span>

## <span data-ttu-id="3e6f1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e6f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e6f1-141">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3e6f1-141">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="3e6f1-142">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3e6f1-142">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="3e6f1-143">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3e6f1-143">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="3e6f1-144">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3e6f1-144">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="3e6f1-145">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3e6f1-145">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="3e6f1-146">Parar-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="3e6f1-146">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


