---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432806"
---
# <span data-ttu-id="671e1-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="671e1-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="671e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="671e1-102">SYNOPSIS</span></span>
<span data-ttu-id="671e1-103">Importa um documento MOF como uma configuração de nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="671e1-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="671e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="671e1-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="671e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="671e1-105">DESCRIPTION</span></span>
<span data-ttu-id="671e1-106">O cmdlet **Import-AzureRmAutomationDscConfiguration** importa um documento de configuração do MOF (Managed Object Format) para a automação do Azure como uma configuração de nó de configuração de estado desejado (DSC).</span><span class="sxs-lookup"><span data-stu-id="671e1-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="671e1-107">Especifique o caminho de um arquivo. mof.</span><span class="sxs-lookup"><span data-stu-id="671e1-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="671e1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="671e1-108">EXAMPLES</span></span>

### <span data-ttu-id="671e1-109">Exemplo 1: importar uma configuração de nó DSC para automação</span><span class="sxs-lookup"><span data-stu-id="671e1-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="671e1-110">Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="671e1-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="671e1-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="671e1-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="671e1-112">Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando a substituirá.</span><span class="sxs-lookup"><span data-stu-id="671e1-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="671e1-113">Exemplo 2: importar uma configuração de nó DSC para automação e criar uma nova versão de compilação e não substituir NodeConfiguration existentes.</span><span class="sxs-lookup"><span data-stu-id="671e1-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="671e1-114">Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="671e1-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="671e1-115">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="671e1-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="671e1-116">Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando adicionará uma nova versão de compilação com o nome ContosoConfiguration [2]. WebServer.</span><span class="sxs-lookup"><span data-stu-id="671e1-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="671e1-117">OS</span><span class="sxs-lookup"><span data-stu-id="671e1-117">PARAMETERS</span></span>

### <span data-ttu-id="671e1-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="671e1-118">-AutomationAccountName</span></span>
<span data-ttu-id="671e1-119">Especifica o nome da conta de automação na qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="671e1-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="671e1-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="671e1-120">-ConfigurationName</span></span>
<span data-ttu-id="671e1-121">Especifica o nome de uma configuração DSC em automação para usar como o namespace e o contêiner para a configuração do nó a ser importada.</span><span class="sxs-lookup"><span data-stu-id="671e1-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="671e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671e1-122">-DefaultProfile</span></span>
<span data-ttu-id="671e1-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="671e1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="671e1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="671e1-124">-Force</span></span>
<span data-ttu-id="671e1-125">Indica que esse cmdlet substitui uma configuração de nó DSC existente na automação.</span><span class="sxs-lookup"><span data-stu-id="671e1-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="671e1-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="671e1-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="671e1-127">Cria uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="671e1-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="671e1-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="671e1-128">-Path</span></span>
<span data-ttu-id="671e1-129">Especifica o caminho do documento de configuração do MOF que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="671e1-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="671e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="671e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="671e1-131">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="671e1-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="671e1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="671e1-132">-Confirm</span></span>
<span data-ttu-id="671e1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="671e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="671e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="671e1-134">-WhatIf</span></span>
<span data-ttu-id="671e1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="671e1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="671e1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="671e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="671e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671e1-137">CommonParameters</span></span>
<span data-ttu-id="671e1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="671e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671e1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="671e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671e1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="671e1-140">INPUTS</span></span>

### <span data-ttu-id="671e1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="671e1-141">System.String</span></span>

## <span data-ttu-id="671e1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="671e1-142">OUTPUTS</span></span>

### <span data-ttu-id="671e1-143">Microsoft. Azure. Commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="671e1-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="671e1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="671e1-144">NOTES</span></span>

## <span data-ttu-id="671e1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="671e1-145">RELATED LINKS</span></span>

[<span data-ttu-id="671e1-146">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="671e1-146">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="671e1-147">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="671e1-147">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


