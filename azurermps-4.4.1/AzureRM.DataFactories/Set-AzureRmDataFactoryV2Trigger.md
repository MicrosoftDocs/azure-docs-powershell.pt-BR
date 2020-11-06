---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 490965bf1edf39942272b9ef6caeb598b4e2d296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610815"
---
# <span data-ttu-id="8a096-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8a096-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8a096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a096-102">SYNOPSIS</span></span>
<span data-ttu-id="8a096-103">Cria um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8a096-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a096-104">SYNTAX</span></span>

### <span data-ttu-id="8a096-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a096-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a096-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a096-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a096-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a096-107">DESCRIPTION</span></span>
<span data-ttu-id="8a096-108">O cmdlet **set-AzureRmDataFactoryV2Trigger** cria um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8a096-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="8a096-109">Se você especificar um nome para um gatilho que já existe, o cmdlet solicitará confirmação antes de substituir o gatilho.</span><span class="sxs-lookup"><span data-stu-id="8a096-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="8a096-110">Se você especificar o parâmetro _Force_ , o cmdlet substituirá o gatilho existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8a096-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="8a096-111">Os gatilhos são criados no estado "interrompido", o que significa que eles não começam a invocar imediatamente os pipelines referenciados.</span><span class="sxs-lookup"><span data-stu-id="8a096-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="8a096-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a096-112">EXAMPLES</span></span>

### <span data-ttu-id="8a096-113">Exemplo 1: criar um gatilho</span><span class="sxs-lookup"><span data-stu-id="8a096-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="8a096-114">Crie um novo gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8a096-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="8a096-115">O gatilho é criado no estado "parado", o que significa que ele não é iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a096-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="8a096-116">Um gatilho pode ser iniciado usando o `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a096-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="8a096-117">OS</span><span class="sxs-lookup"><span data-stu-id="8a096-117">PARAMETERS</span></span>

### <span data-ttu-id="8a096-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a096-118">-Confirm</span></span>
<span data-ttu-id="8a096-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a096-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a096-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8a096-120">-DataFactoryName</span></span>
<span data-ttu-id="8a096-121">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8a096-121">The data factory name.</span></span>

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

### <span data-ttu-id="8a096-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8a096-122">-DefinitionFile</span></span>
<span data-ttu-id="8a096-123">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="8a096-123">The JSON file path.</span></span>

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

### <span data-ttu-id="8a096-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8a096-124">-Force</span></span>
<span data-ttu-id="8a096-125">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8a096-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8a096-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a096-126">-Name</span></span>
<span data-ttu-id="8a096-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="8a096-127">The trigger name.</span></span>

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

### <span data-ttu-id="8a096-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a096-128">-ResourceGroupName</span></span>
<span data-ttu-id="8a096-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a096-129">The resource group name.</span></span>

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

### <span data-ttu-id="8a096-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a096-130">-ResourceId</span></span>
<span data-ttu-id="8a096-131">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a096-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8a096-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a096-132">-WhatIf</span></span>
<span data-ttu-id="8a096-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a096-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8a096-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a096-134">-DefaultProfile</span></span>
<span data-ttu-id="8a096-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a096-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a096-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a096-136">CommonParameters</span></span>
<span data-ttu-id="8a096-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a096-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a096-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a096-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a096-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a096-139">INPUTS</span></span>

### <span data-ttu-id="8a096-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8a096-140">System.String</span></span>

## <span data-ttu-id="8a096-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a096-141">OUTPUTS</span></span>

### <span data-ttu-id="8a096-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8a096-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8a096-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a096-143">NOTES</span></span>

## <span data-ttu-id="8a096-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a096-144">RELATED LINKS</span></span>

[<span data-ttu-id="8a096-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8a096-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8a096-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8a096-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8a096-147">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8a096-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8a096-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8a096-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
