---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113278"
---
# <span data-ttu-id="a06a0-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a06a0-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="a06a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a06a0-102">SYNOPSIS</span></span>
<span data-ttu-id="a06a0-103">Cria um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a06a0-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="a06a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a06a0-104">SYNTAX</span></span>

### <span data-ttu-id="a06a0-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a06a0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a06a0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a06a0-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a06a0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a06a0-107">DESCRIPTION</span></span>
<span data-ttu-id="a06a0-108">O cmdlet **Set-AzDataFactoryV2Triory** cria um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a06a0-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="a06a0-109">Se você especificar um nome para um gatilho que já existe, o cmdlet solicitará confirmação antes de substituir o gatilho.</span><span class="sxs-lookup"><span data-stu-id="a06a0-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="a06a0-110">Se você especificar o _parâmetro Forçar,_ o cmdlet substituirá o gatilho existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a06a0-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="a06a0-111">Os gatilhos são criados no estado "Parado", o que significa que eles não começam imediatamente a invocar pipelines referenciados.</span><span class="sxs-lookup"><span data-stu-id="a06a0-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="a06a0-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a06a0-112">EXAMPLES</span></span>

### <span data-ttu-id="a06a0-113">Exemplo 1: Criar um gatilho</span><span class="sxs-lookup"><span data-stu-id="a06a0-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="a06a0-114">Crie um novo gatilho chamado "ScheduledTri wiki" no fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a06a0-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="a06a0-115">O gatilho é criado no estado "Parado", o que significa que ele não inicia imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a06a0-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="a06a0-116">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06a0-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="a06a0-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a06a0-117">PARAMETERS</span></span>

### <span data-ttu-id="a06a0-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a06a0-118">-DataFactoryName</span></span>
<span data-ttu-id="a06a0-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a06a0-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06a0-120">-DefaultProfile</span></span>
<span data-ttu-id="a06a0-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a06a0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a06a0-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a06a0-122">-DefinitionFile</span></span>
<span data-ttu-id="a06a0-123">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="a06a0-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a06a0-124">-Force</span></span>
<span data-ttu-id="a06a0-125">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a06a0-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a06a0-126">-Name</span></span>
<span data-ttu-id="a06a0-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a06a0-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="a06a0-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a06a0-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a06a0-130">-ResourceId</span></span>
<span data-ttu-id="a06a0-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="a06a0-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a06a0-132">-Confirm</span></span>
<span data-ttu-id="a06a0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06a0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06a0-134">-WhatIf</span></span>
<span data-ttu-id="a06a0-135">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06a0-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06a0-136">CommonParameters</span></span>
<span data-ttu-id="a06a0-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06a0-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06a0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06a0-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="a06a0-139">INPUTS</span></span>

### <span data-ttu-id="a06a0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a06a0-140">System.String</span></span>

## <span data-ttu-id="a06a0-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a06a0-141">OUTPUTS</span></span>

### <span data-ttu-id="a06a0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="a06a0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="a06a0-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a06a0-143">NOTES</span></span>

## <span data-ttu-id="a06a0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a06a0-144">RELATED LINKS</span></span>

[<span data-ttu-id="a06a0-145">Get-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="a06a0-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a06a0-146">Start-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="a06a0-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a06a0-147">Stop-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="a06a0-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a06a0-148">Remove-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="a06a0-148">Remove-AzDataFactoryV2Trigger</span></span>]()
