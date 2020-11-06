---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 790a0f0383796728b4754c4d64d98ef2ca7ed3c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428997"
---
# <span data-ttu-id="9d40c-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9d40c-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="9d40c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d40c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d40c-103">Compila uma configuração DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="9d40c-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d40c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d40c-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d40c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d40c-105">DESCRIPTION</span></span>
<span data-ttu-id="9d40c-106">O cmdlet **Start-AzureRmAutomationDscCompilationJob** compila uma configuração DSC (configuração de estado desejado APS) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d40c-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="9d40c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d40c-107">EXAMPLES</span></span>

### <span data-ttu-id="9d40c-108">Exemplo 1: compilar uma configuração DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="9d40c-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9d40c-109">O primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="9d40c-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="9d40c-110">O segundo comando compila a configuração DSC chamada Config01.</span><span class="sxs-lookup"><span data-stu-id="9d40c-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="9d40c-111">O comando inclui os valores em $Params para parâmetros de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="9d40c-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="9d40c-112">Exemplo 2: compilar uma configuração DSC do Azure em automação com uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="9d40c-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="9d40c-113">Semelhante ao primeiro exemplo, o primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="9d40c-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="9d40c-114">O segundo comando compila a configuração DSC chamada Config01.</span><span class="sxs-lookup"><span data-stu-id="9d40c-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="9d40c-115">O comando inclui os valores em $Params para parâmetros de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="9d40c-115">The command includes the values in $Params for DSC configuration parameters.</span></span>

<span data-ttu-id="9d40c-116">Ele não substitui a configuração de nó existente anterior criando uma nova configuração de nó com o nome Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="9d40c-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="9d40c-117">O número da versão é incrementado com base no número de versão existente já presente.</span><span class="sxs-lookup"><span data-stu-id="9d40c-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="9d40c-118">OS</span><span class="sxs-lookup"><span data-stu-id="9d40c-118">PARAMETERS</span></span>

### <span data-ttu-id="9d40c-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d40c-119">-AutomationAccountName</span></span>
<span data-ttu-id="9d40c-120">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="9d40c-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="9d40c-121">-ConfigurationData</span></span>
<span data-ttu-id="9d40c-122">Especifica um dicionário de dados de configuração para a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="9d40c-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9d40c-123">-ConfigurationName</span></span>
<span data-ttu-id="9d40c-124">Especifica o nome da configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="9d40c-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d40c-125">-DefaultProfile</span></span>
<span data-ttu-id="9d40c-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9d40c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d40c-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="9d40c-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="9d40c-128">Cria uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="9d40c-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-129">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d40c-129">-Parameters</span></span>
<span data-ttu-id="9d40c-130">Especifica um dicionário de parâmetros que esse cmdlet usa para compilar a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="9d40c-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d40c-131">-ResourceGroupName</span></span>
<span data-ttu-id="9d40c-132">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="9d40c-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d40c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d40c-133">-Confirm</span></span>
<span data-ttu-id="9d40c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d40c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d40c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d40c-135">-WhatIf</span></span>
<span data-ttu-id="9d40c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d40c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d40c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d40c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d40c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d40c-138">CommonParameters</span></span>
<span data-ttu-id="9d40c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d40c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d40c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d40c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d40c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d40c-141">INPUTS</span></span>

### <span data-ttu-id="9d40c-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d40c-142">None</span></span>
<span data-ttu-id="9d40c-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9d40c-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d40c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d40c-144">OUTPUTS</span></span>

### <span data-ttu-id="9d40c-145">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="9d40c-145">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="9d40c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d40c-146">NOTES</span></span>

## <span data-ttu-id="9d40c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d40c-147">RELATED LINKS</span></span>

[<span data-ttu-id="9d40c-148">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9d40c-148">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="9d40c-149">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9d40c-149">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


