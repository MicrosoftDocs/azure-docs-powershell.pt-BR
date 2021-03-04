---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885948"
---
# <span data-ttu-id="c5533-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="c5533-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="c5533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5533-102">SYNOPSIS</span></span>
<span data-ttu-id="c5533-103">Cria um controle de origem de automação.</span><span class="sxs-lookup"><span data-stu-id="c5533-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="c5533-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c5533-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5533-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c5533-105">DESCRIPTION</span></span>
<span data-ttu-id="c5533-106">O New-AzAutomationSourceControl cmdlet cria uma configuração para vincular minha conta de Automação do Azure com meu VSTS TFVC, VSTS Git ou GitHub.</span><span class="sxs-lookup"><span data-stu-id="c5533-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="c5533-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5533-107">EXAMPLES</span></span>

### <span data-ttu-id="c5533-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5533-108">Example 1</span></span>
<span data-ttu-id="c5533-109">Crie uma configuração de controle de origem para vincular minha conta de Automação do Azure com meu projeto TFVC VSTS.</span><span class="sxs-lookup"><span data-stu-id="c5533-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="c5533-110">Os projetos TFVC não têm ramificações e, portanto, o parâmetro Branch não é especificado.</span><span class="sxs-lookup"><span data-stu-id="c5533-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="c5533-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5533-111">Example 2</span></span>
<span data-ttu-id="c5533-112">Crie uma configuração de controle de origem para vincular minha conta de Automação do Azure com meu projeto VSTS Git.</span><span class="sxs-lookup"><span data-stu-id="c5533-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="c5533-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5533-113">Example 3</span></span>
<span data-ttu-id="c5533-114">Crie uma configuração de controle de origem para vincular minha conta de Automação do Azure ao meu projeto do GitHub.</span><span class="sxs-lookup"><span data-stu-id="c5533-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="c5533-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c5533-115">PARAMETERS</span></span>

### <span data-ttu-id="c5533-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="c5533-116">-AccessToken</span></span>
<span data-ttu-id="c5533-117">O token de acesso de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-117">The source control access token.</span></span>

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

### <span data-ttu-id="c5533-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5533-118">-AutomationAccountName</span></span>
<span data-ttu-id="c5533-119">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="c5533-119">The automation account name.</span></span>

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

### <span data-ttu-id="c5533-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="c5533-120">-Branch</span></span>
<span data-ttu-id="c5533-121">O branch de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-121">The source control branch.</span></span>

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

### <span data-ttu-id="c5533-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5533-122">-DefaultProfile</span></span>
<span data-ttu-id="c5533-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5533-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5533-124">-Description</span><span class="sxs-lookup"><span data-stu-id="c5533-124">-Description</span></span>
<span data-ttu-id="c5533-125">A descrição do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-125">The source control description.</span></span>

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

### <span data-ttu-id="c5533-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="c5533-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="c5533-127">A propriedade publishRunbook do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="c5533-128">Se DoNotPublishRunbook estiver definido, isso significa que os runbooks do usuário serão importados como 'Rascunho'.</span><span class="sxs-lookup"><span data-stu-id="c5533-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="c5533-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="c5533-129">-EnableAutoSync</span></span>
<span data-ttu-id="c5533-130">A propriedade autoSync para o controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="c5533-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="c5533-131">-FolderPath</span></span>
<span data-ttu-id="c5533-132">O caminho da pasta de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-132">The source control folder path.</span></span>

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

### <span data-ttu-id="c5533-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c5533-133">-Name</span></span>
<span data-ttu-id="c5533-134">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-134">The source control name.</span></span>

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

### <span data-ttu-id="c5533-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="c5533-135">-RepoUrl</span></span>
<span data-ttu-id="c5533-136">A url de repo do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-136">The source control repo url.</span></span>

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

### <span data-ttu-id="c5533-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5533-137">-ResourceGroupName</span></span>
<span data-ttu-id="c5533-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5533-138">The resource group name.</span></span>

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

### <span data-ttu-id="c5533-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c5533-139">-SourceType</span></span>
<span data-ttu-id="c5533-140">O tipo de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c5533-140">The source control type.</span></span>

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

### <span data-ttu-id="c5533-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5533-141">-Confirm</span></span>
<span data-ttu-id="c5533-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5533-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5533-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5533-143">-WhatIf</span></span>
<span data-ttu-id="c5533-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5533-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5533-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5533-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5533-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5533-146">CommonParameters</span></span>
<span data-ttu-id="c5533-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5533-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5533-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5533-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5533-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5533-149">INPUTS</span></span>

### <span data-ttu-id="c5533-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c5533-150">System.String</span></span>

## <span data-ttu-id="c5533-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c5533-151">OUTPUTS</span></span>

### <span data-ttu-id="c5533-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="c5533-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="c5533-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="c5533-153">NOTES</span></span>

## <span data-ttu-id="c5533-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5533-154">RELATED LINKS</span></span>
