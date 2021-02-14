---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116992"
---
# <span data-ttu-id="c32ee-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c32ee-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="c32ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c32ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c32ee-103">Importa um documento MOF como uma configuração de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="c32ee-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="c32ee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c32ee-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c32ee-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c32ee-105">DESCRIPTION</span></span>
<span data-ttu-id="c32ee-106">O cmdlet **Import-AzAutomationDscConfiguration** importa um documento de configuração de Formato de Objeto Gerenciado (MOF) para a Automação do Azure como uma configuração de nó DSC (Configuração de Estado Desejada).</span><span class="sxs-lookup"><span data-stu-id="c32ee-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="c32ee-107">Especifique o caminho de um arquivo .mof.</span><span class="sxs-lookup"><span data-stu-id="c32ee-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="c32ee-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c32ee-108">EXAMPLES</span></span>

### <span data-ttu-id="c32ee-109">Exemplo 1: Importar uma configuração de nó DSC para Automação</span><span class="sxs-lookup"><span data-stu-id="c32ee-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="c32ee-110">Esse comando importa uma configuração de nó DSC do arquivo chamado webserver.mof para a conta de Automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c32ee-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="c32ee-111">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="c32ee-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c32ee-112">Se houver uma configuração de nó DSC existente chamada ContosoConfiguration.webserver, esse comando a substituirá.</span><span class="sxs-lookup"><span data-stu-id="c32ee-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="c32ee-113">Exemplo 2: Importar uma configuração de nó DSC para Automação e criar uma nova versão de com build e não substituir nodeConfiguration existente.</span><span class="sxs-lookup"><span data-stu-id="c32ee-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="c32ee-114">Esse comando importa uma configuração de nó DSC do arquivo chamado webserver.mof para a conta de Automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c32ee-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="c32ee-115">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="c32ee-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c32ee-116">Se houver uma configuração de nó DSC existente chamada ContosoConfiguration.webserver, esse comando adiciona uma nova versão de com build com o nome ContosoConfiguration[2].webserver.</span><span class="sxs-lookup"><span data-stu-id="c32ee-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="c32ee-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c32ee-117">PARAMETERS</span></span>

### <span data-ttu-id="c32ee-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c32ee-118">-AutomationAccountName</span></span>
<span data-ttu-id="c32ee-119">Especifica o nome da conta automação para a qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="c32ee-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="c32ee-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c32ee-120">-ConfigurationName</span></span>
<span data-ttu-id="c32ee-121">Especifica o nome de uma configuração DSC em Automação a ser usada como namespace e contêiner para a configuração do nó a ser importada.</span><span class="sxs-lookup"><span data-stu-id="c32ee-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="c32ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32ee-122">-DefaultProfile</span></span>
<span data-ttu-id="c32ee-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c32ee-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c32ee-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c32ee-124">-Force</span></span>
<span data-ttu-id="c32ee-125">Indica que esse cmdlet substitui uma configuração de nó DSC existente em Automação.</span><span class="sxs-lookup"><span data-stu-id="c32ee-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="c32ee-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="c32ee-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="c32ee-127">Cria uma nova versão de com build de Configuração de Nó.</span><span class="sxs-lookup"><span data-stu-id="c32ee-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="c32ee-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c32ee-128">-Path</span></span>
<span data-ttu-id="c32ee-129">Especifica o caminho do documento de configuração MOF que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="c32ee-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c32ee-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32ee-130">-ResourceGroupName</span></span>
<span data-ttu-id="c32ee-131">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="c32ee-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="c32ee-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c32ee-132">-Confirm</span></span>
<span data-ttu-id="c32ee-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c32ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c32ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c32ee-134">-WhatIf</span></span>
<span data-ttu-id="c32ee-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c32ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c32ee-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c32ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c32ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32ee-137">CommonParameters</span></span>
<span data-ttu-id="c32ee-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32ee-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c32ee-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32ee-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="c32ee-140">INPUTS</span></span>

### <span data-ttu-id="c32ee-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c32ee-141">System.String</span></span>

## <span data-ttu-id="c32ee-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="c32ee-142">OUTPUTS</span></span>

### <span data-ttu-id="c32ee-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c32ee-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="c32ee-144">Notas</span><span class="sxs-lookup"><span data-stu-id="c32ee-144">NOTES</span></span>

## <span data-ttu-id="c32ee-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c32ee-145">RELATED LINKS</span></span>

[<span data-ttu-id="c32ee-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c32ee-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c32ee-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c32ee-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


