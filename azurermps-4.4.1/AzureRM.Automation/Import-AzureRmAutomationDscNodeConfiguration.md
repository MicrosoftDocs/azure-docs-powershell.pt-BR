---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 9c3fd17454381cf17604eb430588255b4889b3cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431184"
---
# <span data-ttu-id="46aca-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="46aca-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="46aca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46aca-102">SYNOPSIS</span></span>
<span data-ttu-id="46aca-103">Importa um documento MOF como uma configuração de nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="46aca-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46aca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46aca-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46aca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46aca-105">DESCRIPTION</span></span>
<span data-ttu-id="46aca-106">O cmdlet **Import-AzureRmAutomationDscConfiguration** importa um documento de configuração do MOF (Managed Object Format) para a automação do Azure como uma configuração de nó de configuração de estado desejado (DSC).</span><span class="sxs-lookup"><span data-stu-id="46aca-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="46aca-107">Especifique o caminho de um arquivo. mof.</span><span class="sxs-lookup"><span data-stu-id="46aca-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="46aca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46aca-108">EXAMPLES</span></span>

### <span data-ttu-id="46aca-109">Exemplo 1: importar uma configuração de nó DSC para automação</span><span class="sxs-lookup"><span data-stu-id="46aca-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="46aca-110">Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="46aca-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="46aca-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="46aca-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="46aca-112">Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando a substituirá.</span><span class="sxs-lookup"><span data-stu-id="46aca-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="46aca-113">Exemplo 2: importar uma configuração de nó DSC para automação e criar uma nova versão de compilação e não substituir NodeConfiguration existentes.</span><span class="sxs-lookup"><span data-stu-id="46aca-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="46aca-114">Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="46aca-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="46aca-115">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="46aca-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="46aca-116">Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando adicionará uma nova versão de compilação com o nome ContosoConfiguration [2]. WebServer.</span><span class="sxs-lookup"><span data-stu-id="46aca-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="46aca-117">OS</span><span class="sxs-lookup"><span data-stu-id="46aca-117">PARAMETERS</span></span>

### <span data-ttu-id="46aca-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="46aca-118">-AutomationAccountName</span></span>
<span data-ttu-id="46aca-119">Especifica o nome da conta de automação na qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="46aca-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="46aca-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="46aca-120">-ConfigurationName</span></span>
<span data-ttu-id="46aca-121">Especifica o nome de uma configuração DSC em automação para usar como o namespace e o contêiner para a configuração do nó a ser importada.</span><span class="sxs-lookup"><span data-stu-id="46aca-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="46aca-122">-Force</span><span class="sxs-lookup"><span data-stu-id="46aca-122">-Force</span></span>
<span data-ttu-id="46aca-123">Indica que esse cmdlet substitui uma configuração de nó DSC existente na automação.</span><span class="sxs-lookup"><span data-stu-id="46aca-123">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="46aca-124">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="46aca-124">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="46aca-125">Cria uma nova versão de compilação de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="46aca-125">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="46aca-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="46aca-126">-Path</span></span>
<span data-ttu-id="46aca-127">Especifica o caminho do documento de configuração do MOF que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="46aca-127">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="46aca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46aca-128">-ResourceGroupName</span></span>
<span data-ttu-id="46aca-129">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração de nó DSC.</span><span class="sxs-lookup"><span data-stu-id="46aca-129">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="46aca-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46aca-130">-Confirm</span></span>
<span data-ttu-id="46aca-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46aca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46aca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46aca-132">-WhatIf</span></span>
<span data-ttu-id="46aca-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46aca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46aca-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46aca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46aca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46aca-135">-DefaultProfile</span></span>
<span data-ttu-id="46aca-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46aca-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46aca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46aca-137">CommonParameters</span></span>
<span data-ttu-id="46aca-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46aca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46aca-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46aca-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46aca-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46aca-140">INPUTS</span></span>

## <span data-ttu-id="46aca-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46aca-141">OUTPUTS</span></span>

### <span data-ttu-id="46aca-142">Microsoft. Azure. Commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="46aca-142">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="46aca-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46aca-143">NOTES</span></span>

## <span data-ttu-id="46aca-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46aca-144">RELATED LINKS</span></span>

[<span data-ttu-id="46aca-145">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="46aca-145">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="46aca-146">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="46aca-146">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

