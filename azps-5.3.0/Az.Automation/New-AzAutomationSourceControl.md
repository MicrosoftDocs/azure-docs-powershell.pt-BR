---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430624"
---
# <span data-ttu-id="29fbf-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="29fbf-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="29fbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="29fbf-103">Cria um controle de fonte de automação.</span><span class="sxs-lookup"><span data-stu-id="29fbf-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="29fbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29fbf-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fbf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="29fbf-106">O cmdlet New-AzAutomationSourceControl cria uma configuração para vincular minha conta de automação do Azure com meu VSTS TFVC, VSTS git ou GitHub.</span><span class="sxs-lookup"><span data-stu-id="29fbf-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="29fbf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29fbf-107">EXAMPLES</span></span>

### <span data-ttu-id="29fbf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29fbf-108">Example 1</span></span>
<span data-ttu-id="29fbf-109">Crie uma configuração de controle de origem para vincular minha conta de automação do Azure ao meu projeto do VSTS TFVC.</span><span class="sxs-lookup"><span data-stu-id="29fbf-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="29fbf-110">Projetos TFVC não têm ramificações e, portanto, o parâmetro ramificação não é especificado.</span><span class="sxs-lookup"><span data-stu-id="29fbf-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="29fbf-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29fbf-111">Example 2</span></span>
<span data-ttu-id="29fbf-112">Crie uma configuração de controle de origem para vincular minha conta de automação do Azure ao meu projeto do VSTS git.</span><span class="sxs-lookup"><span data-stu-id="29fbf-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="29fbf-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="29fbf-113">Example 3</span></span>
<span data-ttu-id="29fbf-114">Crie uma configuração de controle de origem para vincular minha conta de automação do Azure ao meu projeto GitHub.</span><span class="sxs-lookup"><span data-stu-id="29fbf-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="29fbf-115">OS</span><span class="sxs-lookup"><span data-stu-id="29fbf-115">PARAMETERS</span></span>

### <span data-ttu-id="29fbf-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="29fbf-116">-AccessToken</span></span>
<span data-ttu-id="29fbf-117">O token de acesso de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29fbf-118">-AutomationAccountName</span></span>
<span data-ttu-id="29fbf-119">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="29fbf-119">The automation account name.</span></span>

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

### <span data-ttu-id="29fbf-120">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="29fbf-120">-Branch</span></span>
<span data-ttu-id="29fbf-121">Ramificação do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-121">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fbf-122">-DefaultProfile</span></span>
<span data-ttu-id="29fbf-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29fbf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fbf-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="29fbf-124">-Description</span></span>
<span data-ttu-id="29fbf-125">A descrição do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="29fbf-125">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="29fbf-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="29fbf-127">A propriedade publishRunbook do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="29fbf-128">Se DoNotPublishRunbook estiver definido, isso significa que os runbooks do usuário serão importados como ' rascunho '.</span><span class="sxs-lookup"><span data-stu-id="29fbf-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="29fbf-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="29fbf-129">-EnableAutoSync</span></span>
<span data-ttu-id="29fbf-130">A Propriedade AutoSync para o controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="29fbf-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="29fbf-131">-FolderPath</span></span>
<span data-ttu-id="29fbf-132">O caminho da pasta do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="29fbf-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="29fbf-133">-Name</span></span>
<span data-ttu-id="29fbf-134">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-135">-Rederramar</span><span class="sxs-lookup"><span data-stu-id="29fbf-135">-RepoUrl</span></span>
<span data-ttu-id="29fbf-136">A URL do repositório de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="29fbf-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fbf-137">-ResourceGroupName</span></span>
<span data-ttu-id="29fbf-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29fbf-138">The resource group name.</span></span>

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

### <span data-ttu-id="29fbf-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="29fbf-139">-SourceType</span></span>
<span data-ttu-id="29fbf-140">O tipo de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="29fbf-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fbf-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29fbf-141">-Confirm</span></span>
<span data-ttu-id="29fbf-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fbf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fbf-143">-WhatIf</span></span>
<span data-ttu-id="29fbf-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29fbf-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fbf-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29fbf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fbf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fbf-146">CommonParameters</span></span>
<span data-ttu-id="29fbf-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29fbf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fbf-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29fbf-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fbf-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29fbf-149">INPUTS</span></span>

### <span data-ttu-id="29fbf-150">System. String</span><span class="sxs-lookup"><span data-stu-id="29fbf-150">System.String</span></span>

## <span data-ttu-id="29fbf-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29fbf-151">OUTPUTS</span></span>

### <span data-ttu-id="29fbf-152">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="29fbf-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="29fbf-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29fbf-153">NOTES</span></span>

## <span data-ttu-id="29fbf-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29fbf-154">RELATED LINKS</span></span>
