---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597709"
---
# <span data-ttu-id="0ca04-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="0ca04-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="0ca04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca04-103">Atualiza um controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca04-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="0ca04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ca04-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ca04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ca04-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca04-106">O cmdlet Update-AzAutomationSourceControl modifica o valor de um campo em um controle de origem na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca04-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="0ca04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ca04-107">EXAMPLES</span></span>

### <span data-ttu-id="0ca04-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ca04-108">Example 1</span></span>
<span data-ttu-id="0ca04-109">Esses comandos definem o campo PublishRunbook como false para o controle de origem de automação do Azure chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="0ca04-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="0ca04-110">OS</span><span class="sxs-lookup"><span data-stu-id="0ca04-110">PARAMETERS</span></span>

### <span data-ttu-id="0ca04-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="0ca04-111">-AccessToken</span></span>
<span data-ttu-id="0ca04-112">O token de acesso de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="0ca04-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca04-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ca04-113">-AutomationAccountName</span></span>
<span data-ttu-id="0ca04-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="0ca04-114">The automation account name.</span></span>

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

### <span data-ttu-id="0ca04-115">-Sincronização automática</span><span class="sxs-lookup"><span data-stu-id="0ca04-115">-AutoSync</span></span>
<span data-ttu-id="0ca04-116">A Propriedade AutoSync para o controle de origem.</span><span class="sxs-lookup"><span data-stu-id="0ca04-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca04-117">-Ramificação</span><span class="sxs-lookup"><span data-stu-id="0ca04-117">-Branch</span></span>
<span data-ttu-id="0ca04-118">Ramificação do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="0ca04-118">The source control branch.</span></span>

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

### <span data-ttu-id="0ca04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca04-119">-DefaultProfile</span></span>
<span data-ttu-id="0ca04-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca04-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ca04-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0ca04-121">-Description</span></span>
<span data-ttu-id="0ca04-122">A descrição do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="0ca04-122">The source control description.</span></span>

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

### <span data-ttu-id="0ca04-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="0ca04-123">-FolderPath</span></span>
<span data-ttu-id="0ca04-124">O caminho da pasta do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="0ca04-124">The source control folder path.</span></span>

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

### <span data-ttu-id="0ca04-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ca04-125">-Name</span></span>
<span data-ttu-id="0ca04-126">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="0ca04-126">The source control name.</span></span>

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

### <span data-ttu-id="0ca04-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="0ca04-127">-PublishRunbook</span></span>
<span data-ttu-id="0ca04-128">A propriedade publishRunbook do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="0ca04-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca04-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca04-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ca04-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ca04-130">The resource group name.</span></span>

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

### <span data-ttu-id="0ca04-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0ca04-131">-Confirm</span></span>
<span data-ttu-id="0ca04-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ca04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca04-133">-WhatIf</span></span>
<span data-ttu-id="0ca04-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0ca04-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ca04-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ca04-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca04-136">CommonParameters</span></span>
<span data-ttu-id="0ca04-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca04-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca04-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca04-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ca04-139">INPUTS</span></span>

### <span data-ttu-id="0ca04-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca04-140">System.String</span></span>

## <span data-ttu-id="0ca04-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ca04-141">OUTPUTS</span></span>

### <span data-ttu-id="0ca04-142">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="0ca04-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="0ca04-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ca04-143">NOTES</span></span>

## <span data-ttu-id="0ca04-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ca04-144">RELATED LINKS</span></span>
