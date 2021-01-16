---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260095"
---
# <span data-ttu-id="48b7b-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="48b7b-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="48b7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="48b7b-103">Compila uma configuração DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="48b7b-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="48b7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48b7b-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48b7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="48b7b-106">O cmdlet **Start-AzAutomationDscCompilationJob** compila uma configuração DSC (configuração de estado desejado APS) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="48b7b-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="48b7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="48b7b-108">Exemplo 1: compilar uma configuração DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="48b7b-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="48b7b-109">O primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="48b7b-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="48b7b-110">O segundo comando compila a configuração DSC chamada Config01.</span><span class="sxs-lookup"><span data-stu-id="48b7b-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="48b7b-111">O comando inclui os valores em $Params para parâmetros de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="48b7b-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="48b7b-112">Exemplo 2: compilar uma configuração DSC do Azure em automação com uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="48b7b-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="48b7b-113">Semelhante ao primeiro exemplo, o primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="48b7b-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="48b7b-114">O segundo comando compila a configuração DSC chamada Config01.</span><span class="sxs-lookup"><span data-stu-id="48b7b-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="48b7b-115">O comando inclui os valores em $Params para parâmetros de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="48b7b-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="48b7b-116">Ele não substitui a configuração de nó existente anterior criando uma nova configuração de nó com o nome Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="48b7b-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="48b7b-117">O número da versão é incrementado com base no número de versão existente já presente.</span><span class="sxs-lookup"><span data-stu-id="48b7b-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="48b7b-118">OS</span><span class="sxs-lookup"><span data-stu-id="48b7b-118">PARAMETERS</span></span>

### <span data-ttu-id="48b7b-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="48b7b-119">-AutomationAccountName</span></span>
<span data-ttu-id="48b7b-120">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="48b7b-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="48b7b-121">-ConfigurationData</span></span>
<span data-ttu-id="48b7b-122">Especifica um dicionário de dados de configuração para a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="48b7b-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="48b7b-123">-ConfigurationName</span></span>
<span data-ttu-id="48b7b-124">Especifica o nome da configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="48b7b-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b7b-125">-DefaultProfile</span></span>
<span data-ttu-id="48b7b-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48b7b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48b7b-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="48b7b-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="48b7b-128">Cria uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="48b7b-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-129">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b7b-129">-Parameters</span></span>
<span data-ttu-id="48b7b-130">Especifica um dicionário de parâmetros que esse cmdlet usa para compilar a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="48b7b-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b7b-131">-ResourceGroupName</span></span>
<span data-ttu-id="48b7b-132">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="48b7b-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b7b-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48b7b-133">-Confirm</span></span>
<span data-ttu-id="48b7b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b7b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b7b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b7b-135">-WhatIf</span></span>
<span data-ttu-id="48b7b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48b7b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48b7b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48b7b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b7b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b7b-138">CommonParameters</span></span>
<span data-ttu-id="48b7b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b7b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b7b-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b7b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b7b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48b7b-141">INPUTS</span></span>

### <span data-ttu-id="48b7b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="48b7b-142">System.String</span></span>

## <span data-ttu-id="48b7b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48b7b-143">OUTPUTS</span></span>

### <span data-ttu-id="48b7b-144">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="48b7b-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="48b7b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48b7b-145">NOTES</span></span>

## <span data-ttu-id="48b7b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48b7b-146">RELATED LINKS</span></span>

[<span data-ttu-id="48b7b-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="48b7b-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="48b7b-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="48b7b-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


