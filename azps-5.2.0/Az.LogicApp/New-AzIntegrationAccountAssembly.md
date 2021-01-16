---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256868"
---
# <span data-ttu-id="2b418-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b418-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="2b418-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b418-102">SYNOPSIS</span></span>
<span data-ttu-id="2b418-103">Cria um assembly de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="2b418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b418-104">SYNTAX</span></span>

### <span data-ttu-id="2b418-105">ByIntegrationAccountAndFilePath (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b418-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="2b418-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b418-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="2b418-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b418-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="2b418-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="2b418-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="2b418-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="2b418-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="2b418-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b418-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="2b418-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b418-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b418-114">DESCRIPTION</span></span>
<span data-ttu-id="2b418-115">O cmdlet **Get-AzIntegrationAccountAssembly** cria um novo assembly em uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="2b418-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b418-116">EXAMPLES</span></span>

### <span data-ttu-id="2b418-117">Exemplo 1: criar um novo assembly usando um arquivo local</span><span class="sxs-lookup"><span data-stu-id="2b418-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="2b418-118">Cria um novo assembly usando o arquivo local localizado no caminho do arquivo contido em "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="2b418-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="2b418-119">Exemplo 2: criar um novo assembly usando dados de bytes</span><span class="sxs-lookup"><span data-stu-id="2b418-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="2b418-120">Cria um novo assembly usando a matriz de bytes contida em "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="2b418-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="2b418-121">Exemplo 3: criar um novo assembly usando um link de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2b418-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="2b418-122">Cria um novo assembly usando os dados de bytes localizados na URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="2b418-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="2b418-123">Esse é o método sugerido para a criação de conjuntos de grandes tamanhos.</span><span class="sxs-lookup"><span data-stu-id="2b418-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="2b418-124">OS</span><span class="sxs-lookup"><span data-stu-id="2b418-124">PARAMETERS</span></span>

### <span data-ttu-id="2b418-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="2b418-125">-AssemblyData</span></span>
<span data-ttu-id="2b418-126">A conta de integração assembly dados de bytes.</span><span class="sxs-lookup"><span data-stu-id="2b418-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="2b418-127">-AssemblyFilePath</span></span>
<span data-ttu-id="2b418-128">O caminho do arquivo de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="2b418-129">-ContentLink</span></span>
<span data-ttu-id="2b418-130">Um link publicamente acessível para os dados de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b418-131">-DefaultProfile</span></span>
<span data-ttu-id="2b418-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b418-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b418-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="2b418-133">-Metadata</span></span>
<span data-ttu-id="2b418-134">Os metadados de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b418-135">-Name</span></span>
<span data-ttu-id="2b418-136">O nome do assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="2b418-137">-ParentName</span></span>
<span data-ttu-id="2b418-138">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2b418-139">-ParentObject</span></span>
<span data-ttu-id="2b418-140">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2b418-141">-ParentResourceId</span></span>
<span data-ttu-id="2b418-142">A ID do recurso da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="2b418-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b418-143">-ResourceGroupName</span></span>
<span data-ttu-id="2b418-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b418-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b418-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b418-145">-Confirm</span></span>
<span data-ttu-id="2b418-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b418-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b418-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b418-147">-WhatIf</span></span>
<span data-ttu-id="2b418-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b418-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b418-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b418-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b418-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b418-150">CommonParameters</span></span>
<span data-ttu-id="2b418-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b418-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b418-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b418-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b418-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b418-153">INPUTS</span></span>

### <span data-ttu-id="2b418-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2b418-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="2b418-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2b418-155">System.String</span></span>

## <span data-ttu-id="2b418-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b418-156">OUTPUTS</span></span>

### <span data-ttu-id="2b418-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2b418-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="2b418-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b418-158">NOTES</span></span>

## <span data-ttu-id="2b418-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b418-159">RELATED LINKS</span></span>
