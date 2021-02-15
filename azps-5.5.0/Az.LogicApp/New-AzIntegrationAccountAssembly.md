---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111808"
---
# <span data-ttu-id="0a305-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a305-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="0a305-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a305-102">SYNOPSIS</span></span>
<span data-ttu-id="0a305-103">Cria uma montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="0a305-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a305-104">SYNTAX</span></span>

### <span data-ttu-id="0a305-105">ByIntegrationAccountAndFilePath (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0a305-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="0a305-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a305-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="0a305-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a305-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="0a305-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="0a305-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="0a305-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="0a305-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="0a305-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a305-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="0a305-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a305-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a305-114">DESCRIPTION</span></span>
<span data-ttu-id="0a305-115">O cmdlet **Get-AzIntegrationAccountAssembly** cria uma nova montagem em uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="0a305-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a305-116">EXAMPLES</span></span>

### <span data-ttu-id="0a305-117">Exemplo 1: Criar nova montagem usando o arquivo local</span><span class="sxs-lookup"><span data-stu-id="0a305-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0a305-118">Cria uma nova montagem usando o arquivo local localizado no caminho de arquivo contido em "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="0a305-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="0a305-119">Exemplo 2: Criar nova montagem usando dados de byte</span><span class="sxs-lookup"><span data-stu-id="0a305-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0a305-120">Cria uma nova montagem usando a matriz byte contida em "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="0a305-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="0a305-121">Exemplo 3: Criar nova montagem usando um link de conteúdo</span><span class="sxs-lookup"><span data-stu-id="0a305-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="0a305-122">Cria uma nova montagem usando os dados de um byte localizados na URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="0a305-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="0a305-123">Este é o método sugerido para criar grandes conjuntos de tamanhos.</span><span class="sxs-lookup"><span data-stu-id="0a305-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="0a305-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a305-124">PARAMETERS</span></span>

### <span data-ttu-id="0a305-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="0a305-125">-AssemblyData</span></span>
<span data-ttu-id="0a305-126">Os dados de byte de montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="0a305-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="0a305-127">-AssemblyFilePath</span></span>
<span data-ttu-id="0a305-128">O caminho do arquivo de montagem de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="0a305-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="0a305-129">-ContentLink</span></span>
<span data-ttu-id="0a305-130">Um link publicamente acessível para os dados de montagem da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="0a305-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a305-131">-DefaultProfile</span></span>
<span data-ttu-id="0a305-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a305-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a305-133">-Metadados</span><span class="sxs-lookup"><span data-stu-id="0a305-133">-Metadata</span></span>
<span data-ttu-id="0a305-134">Os metadados de montagem da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="0a305-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a305-135">-Name</span></span>
<span data-ttu-id="0a305-136">O nome de montagem da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="0a305-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="0a305-137">-ParentName</span></span>
<span data-ttu-id="0a305-138">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-138">The integration account name.</span></span>

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

### <span data-ttu-id="0a305-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a305-139">-ParentObject</span></span>
<span data-ttu-id="0a305-140">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-140">An integration account object.</span></span>

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

### <span data-ttu-id="0a305-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a305-141">-ParentResourceId</span></span>
<span data-ttu-id="0a305-142">A ID de recurso da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0a305-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="0a305-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a305-143">-ResourceGroupName</span></span>
<span data-ttu-id="0a305-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a305-144">The resource group name.</span></span>

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

### <span data-ttu-id="0a305-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a305-145">-Confirm</span></span>
<span data-ttu-id="0a305-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a305-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a305-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a305-147">-WhatIf</span></span>
<span data-ttu-id="0a305-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a305-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a305-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a305-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a305-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a305-150">CommonParameters</span></span>
<span data-ttu-id="0a305-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a305-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a305-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a305-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a305-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a305-153">INPUTS</span></span>

### <span data-ttu-id="0a305-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0a305-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="0a305-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0a305-155">System.String</span></span>

## <span data-ttu-id="0a305-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a305-156">OUTPUTS</span></span>

### <span data-ttu-id="0a305-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a305-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="0a305-158">Notas</span><span class="sxs-lookup"><span data-stu-id="0a305-158">NOTES</span></span>

## <span data-ttu-id="0a305-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a305-159">RELATED LINKS</span></span>
